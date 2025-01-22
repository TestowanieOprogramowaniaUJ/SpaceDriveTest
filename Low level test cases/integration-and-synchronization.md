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

---

### TC-INTEG-SYNC-02: Weryfikacja czasu opóźnienia synchronizacji

**Cel:** Sprawdzić, jaki jest czas opóźnienia synchronizacjii plików między urządzeniami.  
**Powiązane wymaganie:** REQ-FUNC-09

### Wymagania wstępne:

1. Zainstalowany spacedrive na dwóch róznych urządzenaich
2. Sekundomierz
3. Plik o rozmiarze > 100 MB

### Kroki :

1. Popołącz urządzenia
2. Przygotuj sekundomierz
3. Stwórz nowy pusty plik tekstowy 1.txt i naciśnij start na sekundomierze
4. Po pojawieniu nowego pliku testowego na drugim urządzeniu naciśnij stop.
5. Powtórz kroki 2-4 dla pliku o rozmiarze większym niż 100mb;

### Oczekiwane wyniki:

- Pliki są dostępne na drugim urządzeniu
- Informacja o pliku na drugim urządzeniu pojawia się w ciągu 30 sekund.

---

### TC-INTEG-SYNC-03: Weryfikacja integracji kont chmurowych

Cel: Sprawdzić, czy aplikacja umożliwia poprawne logowanie do usług chmurowych i zarządzanie plikami.  
**Powiązane wymaganie:** REQ-FUNC-10

### Wymagania wstępne:

1. Zainstalowany spacedrive
2. Konto google z plikami na google drive

### Kroki :

1. Połąć spacedrive z servisem chmurowym Google Drive.
2. Sprawdź czy wszystkie pliki i foldery są widoczne.
3. Spróbuj otworzyć jeden plik.

### Oczekiwane wyniki:

- Spacedrive pomyślne połaczony z Google Drive.
- Zawartość dyska i plików widoczna w SpaceDrive odpowiada rzeciwistości.
- Plik otwierany poprawnie.

---

### TC-INTEG-SYNC-04: Weryfikacja przesyłania plików za pomocą Spacedrop

**Cel:** Sprawdzić, czy użytkownicy mogą przesyłać pliki między urządzeniami przy użyciu funkcji Spacedrop.  
**Powiązane wymaganie:** REQ-FUNC-12

### Wymagania wstępne:

1. Zainstalowany spacedrive na dwóch róznych urządzenaich
2. Plik o rozmiarze > 100 MB

### Kroki :

1. Popołącz urządzenia
2. Prześlij plik na drugie urządzenia używając space dropa
3. Sprawdź zawartość pliku na drugim urządzeniu.

### Oczekiwane wyniki:

- Plik został presłany i ma tą samą zawartość.

---

### TC-INTEG-SYNC-05: Weryfikacja integralności danych podczas transferu
**Cel:** Sprawdzić, czy dane przesyłane między urządzeniami są poprawnie przesyłane bez uszkodzeń.  
**Powiązane wymaganie:** REQ-NFUNC-03

### Wymagania wstępne:
- plik o rozmiarze > 100 MB.
- katalog z 20 plikami o małym rozmiarze

### Kroki:
1. Połącz urządzenia
2. prześlij pliki między urządzeniami (w 2. strony)
3. zmień nazwę i prześlij pliki na jedno urządzenie za pomocą innego transferu (np.google drive)
4. sprawdź czy pliki są identyczne
### Oczekiwane wyniki:
- pliki ze wszystkich urządzeń są identyczne

---

### TC-INTEG-SYNC-06: Weryfikacja spójności danych podczas synchronizacji

**Cel:** Sprawdzić, czy synchronizacja plików między urządzeniami zachowuje spójność wersji.  
**Powiązane wymaganie:** REQ-NFUNC-09

### Wymagania wstępne:

1. Zainstalowany spacedrive na dwóch róznych urządzenaich
2. Plik tekstowy

### Kroki:

1. Połącz urządzenia
2. Zmodyfikuj plik tekstowy
3. Zaczekaj 10-20 sekund
4. Sprawdź czy pliki są identyczne

### Oczekiwane wyniki:

- pliki ze wszystkich urządzeń są identyczne
