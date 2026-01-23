## Regionalizacja - jak to działa?

### Jak to działa na poziomie aplikacji?
Regionalizacja aplikowana jest tylko do wiadomości wysyłanych na kanałach i NIE wpływa na prywatne wiadomości (DM) wysyłane bezpośrednio do innych użytkowników oraz adverty.

Aplikacja umożliwia definiowanie regionów, do których wysyłane są wiadomości. Można skonfigurować wiele regionów, jednak dana wiadomość może być wysłana jednorazowo tylko do jednego regionu. Wyboru regionu dokonuje się na każdym kanale osobno, a wybór można w każdej chwili zmienić. Wiadomości bez zdefiniowanego regionu przyjmują domyślnie jako region symbol wieloznaczny, czyli `*`.

### Jak to działa na poziomie repeaterów?
Oprogramowanie repeaterów do wersji 1.10 ignoruje regiony i przekazuje wszystkie wiadomości dalej.

Od wersji 1.10 dodane zostało wsparcie dla regionalizacji. Wszystkie repeatery począwszy od tej wersji otrzymują domyślną konfigurację pozwalającą na przekazywanie wiadomości z symbolem wieloznacznym (`*`), czyli wiadomości bez zdefiniowanego regionu. Z poziomu linii komend (poprzez aplikację lub przeglądarkę) administrator może dodawać regiony oraz definiować, które regiony mają być przekazywane dalej, a które nie.

!!! Warning "Uwaga!"

    Symbol wieloznaczności nie oznacza przekazywanie wiadomości ze zdefiniowanym dowolnym regionem. Oznacza on przekazywanie wiadomości bez zdefiniowanego regionu!


!!! Tip "Wskazówka"

    Jeśli chcemy, by wiadomości ze zdefiniowanym danym regionem były przekazywane dalej, nie wystarczy dodać region do repeatera. Trzeba jeszcze jawnie zadeklarować, że mają być one przekazywane.


!!! Tip "Wskazówka"

    Pominięcie regionu na repeaterze, dodanie regionu bez zezwolenia na przekazywanie oraz dodanie regionu z zakazem przekazywania są ze sobą jednoznaczne i działają tak samo.



### Przykładowe konfiguracje repeaterów, regiony wiadomości oraz statusy
 Regiony repeatera                               | Region wiadomości | Status           
-------------------------------------------------|-------------------|------------------
 ✅ *                                             | brak regionu      | 🟢 przekazana    
 ✅ *                                             | #poznan           | 🟠 zignorowana   
 ✅ *<br>❌ #poznan                                | brak regionu      | 🟢 przekazana    
 ✅ *<br>❌ #poznan                                | #poznan           | 🟠 zignorowana   
 ✅ *<br>✅ #poznan                                | brak regionu      | 🟢 przekazana    
 ✅ *<br>✅ #poznan                                | #poznan           | 🟢 przekazana    
 ❌ *<br>✅ #poznan                                | brak regionu      | 🟠 zignorowana   
 ❌ *<br>✅ #poznan                                | #poznan           | 🟢 przekazana    
 ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | brak regionu      | 🟢 przekazana    
 ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #poznan           | 🟢 przekazana    
 ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #leszno           | 🟢 przekazana    
 ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #gniezno          | 🟠 zignorowana   
 ✅ *<br>✅ #poznan<br>✅ #leszno<br>❌ #gniezno     | #kalisz           | 🟠 zignorowana   

Legenda:<br>
✅ - przekazywanie wiadomości w danym regionie włączone <br>
❌ - przekazywanie wiadomości w danym regionie wyłączone


## Testowe ustawienia dla Wielkopolskiej Sieci
W ramach testów, komunikacja na kanale `#wlkp` odbywa się z uwzględnieniem regionu `#wlkp`. Poniżej znajdziesz opis co musisz zrobić, 
aby dołączyć do testów oraz co się stanie, jak nie podejmiesz żadnej akcji.

### Jak dołączyć do testów?

#### Konfiguracja repeatera
Jeśli jesteś operatorem repeatera, skonfiguruj na nim region `#wlkp`. To proste, zajmuje mniej niż minutę, a jednocześnie nie wprowadza żadnych ograniczeń. 
Twój repeater po zmianach nadal będzie przekazywać te same wiadomości co wcześniej, a DODATKOWO wiadomości kierowane do regionu #wlkp.

Poniższa konfiguracja wpływa na to, jakie regiony Twój repeater słyszy i przekazuje dalej. Nie wpływa na wiadomości bez regionów. Nie wpływa na ustawienia kanałów.

Konfiguracji możesz dokonać na dwa sposoby: zdalnie poprzez aplikację MeshCore oraz poprzez konsolę dostępną na stronie https://flasher.meshcore.co.uk/ po podłączeniu repeatera kablem USB do komputera.
W obu przypadkach konfiguracja wygląda tak samo. Poniżej instrukcja zdalnej konfiguracji poprzez aplikację mobilną:
1. Zaloguj się do repeatera poprzez aplikację i przejdź do zakładki "Command Line".
2. Wpisz trzy komendy: `region put #wlkp`, `region allowf #wlkp` i `region save`. Uwaga! Początkowy hasztag i wielkość znaków mają znaczenie!
3. Gotowe.

Jeśli chcesz wycofać zmiany:
1. Zaloguj się do repeatera poprzez aplikację i przejdź do zakładki "Command Line".
2. Wpisz komendy: `region remove #wlkp` i `region save`.
3. Gotowe.

!!! Info "Info"

    \#wlkp w komendach powyżej odnosi się do nazwy regionu. Nie jest to powiązane z nazwą kanału.
    
    
#### Konfiguracja regionu dla wiadomości
Ta zmiana pozwoli Ci zdecydować, gdzie chcesz, żeby były widoczne Twoje wiadomości. W ramach testów, komunikacja na kanale `#wlkp` odbywa się w ramach regionu `#wlkp`.
Poniższa zmiana nie wpływa na żadne inne kanały, prywatne wiadomości oraz adverty. Nie wpływa też na wiadomości odbierane przez Ciebie na kanale `#wlkp`. 
Poniższa zmiana wpływa jedynie na wiadomości wysyłane przez Ciebie na kanał `#wlkp`.

1. Otwórz w aplikacji MeshCore kanał `#wlkp`.
2. Z menu w prawym górnym rogu wybierz "Set Region Scope"
3. W prawym górnym rogu wybierz "+", dodaj region `#wlkp` i zapisz "ptaszkiem" w prawym górnym rogu. Hasztag i wielkość znaków mają znaczenie!
4. Po zapisaniu zmian aplikacja przeniesie Cię do ekranu "Select Region". Wybierz `#wlkp` klikając w niego. 
5. Po powrocie do kanału pojawia się na górze potwierdzenie: "Only repeaters allowing region will forward."
6. Gotowe.

Od teraz wiadomości wysłane przez Ciebie na kanał `#wlkp` nie będą przekazywane dalej przez repeatery bez skonfigurowanego regionu `#wlkp`.

Jeśli chcesz wycofać zmianę tymczasowo (możesz wysłać pojedynczą wiadomość bez zdefiniowanego regionu) lub na stałe, wykonaj poniższe kroki:
1. Otwórz kanał `#wlkp`.
2. Z menu w prawym górnym rogu wybierz "Set Region Scope"
3. W prawym górnym rogu z menu oznaczonego trzema kropkami wybierz "Clear Scope".
4. Gotowe. 

Teraz wszystkie Twoje wiadomości wysłane na kanał `wlkp` będą przekazywane dalej przez wszystkie repeatery w zasięgu.


#### Jeśli nie zrobisz nic...
Jeśli nie zrobisz nic, Twoje wiadomości nadal będą widoczne dla wszystkich, jednak mogą "wyciekać" poza nasz region, a w dobrych warunkach również poza granice kraju. 
Jeśli jesteś operatorem repeatera, nie będzie on przekazywał dalej wiadomości z kanału `#wlkp` wysyłanych ze zdefiniowanym regionem `#wlkp`. Jeśli nie jesteś w zasięgu innego repeatera
ze zdefiniowanym regionem, część wiadomości na kanale `#wlkp` może do Ciebie nie docierać. 
