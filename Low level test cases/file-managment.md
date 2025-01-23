# Zarządzanie plikami i bibliotekami
---
TC-FILE-MGMT-02: Weryfikacja aktualizacji listy folderów i plików
Cel: Sprawdzić, czy lista folderów i plików jest zawsze aktualna, nie zawiera plików usuniętych oraz wyświetla wszystkie istniejące pliki.
Powiązane wymaganie: REQ-FUNC-02

## Kroki:
1. Stwórz foldery i pliki zagnieżdżone jak poniżej za pomocą spacedrive:
```
|- folder1/folder3/file3
|- folder2/file2
|- file1
```

3. dodaj file3 do tagów
4. dodaj folder3 do lokalizacji na pasku
5. usuń folder1
6. usuń file2 używając innej aplikacji
7. usuń folder2 używając innej aplikacji
8. usuń folder1
9. Sprawdź czy wszystko jest poprawnie usunięte

Zrób to samo dla przenieś do kosza

## Oczekiwanie działanie:
Wszystkie tworzą się porawnie i po usunięciu pliki są nie widoczne

---

### TC-FILE-MGMT-03: Weryfikacja funkcji wyszukiwania i filtrowania plików  
**Cel:** Sprawdzić, czy użytkownicy mogą wyszukiwać i filtrować pliki według typu, daty oraz rozmiaru, a także sortować wyniki w kolejności rosnącej i malejącej dla wszystkich kategorii.  
**Powiązane wymaganie:** REQ-FUNC-05  



## Kroki:  

1. **Przygotowanie plików:**  
   Stwórz strukturę plików i folderów za pomocą aplikacji:  
   ```
   |- folder1/file1.txt (1 KB, utworzony: 2025-01-01)  
   |- folder1/file2.pdf (5 MB, utworzony: 2025-01-05)  
   |- folder2/file3.jpg (15 MB, utworzony: 2025-01-10)  
   |- folder2/file4.docx (3 MB, utworzony: 2025-01-15)  
   ```

2. **Test wyszukiwania:**  
   - Wyszukaj „file1” w wyszukiwarce.  
   - Wyszukaj „file” i sprawdź, czy zwracane są wszystkie pliki.  
   - Wyszukaj ciąg, który nie występuje w nazwach plików (np. „test”) i sprawdź komunikat „Brak wyników”.  

3. **Filtrowanie według typu:**  
   - Filtruj pliki, wybierając typ „.pdf”.  
   - Powtórz dla każdego dostępnego typu (np. „.txt”, „.jpg”, „.docx”).  

4. **Filtrowanie według daty:**  
   - Ustaw filtr dat od „2025-01-01” do „2025-01-10” i sprawdź wyniki.  
   - Powtórz dla zakresu „2025-01-10” do „2025-01-15”.  

5. **Filtrowanie według rozmiaru:**  
   - Filtruj pliki o rozmiarze < 1 MB.  
   - Powtórz dla zakresów 1-10 MB i > 10 MB.  

6. **Sortowanie wyników:**  
   - Wyszukaj dowolny zestaw plików i:  
     - Posortuj wyniki według typu pliku (rosnąco i malejąco).  
     - Posortuj wyniki według daty (rosnąco i malejąco).  
     - Posortuj wyniki według rozmiaru (rosnąco i malejąco).  

7. **Kombinacja wyszukiwania i filtrowania:**  
   - Wyszukaj „file” i zastosuj filtr typu „.jpg”.  
   - Sortuj wyniki według daty utworzenia (rosnąco).  
   - Zweryfikuj, czy wszystkie warunki są spełnione.  



## Oczekiwane działanie:  
1. **Wyszukiwanie:**  
   - Pliki zgodne z zapytaniem są wyświetlane poprawnie.  
   - Dla zapytań bez wyników pojawia się komunikat „Brak wyników”.  

2. **Filtrowanie:**  
   - Pliki są poprawnie ograniczane do wybranego typu, daty lub rozmiaru.  

3. **Sortowanie:**  
   - Wyniki są poprawnie sortowane w kolejności rosnącej i malejącej dla każdej kategorii.  

4. **Kombinacja funkcji:**  
   - Wszystkie kombinacje wyszukiwania, filtrowania i sortowania działają poprawnie i zwracają odpowiednie wyniki.  
---


### TC-FILE-MGMT-04: Weryfikacja funkcji ulubionych plików  
**Cel:** Sprawdzić, czy użytkownik może dodawać pliki do listy ulubionych i czy aplikacja poprawnie wyświetla tę listę.  
**Powiązane wymaganie:** REQ-FUNC-13  

---

## Kroki:  

1. **Przygotowanie plików:**  
   Utwórz poniższą strukturę plików:  
   ```
   |- folder1/file1.txt  
   |- folder1/file2.pdf  
   |- folder2/file3.jpg  
   |- folder2/file4.docx  
   ```

2. **Dodawanie plików do ulubionych:**  
   - Dodaj „file1.txt” i „file3.jpg” do listy ulubionych.  
   - Sprawdź, czy pliki są widoczne na liście ulubionych.  

3. **Usuwanie plików z ulubionych:**  
   - Usuń „file1.txt” z ulubionych.  
   - Sprawdź, czy plik został usunięty z listy ulubionych, ale pozostaje widoczny w głównej strukturze plików.  

4. **Dodanie plików spoza ulubionych:**  
   - Dodaj „file4.docx” do ulubionych.  
   - Zweryfikuj, czy pojawił się na liście ulubionych.  

5. **Weryfikacja stanu listy ulubionych:**  
   - Zaktualizuj widok aplikacji (np. przez odświeżenie) i sprawdź, czy lista ulubionych pozostaje poprawna.  
   - Sprawdź, czy lista ulubionych zachowuje się poprawnie po ponownym uruchomieniu aplikacji.  

---

## Oczekiwane działanie:  
1. Pliki poprawnie dodają się do listy ulubionych.  
2. Usunięcie plików z ulubionych nie powoduje ich usunięcia z głównej struktury plików.  
3. Lista ulubionych jest aktualizowana w czasie rzeczywistym i zapamiętywana po ponownym uruchomieniu aplikacji.  


