# Bezpieczeństwo i prywatność

---

### TC-SEC-PRIV-01: Weryfikacja uzyskiwania permisji dostępu do plików/folderów
**Cel:** Sprawdzić, czy aplikacja poprawnie pyta użytkownika o udzielenie dostępu do plików lub folderów, jeśli nie ma odpowiednich uprawnień.  
**Powiązane wymaganie:** REQ-FUNC-03  

**Kroki:**
1. Zainstaluj aplikację na nowym urządzeniu lub wyczyść dane aplikacji, aby wymusić brak wcześniejszych uprawnień.
2. Spróbuj otworzyć plik znajdujący się w pamięci urządzenia (np. `Documents/file1.txt`).
3. Spróbuj zapisać nowy plik w folderze z ograniczonym dostępem (np. `ProtectedFolder/`).
4. Odrzuć prośbę o uprawnienia i powtórz kroki 2 i 3.
5. Po odrzuceniu, przejdź do ustawień aplikacji i ręcznie przyznaj brakujące uprawnienia.
6. Spróbuj ponownie wykonać kroki 2 i 3.

**Oczekiwane działanie:**
- Aplikacja wyświetla komunikat o konieczności przyznania uprawnień.
- Użytkownik może przyznać lub odrzucić uprawnienia.
- Po przyznaniu uprawnień dostęp do plików/folderów działa poprawnie.

---

### TC-SEC-PRIV-02: Weryfikacja szyfrowania katalogów hasłem
**Cel:** Sprawdzić, czy użytkownicy mają możliwość szyfrowania i odszyfrowania katalogów hasłem oraz czy aplikacja obsługuje szyfrowane pliki z innych aplikacji.  
**Powiązane wymaganie:** REQ-FUNC-11  

**Kroki:**
1. Utwórz folder `SensitiveData` i dodaj do niego kilka plików (np. `file1.txt`, `file2.jpg`).
2. Użyj funkcji aplikacji do zaszyfrowania folderu hasłem (np. `1234abcd`).
3. Spróbuj otworzyć plik z zaszyfrowanego folderu bez podania hasła.
4. Podaj poprawne hasło i otwórz folder oraz jego pliki.
5. Przetestuj błędne hasło co najmniej 3 razy i sprawdź reakcję aplikacji (np. blokada na pewien czas).
6. Zaimportuj folder zaszyfrowany inną aplikacją i sprawdź jego kompatybilność (np. otwórz folder z hasłem `abcd1234`).
7. Zaszyfruj folder w aplikacji i spróbuj otworzyć go w innej aplikacji kompatybilnej z funkcją szyfrowania.

**Oczekiwane działanie:**
- Aplikacja poprawnie szyfruje foldery i wymaga hasła do ich odszyfrowania.
- Foldery zaszyfrowane innymi aplikacjami są poprawnie obsługiwane, jeśli są kompatybilne.
- Nieprawidłowe hasło wyświetla komunikat o błędzie, a próby są ograniczane.

---

### TC-SEC-PRIV-03: Weryfikacja zgodności z przepisami o ochronie prywatności
**Cel:** Sprawdzić, czy aplikacja jest zgodna z przepisami dotyczącymi ochrony prywatności, takimi jak RODO, oraz czy dane użytkowników są odpowiednio chronione.  
**Powiązane wymaganie:** REQ-NFUNC-04  

**Kroki:**
1. Przejdź do sekcji ustawień prywatności w aplikacji.
2. Sprawdź, czy aplikacja umożliwia użytkownikowi:
   - Wgląd w dane przechowywane na serwerach.
   - Pobranie kopii danych osobowych.
   - Usunięcie danych osobowych z aplikacji/serwerów.
3. Przeanalizuj politykę prywatności aplikacji (link powinien być dostępny w ustawieniach).
4. Spróbuj skorzystać z funkcji „Żądanie usunięcia danych” i sprawdź, czy proces działa zgodnie z opisem.
5. Sprawdź, czy aplikacja wyświetla komunikaty dotyczące zbierania danych w momencie ich gromadzenia.

**Oczekiwane działanie:**
- Aplikacja spełnia wymagania RODO lub innych lokalnych przepisów o ochronie danych.
- Dane osobowe można łatwo pobrać i usunąć zgodnie z polityką prywatności.

---

### TC-SEC-PRIV-04: Weryfikacja minimalizacji danych telemetrycznych
**Cel:** Sprawdzić, czy aplikacja ogranicza zbieranie danych telemetrycznych do minimum oraz umożliwia użytkownikowi wyłączenie zbierania danych.  
**Powiązane wymaganie:** REQ-NFUNC-11  

**Kroki:**
1. Przejdź do sekcji ustawień aplikacji i znajdź opcję dotyczącą zbierania danych telemetrycznych.
2. Sprawdź, czy użytkownik jest informowany o zakresie zbieranych danych (np. w oknie pop-up przy pierwszym uruchomieniu aplikacji).
3. Wyłącz zbieranie danych telemetrycznych.
4. Używaj aplikacji przez 10 minut i monitoruj połączenia sieciowe (np. za pomocą narzędzi takich jak Wireshark).
5. Powtórz krok 4 z włączoną opcją zbierania danych telemetrycznych.
6. Sprawdź, czy aplikacja umożliwia trwałe wyłączenie zbierania danych telemetrycznych po ponownym uruchomieniu.

**Oczekiwane działanie:**
- Aplikacja wyraźnie informuje użytkownika o zakresie i celu zbierania danych telemetrycznych.
- Wyłączenie zbierania danych telemetrycznych skutecznie ogranicza przesyłanie informacji do serwerów.
- Wyłączona opcja pozostaje zapamiętana po ponownym uruchomieniu aplikacji.