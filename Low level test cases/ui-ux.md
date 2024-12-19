# Interfejs użykownika i UX

---

### TC-UIUX-01: Weryfikacja czy pliki są otwierane przez aplikację domyślne

**Cel:** Sprawdzić, czy przy próbie użytkownika otworzyć plik, otwiera się on w aplikacji domyślnej  
**Powiązane wymaganie:** REQ-FUNC-04
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive
- Zainstalowane i uznane jako domyślne Word (dla `.docx`), Microsoft Edge, Google Chrome bądź Adobe Acrobat (dla `.pdf`), CodeBlocks, VisualStudio Code (dla `.c`) .
- Zainstalowana aplikacja SpaceDrive.

**Kroki:**

1. Otwórzcie aplikację Word.
2. Wklejcie do nowego pliku zawartość tego testcase'u.
3. Zapiście ten plik w folder `Documents` jako `test.docx`, `test.pdf`.

4. W notepad, VScode bądż Codeblocks stwórzcie plik `test.c` zawirający aplikację 'Hello world' w języku c;
5. SpaceDrive'ie otwórzcie folder `Documents` i spróbujcie otworzyć pliki `test.docx`, `test.pdf`, `test.c`.
   **Oczekiwane wyniki:**

- Zainstalowana aplikacja SpaceDrive
- Plik `test.docx` otworzy się w aplikacji Microsoft Word.
- Plik `test.pdf` otworzy się w domyślnej aplikacji dla plików pdf.
- Plik `test.pdf` otworzy się w domyślnej aplikacji dla plików `.c`.

---

### TC-UIUX-02: Weryfikacja czy działa Drag & Drop między folderami, dyskami i urządzeniami

**Cel:** Sprawdzić, czy Drag & Drop między folderami działa poprawnie, plik jest dostępny w nowym miejsciu i nie ma go w starej lokacji.
**Powiązane wymaganie:** REQ-FUNC-07
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive
- Pliki stworzone w TC-UIUX-01
- Domyślne windowsowe foldery `Documments` i `Pictures`.
- Defoltowy systemowy file explorer.

**Kroki:**

1. Otworzcie folder `Documents` i `Pictures` w dwóch różnych okienkach SpaceDrive.
2. Spróbujcie przeciągnuć plik `test.c` do folderu `Pictures` używając Drag&Drop.
3. Spróbujcie przeciągnuć plik `test.docx`, `test.pdf` do folderu `Pictures` używając Drag&Drop.
4. Spróbujcie otworzyć te pliki w nowej lokalizacji przez systemowy file explorer.

**Oczekiwane wyniki:**

- Pliki będą się znajdować w nowej lokalizacji.
- Pliki po przeniesieniu nie zmienią swojej treści.

---

### TC-UIUX-03: Weryfikacja czy działa Drag & Drop z innych aplikacji

**Cel:** Sprawdzić, czy da się pomyślnie przeciągnać pliki z innych aplikacji do SpaceDrive (plik jest dostępny w docelowym folderze/urządzeniu).
**Powiązane wymaganie:** REQ-FUNC-08
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive
- Pliki stworzone w TC-UIUX-01 i w lokalizacji jak w końcu TC-UIUX-02
- Domyślne windowsowe foldery `Documments` i `Pictures` w systemowym file exploreru.
  **Kroki:**

1. Otworzcie folder `Pictures` przez systemowy file explorer,a folder `Documents` w SpaceDrive.
2. Spróbujcie przeciągnuć plik `test.c` do folderu `Documents` używając Drag&Drop.
3. Spróbujcie przeciągnuć plik `test.docx`, `test.pdf` do folderu `Documents` używając Drag&Drop.
4. Spróbujcie otworzyć te pliki w `Doucments` przez systemowy file explorer.

**Oczekiwane wyniki:**

- Pliki będą się znajdować w folderze `Documents`.
- Pliki po przeniesieniu nie zmienią swojej treści.

---

### TC-UIUX-04: Weryfikacja responsywności wyświetlanie elementów interfejsu

**Cel:** Sprawdzić, czy poprawnie wyświetlają się wszystkie elementy interfejsu, responsywnie widok adaptuje się do wymiarów i rozdzielczości.
**Powiązane wymaganie:** REQ-NFUNC-02
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive

**Kroki:**

1. Otwórzcie aplikację SpaceDrive w trybie pełnoekranowym.
2. Spróbujcie zmniejszyć szerokosć okienka.
3. Spróbujcie zmniejszyć szerokosć okienka.
   zmniejszyć wysokość okienka.
4. Spróbujcie zwiększyć szerokość okienka.
5. Spróbujcie zwiększyć wysokość okienka.
6. Spróbujcie jednoczesnie zmieniać wysokość i szerokość.

**Oczekiwane wyniki:**

- Aplikacja ciągle adaptuje się do nowych rozmiarów okienka.
- Nie ma nie uzywanych fragmetów okienka.
- Przy minimałnych rozmiarach aplikacja nadaje się do wykorzystania

---

### TC-UIUX-05: Weryfikacja czasu uruchomienia aplikacji

**Cel:** Sprawdzić, czy aplikacja otworzy się w czasie mniejszym niż 5 sekund na standardowych urządzeniach.
**Powiązane wymaganie:** REQ-NFUNC-06
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive
- Sekundomierz (jako odrębne uzrądzenia, aplikacja na komurce czy komputerze).
- Urządzenia które odpowiada definicji standardowego urządzenia.
  **Kroki:**

1. Przygotujcie i wyzerujcie sekundomierz.
2. Jednoczesnie otworzcie aplikację i zacznicie mierzyć czas.
3. Zaraz po odpalaniu aplikacji nacisnicie na Stop.
4. Zapiście wynik.
5. Powtórzcie kroki 2-4 jeszcze 5-10 razy.
6. Polićcie śriedni czas odpalania
   **Oczekiwane wyniki:**

- Śriedni czas odpalania ma być mniejszy niż 5 sekund.
