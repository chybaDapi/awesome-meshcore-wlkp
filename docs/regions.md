# Regionalizacja

## Jak to działa na poziomie aplikacji?
Regionalizacja aplikowana jest tylko do wiadomości wysyłanych na kanałach i NIE wpływa na prywatne wiadomości (DM) wysyłane bezpośrednio do innych użytkowników oraz adverty.

Aplikacja umożliwia definiowanie regionów, do których wysyłane są wiadomości. Można skonfigurować wiele regionów, jednak dana wiadomość może być wysłana jednorazowo tylko do jednego regionu. Wyboru regionu dokonuje się na każdym kanale osobno, a wybór można w każdej chwili zmienić. Wiadomości bez zdefiniowanego regionu przyjmują domyślnie jako region symbol wieloznaczny, czyli `*`.

## Jak to działa na poziomie repeaterów?
Oprogramowanie repeaterów do wersji 1.10 ignoruje regiony i przekazuje wszystkie wiadomości dalej.

Od wersji 1.10 dodane zostało wsparcie dla regionalizacji. Wszystkie repeatery począwszy od tej wersji otrzymują domyślną konfigurację pozwalającą na przekazywanie wiadomości z symbolem wieloznacznym (`*`), czyli wiadomości bez zdefiniowanego zakresu. Z poziomu linii komend (poprzez aplikację lub przeglądarkę) administrator może dodawać regiony oraz definiować, które regiony mają być przekazywane dalej, a które nie.

!!! Warning "Uwaga!"

    Symbol wieloznaczności nie oznacza przekazywanie wiadomości ze zdefiniowanym dowolnym regionem. Oznacza on przekazywanie wiadomości bez zdefiniowanego regionu!


!!! Tip "Wskazówka"

    Jeśli chcemy, by wiadomości ze zdefiniowanym danym regionem były przekazywane dalej, nie wystarczy dodać region do repeatera. Trzeba jeszcze jawnie zadeklarować, że mają być one przekazywane.


!!! Tip "Wskazówka"

    Pominięcie regionu na repeaterze, dodanie regionu bez zezwolenia na przekazywanie oraz dodanie regionu z zakazem przekazywania są ze sobą jednoznaczne i działają tak samo.



## Przykładowe konfiguracje repeaterów, regiony wiadomości oraz statusy
 Regiony repeatera                               | Region wiadomości | Status           
|-------------------------------------------------|-------------------|------------------|
| ✅ *                                             | brak regionu      | 🟢 przekazana    |
| ✅ *                                             | #poznan           | 🟠 zignorowana   |
| ✅ *<br>❌ #poznan                                | brak regionu      | 🟢 przekazana    |
| ✅ *<br>❌ #poznan                                | #poznan           | 🟠 zignorowana   |
| ✅ *<br>✅ #poznan                                | brak regionu      | 🟢 przekazana    |
| ✅ *<br>✅ #poznan                                | #poznan           | 🟢 przekazana    |
| ❌ *<br>✅ #poznan                                | brak regionu      | 🟠 zignorowana   |
| ❌ *<br>✅ #poznan                                | #poznan           | 🟢 przekazana    |
| ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | brak regionu      | 🟢 przekazana    |
| ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #poznan           | 🟢 przekazana    |
| ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #leszno           | 🟢 przekazana    |
| ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #gniezno          | 🟠 zignorowana   |
| ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #kalisz           | 🟠 zignorowana   |

Legenda:<br>
✅ - przekazywanie wiadomości w danym regionie włączone <br>
❌ - przekazywanie wiadomości w danym regionie wyłączone


## Co nie jest problemem?
1. Repeatery ze oprogramowaniem starszym niż wersja 1.10 nadal będą przekazywać wszystkie wiadomości.
2. Z poziomu aplikacji można łatwo przełączać się między regionami.
3. Repeatery mogą obsługiwać jednocześnie zarówno wiadomości ze zdefiniowanymi regionami, jak i bez regionów.

## Co może być problemem?
1. Repeatery bez zdefiniowanych regionów nie będą przekazywać wiadomości ze zdefioniowanym regionem, nawet jeśli nie jest on jawnie wyłączony na repeaterze. Oznacza to, że decydując się na używanie regionu dla danego kanału, należy zadbać, żeby wszystkie zainteresowane repeatery wprost zezwalały na jego przekazywanie.
