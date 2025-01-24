![logo](https://github.com/user-attachments/assets/5acd29fe-498a-4095-a053-6ca493813a8b)

# Raport z Testów Aplikacji Spacedrive

## 1. Wprowadzenie

Testy aplikacji **Spacedrive** miały na celu weryfikację funkcjonalności, wydajności, kompatybilności oraz zgodności z wymaganiami bezpieczeństwa. Testy obejmowały zarówno przypadki wysokopoziomowe (**High-Level Test Cases**), jak i szczegółowe przypadki niskopoziomowe (**Low-Level Test Cases**).

---

## 2. Zespół

![squad](https://github.com/user-attachments/assets/2e0ce7e9-10c4-40c6-b4f3-0a8f9701dc64)

### 2.1 Zakres obowiązków

- **Michał Skrobot**: przygtowanie przypadków testowych, raportu z testów i tester
- **Adam Tytoń**: przygtowanie przypadków testowych i tester
- **Oleksandr Stehura**: przygtowanie przypadków testowych i tester
- **Jakub Paczek**: przygtowanie przypadków testowych i tester

---

## 3. Zakres Testów

Przeprowadzone testy objęły następujące obszary:

- **Zarządzanie plikami**: kopiowanie, przenoszenie, zmiana nazw, tworzenie folderów.
- **Synchronizacja i integracja**: transfer danych między urządzeniami, synchronizacja w czasie rzeczywistym, integracja z usługami chmurowymi.
- **Wydajność**: czas odpowiedzi aplikacji, generowanie miniatur, responsywność interfejsu.
- **Bezpieczeństwo**: uzyskiwanie uprawnień dostępu do plików, szyfrowanie folderów, minimalizacja danych telemetrycznych.

---

## 4. Wyniki Testów

### 4.1 Przypadki Testowe

#### Zarządzanie plikami

| ID Testu        | Wynik        |
| --------------- | ------------ |
| TC-FILE-MGMT-01 | ✅ Pozytywny |
| TC-FILE-MGMT-02 | ❌ Negatywny |
| TC-FILE-MGMT-03 | ✅ Pozytywny |
| TC-FILE-MGMT-04 | ✅ Pozytywny |
| TC-FILE-MGMT-05 | ✅ Pozytywny |
| TC-FILE-MGMT-06 | ✅ Pozytywny |

#### Integracja i synchronizacja

| ID Testu         | Wynik        |
| ---------------- | ------------ |
| TC-INTEG-SYNC-01 | ✅ Pozytywny |
| TC-INTEG-SYNC-02 | ✅ Pozytywny |
| TC-INTEG-SYNC-03 | ✅ Pozytywny |
| TC-INTEG-SYNC-04 | ✅ Pozytywny |
| TC-INTEG-SYNC-05 | ✅ Pozytywny |
| TC-INTEG-SYNC-06 | ✅ Pozytywny |
| TC-INTEG-SYNC-07 | ✅ Pozytywny |

#### Wydajność i optymalizacja

| ID Testu  | Wynik        |
| --------- | ------------ |
| TC-PER-01 | ✅ Pozytywny |
| TC-PER-02 | ✅ Pozytywny |
| TC-PER-03 | ✅ Pozytywny |
| TC-PER-04 | ✅ Pozytywny |

#### Bezpieczeństwo i prywatność

| ID Testu       | Wynik        |
| -------------- | ------------ |
| TC-SEC-PRIV-01 | ❌ Negatywny |
| TC-SEC-PRIV-02 | ✅ Pozytywny |
| TC-SEC-PRIV-03 | ✅ Pozytywny |
| TC-SEC-PRIV-04 | ✅ Pozytywny |

#### Interfejs użytkownika i UX

| ID Testu   | Wynik        |
| ---------- | ------------ |
| TC-UIUX-01 | ✅ Pozytywny |
| TC-UIUX-02 | ❌ Negatywny |
| TC-UIUX-03 | ❌ Negatywny |
| TC-UIUX-04 | ❌ Negatywny |
| TC-UIUX-05 | ✅ Pozytywny |

---

### 4.2 Problemy Znalezione w Przypadkach Testowych

#### TC-SEC-PRIV-01

- **Opis problemu**:

  - Aplikacja nie wyświetla komunikatu o braku uprawnień do plików/folderów ani nie prosi o uzyskanie dostępu.
  - Brak informacji o braku dostępu do folderów powoduje, że użytkownik nie wie, dlaczego foldery są niewidoczne lub nie można ich otworzyć.

- **Notatki**:
  - Dla folderów z ograniczonymi uprawnieniami aplikacja nie wyświetla żadnego komunikatu ostrzegawczego ani prośby o dostęp.

#### TC-FILE-MGMT-02

- **Opis problemu**:

  - Udało się stworzyć system folderów według schematu.
  - Dodano tag do `file3`.
  - Nie udało się dodać folderu do paska — błąd: **"Not supported nested folders"**.
  - Folder `folder1` udało się usunąć przez SpaceDrive.
  - Folder `folder2` nie mógł zostać usunięty, dopóki aplikacja SpaceDrive nie została zamknięta.
  - Po zamknięciu SpaceDrive wszystkie foldery zostały poprawnie usunięte.

- **Notatki**:
  - Po przeglądaniu foldera w SpaceDrive, nie można go usunąć (nawet jeśli nie jest otwarty w żadnej aplikacji) do momentu zamknięcia okna SpaceDrive.

#### TC-UIUX-02

- **Opis problemu**:

  - Drag & Drop między folderami nie działa poprawnie.
  - **Próba przeniesienia plików między folderami**:
    - Nie można przeciągnąć pliku poza aktualne okno aplikacji.
  - **Próba przeniesienia wielu plików**:
    - Podczas zaznaczenia kilku plików, przenoszony jest tylko pierwszy zaznaczony plik.
  - Pliki nie zostały przeniesione do nowej lokalizacji.

- **Notatki**:
  - Funkcja Drag & Drop pomiędzy folderami i urządzeniami wymaga poprawy.

#### TC-UIUX-03

- **Opis problemu**:
  - Funkcja Drag & Drop z innych aplikacji do SpaceDrive nie działa.
  - Przeciągnięcie pliku z eksploratora systemowego do SpaceDrive kończy się niepowodzeniem — plik nie pojawia się w docelowej lokalizacji.

#### TC-UIUX-04

- **Opis problemu**:
  - Responsywność interfejsu jest ogólnie poprawna, ale po zmniejszeniu szerokości okna niektóre przyciski stają się niewidoczne (np. przycisk zamknięcia okna).
  - Przy minimalnych rozmiarach okno aplikacji jest użyteczne, ale brak widoczności niektórych elementów interfejsu wpływa na doświadczenie użytkownika.

---

### 4.3 Dodatkowe Problemy Wykryte Podczas Testów

Oprócz przypadków testowych zidentyfikowano następujące problemy:

1. **Problemy z usuwaniem folderów po ich przeglądaniu w SpaceDrive**:

   - Folderów przeglądanych w aplikacji nie można usunąć (nawet jeśli nie są otwarte w innej aplikacji) do momentu zamknięcia okna SpaceDrive.

2. **Brak aktualizacji nazw folderów w widoku „Locations”**:

   - Zmiana nazwy folderu w innej aplikacji nie jest automatycznie aktualizowana w SpaceDrive.

3. **Problemy z tagami**:

   - Po utworzeniu nowego tagu dla pliku tag ten automatycznie przypisywany jest do folderu, w którym znajduje się plik.
   - W widoku oznaczeń tagami widoczny jest tylko folder, ale otwarcie folderu w SpaceDrive powoduje otwarcie pliku w aplikacji domyślnej.

4. **Brak informacji o rozmiarze folderów zawierających podfoldery**:
   - SpaceDrive nie pokazuje rozmiaru folderów, które mają zagnieżdżone podfoldery, co utrudnia ocenę zajętości miejsca.

---

## 5. Statystyki testów

![ab066623-c8ff-4b80-86ea-91928f621868](https://github.com/user-attachments/assets/0d4c1e29-8f75-45e6-8378-a6b2ba5412af)
![17df6799-aa44-4dd7-b7f1-a9fc74f96b6e](https://github.com/user-attachments/assets/cd4240e5-a8bf-4235-9e2d-adbee9d86f91)

---

## 6. Podsumowanie

### Wyniki:

- **Liczba testów**: 26
- **Testy pozytywne**: 21
- **Testy negatywne**: 5

---

## 7. Wnioski

Testy aplikacji **Spacedrive** w większości zakończyły się sukcesem, potwierdzając poprawne działanie kluczowych funkcjonalności, takich jak synchronizacja, zarządzanie plikami oraz responsywność interfejsu. Wykryte problemy powinny zostać priorytetowo naprawione, aby poprawić zgodność aplikacji z wymaganiami użytkowników oraz standardami bezpieczeństwa.
