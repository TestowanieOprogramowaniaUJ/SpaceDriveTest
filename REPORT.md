# Raport z Testów Aplikacji Spacedrive

## 1. Wprowadzenie
Testy aplikacji **Spacedrive** miały na celu weryfikację funkcjonalności, wydajności, kompatybilności oraz zgodności z wymaganiami bezpieczeństwa. Testy obejmowały zarówno przypadki wysokopoziomowe (**High-Level Test Cases**), jak i szczegółowe przypadki niskopoziomowe (**Low-Level Test Cases**).

---

## 2. Zakres Testów
Przeprowadzone testy objęły następujące obszary:
- **Zarządzanie plikami**: kopiowanie, przenoszenie, zmiana nazw, tworzenie folderów.
- **Synchronizacja i integracja**: transfer danych między urządzeniami, synchronizacja w czasie rzeczywistym, integracja z usługami chmurowymi.
- **Wydajność**: czas odpowiedzi aplikacji, generowanie miniatur, responsywność interfejsu.
- **Bezpieczeństwo**: uzyskiwanie uprawnień dostępu do plików, szyfrowanie folderów, minimalizacja danych telemetrycznych.

---

## 3. Wyniki Testów
### 3.1 Przypadki Testowe

#### Zarządzanie plikami
| ID Testu              | Wynik        |
|-----------------------|-------------|
| TC-FILE-MGMT-01       | ✅ Pozytywny |
| TC-FILE-MGMT-02       | ✅ Pozytywny |
| TC-FILE-MGMT-03       | ✅ Pozytywny |
| TC-FILE-MGMT-04       | ✅ Pozytywny |
| TC-FILE-MGMT-05       | ✅ Pozytywny |
| TC-FILE-MGMT-06       | ✅ Pozytywny |

#### Integracja i synchronizacja
| ID Testu              | Wynik        |
|-----------------------|-------------|
| TC-INTEG-SYNC-01      | ✅ Pozytywny |
| TC-INTEG-SYNC-02      | ✅ Pozytywny |
| TC-INTEG-SYNC-03      | ✅ Pozytywny |
| TC-INTEG-SYNC-04      | ✅ Pozytywny |
| TC-INTEG-SYNC-05      | ✅ Pozytywny |
| TC-INTEG-SYNC-06      | ✅ Pozytywny |
| TC-INTEG-SYNC-07      | ✅ Pozytywny |

#### Wydajność i optymalizacja
| ID Testu              | Wynik        |
|-----------------------|-------------|
| TC-PER-01             | ✅ Pozytywny |
| TC-PER-02             | ✅ Pozytywny |
| TC-PER-03             | ✅ Pozytywny |
| TC-PER-04             | ✅ Pozytywny |

#### Bezpieczeństwo i prywatność
| ID Testu              | Wynik        |
|-----------------------|-------------|
| TC-SEC-PRIV-01        | ❌ Negatywny |
| TC-SEC-PRIV-02        | ✅ Pozytywny |
| TC-SEC-PRIV-03        | ✅ Pozytywny |
| TC-SEC-PRIV-04        | ✅ Pozytywny |

#### Interfejs użytkownika i UX
| ID Testu              | Wynik        |
|-----------------------|-------------|
| TC-UIUX-01            | ✅ Pozytywny |
| TC-UIUX-02            | ✅ Pozytywny |
| TC-UIUX-03            | ✅ Pozytywny |
| TC-UIUX-04            | ✅ Pozytywny |
| TC-UIUX-05            | ✅ Pozytywny |

---

### 3.2 Dodatkowe Problemy Wykryte Podczas Testów
Oprócz przypadków testowych zidentyfikowano następujące problemy:
1. **Brak uzyskiwania uprawnień dostępu do plików/folderów**:  
   - Aplikacja nie prosi użytkownika o uprawnienia dostępu, a także nie informuje o ich braku, co może powodować trudności przy przeglądaniu folderów.
   - Przykład: Dla folderów bez uprawnień, aplikacja nie informuje użytkownika o braku dostępu.
   
2. **Problemy z usuwaniem folderów po ich przeglądaniu w SpaceDrive**:  
   - Folderów przeglądanych w aplikacji nie można usunąć (nawet jeśli nie są otwarte w innej aplikacji) do momentu zamknięcia okna SpaceDrive.

3. **Brak aktualizacji nazw folderów w widoku „Locations”**:  
   - Zmiana nazwy folderu w innej aplikacji nie jest automatycznie aktualizowana w SpaceDrive.

4. **Problemy z tagami**:  
   - Po utworzeniu nowego tagu dla pliku tag ten automatycznie przypisywany jest do folderu, w którym znajduje się plik.  
   - W widoku oznaczeń tagami widoczny jest tylko folder, ale otwarcie folderu w SpaceDrive powoduje otwarcie pliku w aplikacji domyślnej.

5. **Brak informacji o rozmiarze folderów zawierających podfoldery**:  
   - SpaceDrive nie pokazuje rozmiaru folderów, które mają zagnieżdżone podfoldery, co utrudnia ocenę zajętości miejsca.

---

## 4. Podsumowanie
### Wyniki:
- **Liczba testów**: 27  
- **Testy pozytywne**: 26  
- **Testy negatywne**: 1  

### Krytyczne problemy:
- **TC-SEC-PRIV-01**: Brak uzyskiwania uprawnień dostępu do plików.
- Dodatkowe błędy związane z zarządzaniem folderami, tagami i informacjami o rozmiarze folderów.

---

## 5. Wnioski
Testy aplikacji **Spacedrive** w większości zakończyły się sukcesem, potwierdzając poprawne działanie kluczowych funkcjonalności, takich jak synchronizacja, zarządzanie plikami oraz responsywność interfejsu. Wykryte problemy powinny zostać priorytetowo naprawione, aby poprawić zgodność aplikacji z wymaganiami użytkowników oraz standardami bezpieczeństwa.

