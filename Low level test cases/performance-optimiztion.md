# Wydajność i optymalizacja

---

### TC-PER-01: Weryfikacja czy pliki systemowe są wykluczane przy wyszukiwaniu.

**Cel:** Sprawdzić, czy aplikacja przy wyszukiwaniu ignoruje pliki i foldery systemowe.  
**Powiązane wymaganie:** REQ-FUNC-06
**Warunki wstępne:**

- Zainstalowana aplikacja SpaceDrive

  **Kroki:**

1. Otwórzcie folder `Windows` w defoltowym file exporeru.
2. Stwórzcie listę 10 plików systemowych (nie aplikacji systemowych).
3. Otwórzcie SpaceDrive i sprobójcie w wysukiwarce zanleść pliki z listy.

   **Oczekiwane wyniki:**

- Żaden plik nie ma być znaleziony.

---

# TC-PER-02: Weryfikacja czasu odpowiedzi aplikacji

**Cel:** Sprawdzić, czy aplikacja ma krótszy czas odpowiedzi niż 2 sekundy przy dostępie do plików.

**Warunki wstępne:**
- Katalog zawiera co najmniej 1000 plików różnego typu, w tym co najmniej 100 obrazów > 1 MB.

**Kroki:**
1. Otwórz katalog zawierający 1000 plików.
2. Wprowadź nazwę istniejącego pliku w module wyszukiwania.
3. Uruchom wyszukiwanie.
4. Mierz czas odpowiedzi od momentu uruchomienia wyszukiwania do wyświetlenia wyników. (ma być < 2s)

**Oczekiwane wyniki:**
- Czas odpowiedzi aplikacji nie przekracza 2 sekund.

---
# TC-PER-03: Weryfikacja czasu generowania miniatur

**Cel:** Sprawdzić, czy aplikacja generuje miniatury dla różnych typów plików (np. obrazów, dokumentów) w czasie nieprzekraczającym 3 sekund.

**Warunki wstępne:**
- Katalog zawiera pliki w różnych formatach (takich jak: .py, .jpg, .png, .pdf, .svg).

**Kroki:**
1. Otwórz katalog zawierający różne typy plików co najmniej 10 w każdym formacie w tym co najmniej 20 obrazów > 2 MB.
2. Zmierz czas od wejścia w katalog do pojawienia się wszystkich miniaturek, scrollując w dół. (ma być < 3s)

**Oczekiwane wyniki:**
- Miniatury dla wszystkich plików są wygenerowane w czasie nieprzekraczającym 3 sekund.

---

# TC-PER-04: Weryfikacja czasu interakcji

**Cel:** Sprawdzić, czy aplikacja jest responsywna i czy wszystkie interakcje użytkownika (np. przeglądanie plików, nawigacja) odbywają się bez zauważalnych opóźnień, nieprzekraczających 200 ms.

**Warunki wstępne:**
- Katalog zawiera co najmniej 500 plików.

**Kroki:**
1. Otwórz katalog zawierający 500 plików.
2. Przejdź do dowolnego podkatalogu.
3. Kliknij na plik w celu jego podglądu.
4. Zmierz czas odpowiedzi dla każdej interakcji.

**Oczekiwane wyniki:**
- Czas odpowiedzi dla każdej pojedynczej interakcji: otwarcie katalogu, przejście do podkatalogu, podgląd pliku nie przekracza 200 ms (tylko dla domyślnych aplikacji, gdzie otwarcie standardowo pliku nie przekracza 200ms).
