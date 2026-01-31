# Jak zacząć?

## Companion
Jeśli dołączasz jako posiadacz urządzenia typu companion:
1. Upewnij się, że ustawiony preset odpowiada używanemu w Wielkopolsce - EU/UK Narrow ([zobacz szczegóły](/presets)).
2. Dołącz do kanałów używanych w Wielkopolsce ([lista kanałów](/channels)).
3. Ustaw region `#wlkp` dla kanału `#wlkp` ([zobacz instrukcję](/regions/#konfiguracja-regionu-dla-wiadomosci)).

<details><summary>Szczegółowa instrukcja krok po kroku</summary>

1. Ustawienie presetu EU/UK Narrow:
   - Otwórz aplikację MeshCore i jeśli to konieczne, połącz się ze swoim companionem.
   - W prawym górnym rogu wybierz ikonę koła zębatego, aby otworzyć ustawienia.
   - Przewiń do sekcji "Radio Settings" i kliknij przycisk "Choose Preset".
   - Z pomocą wyszukiwarki znajdź "EU/UK (Narrow)" i wybierz go.
   - Zapisz zmiany, klikając ikonę ptaszka w prawym górnym rogu.
2. Dołączanie do kanałów:
   - Z ekranu głównego aplikacji MeshCore wybierz na dole kartę "Channels".
   - Otwórz menu, klikając ikonę trzech kropek w prawym górnym rogu i wybierz opcję "Add Channel".
   - Wybierz opcję "Join a Hashtag Channel".
   - Podaj nazwę kanału, rozpoczynając od znaku `#`, a następnie zapisz, klikając przycisk "Join channel" oraz "Continue to channel". Listę używanych kanałów sprawdzisz [tutaj](/channels).
3. Ustawianie regionu:
   - Otwórz kanał, dla którego chcesz ustawić region, np. #wlkp.
   - Otwórz menu, klikając ikonę trzech kropek w prawym górnym rogu i wybierz opcję "Set Region Scope".
   - W prawym górnym rogu wybierz "+", dodaj region `#wlkp` i zapisz "ptaszkiem" w prawym górnym rogu. Hasztag i wielkość znaków mają znaczenie!
   - Po zapisaniu zmian aplikacja przeniesie Cię do ekranu "Select Region". Wybierz `#wlkp` klikając w niego.
</details>


## Repeater
Jeśli jesteś właścicielem repeatera:
1. Upewnij się, że ustawiony preset odpowiada używanemu w Wielkopolsce - EU/UK Narrow ([zobacz szczegóły](/presets)).
2. Zsynchronizuj czas (i pamiętaj, by robić to każdorazowo po odłączeniu zasilania): po zalogowaniu do repeatera przejdź do ustawień (`settings`), a następnie wybierz `Sync Clock`.
3. Dodaj do repeatera region `#wlkpl` ([zobacz instrukcję](/regions/#konfiguracja-repeatera)).
4. *(opcjonalnie)* Ustaw dane właściciela repeatera: po zalogowaniu do repeatera przejdź do ustawień (`settings`), a następnie wybierz `Owner Info`.


<details><summary>Szczegółowa instrukcja krok po kroku</summary>

1. Ustawienie presetu EU/UK Narrow:
   - Otwórz aplikację MeshCore i jeśli to konieczne, połącz się ze swoim companionem.
   - Z dolnego menu wybierz "Contacts", a następnie wybierz repeater, którym zarządzasz i zaloguj się do niego jako administrator.
   - Z dolnego menu wybierz pozycję "Settings".
   - Przewiń do sekcji "Radio Settings", kliknij ikonę trzech kropek, by otworzyć menu i wybierz opcję "Choose Preset".
   - Z pomocą wyszukiwarki znajdź "EU/UK (Narrow)" i wybierz go.
   - Zapisz zmiany, klikając ikonę ptaszka w prawym górnym rogu.
2. Synchronizacja czasu:
   - Po zalogowaniu do repeatera z dolnego menu wybierz pozycję "Settings".
   - Przewiń w doł i wybierz pozycję "Sync Clock".
3. Dodawanie regionu:
   - Po zalogowaniu do repeatera z dolnego menu wybierz pozycję "Command Line".
   - Wpisz kolejno trzy komendy, każdorazowo zatwierdzając je enterem: `region put #wlkp`, `region allowf #wlkp` i `region save`. Uwaga! Początkowy hasztag i wielkość znaków mają znaczenie!
4. Ustawianie danych właściciela:
    - Po zalogowaniu do repeatera z dolnego menu wybierz pozycję "Settings".
    - Przewiń w doł i wybierz pozycję "Owner Info".
    - Wpisz nazwę, którą posługujesz się na companionie i zatwierdź, klikając ikonę ptaszka.
</details>
