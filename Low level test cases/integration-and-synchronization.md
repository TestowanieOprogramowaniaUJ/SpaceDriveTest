Integracja i synchronizacja
---

### TC-INTEG-SYNC-01: Weryfikacja synchronizacji plików między urządzeniami
Cel: Sprawdzić, czy aplikacja poprawnie synchronizuje pliki między urządzeniami i czy zmiany wprowadzone na jednym urządzeniu są widoczne na pozostałych.
Powiązane wymaganie: REQ-FUNC-09
### Wymagania wstępne:
- na jednym urządzeniu są 4 pliki:
	- plik systemowy (np. dotfiles)
	- plik pusty z długą nazwą
	- plik pełny min: 100MB
	- zdjęcie 3 MB
### Kroki:
1. połącz urządzenia
2. prześlij pliki między urządzeniami
3. sprawdź czy wszystkie pliki oprócz plików systemowych znajdują się na innych urządzeniach
4. zrób to samo, ale teraz sprawdź czy nie nadpisuje plików o tych samych nazwach na innych urządzeniach

### Oczekiwane wyniki:
- na wszystkich urządzeniach są te same pliki (oprócz systemowych)
- nie nadpisuje plików
