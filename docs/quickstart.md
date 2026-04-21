# Jak zacząć?

## Companion

Jeśli dołączasz jako posiadacz urządzenia typu companion:

1. Upewnij się, że ustawiony preset to EU/UK Narrow ([zobacz szczegóły](/presets)).
2. Dołącz do kanałów używanych w Wielkopolsce ([lista kanałów](/channels)).
3. Ustaw region `pl` dla kanału `public` oraz `wlkp` dla pozostałych kanałów, szczególnie `#wlkp` ([zobacz instrukcję](/regions/#konfiguracja-regionu-dla-wiadomosci)).

<details><summary>Szczegółowa instrukcja krok po kroku</summary>
    <ol>
        <li>
            Ustawienie presetu EU/UK Narrow:
            <ol>
               <li>Otwórz aplikację MeshCore i jeśli to konieczne, połącz się ze swoim companionem.</li>
               <li>W prawym górnym rogu wybierz ikonę koła zębatego, aby otworzyć ustawienia.</li>
               <li>Przewiń do sekcji "Radio SettingsUstawienia radiowe" i kliknij przycisk "Choose Preset/Wybierz preset".</li>
               <li>Z pomocą wyszukiwarki znajdź "EU/UK (Narrow), Switzerland" i wybierz go.</li>
               <li>Zapisz zmiany, klikając ikonę ptaszka w prawym górnym rogu.</li>
            </ol>
        </li>
        <li>
            Dołączanie do kanałów:
            <ol>
               <li>Z ekranu głównego aplikacji MeshCore wybierz na dole kartę "Channels/Kanały".</li>
               <li>Otwórz menu, klikając ikonę trzech kropek w prawym górnym rogu i wybierz opcję "Add Channel/Dodaj kanał".</li>
               <li>Wybierz opcję "Join a Hashtag Channel/Dołącz do hashtagowego kanału".</li>
               <li>Podaj nazwę kanału, rozpoczynając od znaku `#`, np. `#wlkp`, a następnie zapisz, klikając przycisk "Join channel/Dołącz do kanału" oraz "Continue to channel/Przejdź do kanału".</li>
               <li>Powtórz dla pozostałych kanałów zgodnie z [listą](/channels).</li>
             </ol>
        </li>
        <li>
            Ustawianie regionu:
            <ol>
               <li>Otwórz kanał, dla którego chcesz ustawić region, np. wlkp.</li>
               <li>Otwórz menu, klikając ikonę trzech kropek w prawym górnym rogu i wybierz opcję "Set Region Scope/Ustaw zakres regionu".</li>
               <li>W prawym górnym rogu wybierz "+", dodaj region `wlkp` i zapisz "ptaszkiem" w prawym górnym rogu. Hasztag i wielkość znaków mają znaczenie!</li>
               <li>Po zapisaniu zmian aplikacja przeniesie Cię do ekranu "Select Region/Wybierz region". Wybierz `wlkp` klikając w niego.</li>
               <li>Powtórz dla pozostałych kanałów ustawiając region zgodnie z [listą](/channels).</li>
            </ol>
        </li>
    </ol>
</details>


## Repeater

Jeśli jesteś właścicielem repeatera:

1. Upewnij się, że ustawiony preset odpowiada używanemu w Wielkopolsce - EU/UK Narrow ([zobacz szczegóły](/presets)).
2. Zsynchronizuj czas (i pamiętaj, by robić to każdorazowo po odłączeniu zasilania): po zalogowaniu do repeatera przejdź do ustawień (`settings`), a następnie wybierz `Sync Clock`.
3. Dodaj do repeatera regiony `wlkp` i `pl` ([zobacz instrukcję](/regions/#konfiguracja-repeatera)).
4. Ustaw długość prefixu w advertach na 3 bajty.
5. *(opcjonalnie)* Ustaw dane właściciela repeatera: po zalogowaniu do repeatera przejdź do ustawień (`settings`), a następnie wybierz `Owner Info`.

<details><summary>Szczegółowa instrukcja krok po kroku</summary>
    <ol>
        <li>
            Ustawienie presetu EU/UK Narrow:
            <ol>
               <li>Otwórz aplikację MeshCore i jeśli to konieczne, połącz się ze swoim companionem.</li>
               <li>Z dolnego menu wybierz "Contacts/Kontakty", a następnie wybierz repeater, którym zarządzasz i zaloguj się do niego jako administrator.</li>
               <li>Z dolnego menu wybierz pozycję "Settings/Ustawienia".</li>
               <li>Przewiń do sekcji "Radio Settings/Ustawienia radiowe", kliknij ikonę trzech kropek, by otworzyć menu i wybierz opcję "Choose Preset/Wybierz preset".</li>
               <li>Z pomocą wyszukiwarki znajdź "EU/UK (Narrow), Switzerland" i wybierz go.</li>
               <li>Zapisz zmiany, klikając ikonę ptaszka w prawym górnym rogu.</li>
            </ol>
        </li>
        <li>
            Synchronizacja czasu:
            <ol>
               <li>Po zalogowaniu do repeatera z dolnego menu wybierz pozycję "Settings/Ustawienia".</li>
               <li>Przewiń w doł i wybierz pozycję "Sync Clock/Synchronizuj zegar".</li>
            </ol>
        </li>
        <li>
            Dodawanie regionu:
            <ol>
                <li>W aplikacji MeshCore, po zalogowaniu do repeatera, z dolnego menu wybierz pozycję "Settings/Ustawienia".</li>
                <li>Znajdź pozycję "Manage Regions/Zarządzaj regionami", a następnie w prawym górnym roku wybierz ikonę "+".</li>
                <li>Dodaj region "wlkp" i zatwierdź "ptaszkiem". Uwaga! Wielkość liter MA znaczenie!</li>
                <li>Przy nowo utworzonym regionie kliknij trzy kropeczki i wybierz opcję "Allow Flood/Zezwól na flood".</li>
                <li>Dodaj region "pl" i zatwierdź "ptaszkiem". Uwaga! Wielkość liter MA znaczenie!</li>
                <li>Przy nowo utworzonym regionie kliknij trzy kropeczki i wybierz opcję "Allow Flood/Zezwól na flood".</li>
                <li>Zapisz zmiany klikając "ptaszka" w prawym górnym rogu.</li>
            </ol>
        </li>
        <li>
            Konfiguracja długości prefixów w advertach:
            <ol>
                <li>W aplikacji MeshCore, po zalogowaniu do repeatera, z dolnego menu wybierz pozycję "CLI/Wiersz poleceń".</li>
                <li>Wpisz komendę `set path.hash.mode 2` i wyślij.</li>
            </ol>
        </li>
        <li>
            Ustawianie danych właściciela:
            <ol>
                <li>Po zalogowaniu do repeatera z dolnego menu wybierz pozycję "Settings/Ustawienia".</li>
                <li>Przewiń w doł i wybierz pozycję "Owner Info/Informacje o właścicielu".</li>
                <li>Wpisz nazwę, którą posługujesz się na companionie i zatwierdź, klikając ikonę "ptaszka".</li>
            </ol>
        </li>
    </ol>
</details>



## Boty

Jeśli jesteś właścicielem Bota:

1. Upewnij się, że wysyłane przez niego wiadomości są ograniczone do regionu `wlkp`: podłącz companiona wykorzystywanego przez bota do komputera, wejdź na https://app.meshcore.nz/ i skonfiguruj region `wlkp` dla kanałów podobnie, jak w przypadku companionów.