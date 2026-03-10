## Konwencja nazewnictwa
Podobnie jak w pozostałych regionach, w Wielkopolsce nie obowiązuje jedna, spójna konwencja nazewnictwa repeaterów. 
Staraj się jednak nazywać swoje repeatery w taki sposób, by nazwa wskazywała mniej więcej na okolicę, w której znajduje 
się urządzenie (np. nazwa dzielnicy lub osiedla), np. `POZNAN-RATAJE` lub `POZ_RAT`. Możesz też dodać dowolną nazwę 
własną, która ułatwi Ci identyfikację Twoich urządzeń, np. `POZ_RAT_ADAM`.

### Repeatery testowe
Ze zwględów praktycznych, wielu z nas ma wyłączone automatyczne dodawanie kontektów. Pojemność listy kontaktów jest 
ograniczona, a posiadanie repeatera w kontaktach ułatwia np. śledzenie trasy oraz umożliwia podejrzenie telemetrii.
Aby ułatwić innym zarządzanie kontaktami, jeśli stawiasz urządzenie type repeater tymczasowo lub testowo, dodaj
do nazwy suffix `TEST`, np. `POZ_RAT_ADAM_TEST`

### Repeatery solarne (off-grid)
Jeśli budujesz **urządzenie typu off-grid** (tzn. zasilane wyłącznie energią słoneczną), na końcu nazwy dodaj 
**symbol gwiazdki** (`*`), np. `POZ_RAT_ADAM*`. Pomoże to w zorientowaniu się, na które urządzenia możemy 
liczyć w czasie blackoutów. To bardzo cenna informacja, ponieważ założeniem sieci MeshCore jest to, by działała
jako alternatywna sieć kryzysowa, odporna na braki prądu.


## Hasło gościa
Konfigurując repeater, masz możliwość ustawienia dwóch haseł: administratora oraz gościa. Pierwsze z nich powinno być silne
i znane tylko Tobie. Mocno sugerowane jest, aby jako hasło gościa, zgodnie z praktykami stosowanymi w innych częściach 
kraju, należy ustawić `hello`.


## Regiony
W Wielkopolskiej Sieci MeshCore aktywnie wykorzystujemy regiony. Aby sieć mogła działać poprawnie, jako operator repeatera powinieneś skonfigurować na swoim urządzeniu obsługę regionu `#wlkp`.

1. W aplikacji MeshCore, po zalogowaniu do repeatera, z dolnego menu wybierz pozycję "Settings".
2. Znajdź pozycję "Manage Regions", a następnie w prawym górnym roku wybierz ikonę "+".
3. Dodaj region "wlkp" i zatwierdź "ptaszkiem". Uwaga! Wielkość liter MA znaczenie!
4. Przy nowo utworzonym regionie kliknij trzy kropeczki i wybierz opcję "Allow Flood".
5. Zapisz zmiany klikając "ptaszka" w prawym górnym rogu.