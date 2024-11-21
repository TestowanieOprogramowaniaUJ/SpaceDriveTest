# README dla repozytorium planu testów aplikacji Spacedrive

## Opis
Repozytorium zawiera **Plan Testów aplikacji Spacedrive**, narzędzia służącego do zarządzania plikami i danymi na wielu urządzeniach i platformach. Plan testów definiuje podejście, zakres i metodologię stosowaną do walidacji funkcjonalności, wydajności i kompatybilności aplikacji.

## Zawartość repozytorium
- **`PLAN_TESTOW.md`**: Pełna dokumentacja planu testów, opisująca proces testowania, elementy testowe, kryteria oraz wyniki.  
- **`przypadki_testowe/`**: Folder zawierający szczegółowe przypadki testowe dla różnych funkcji.  
- **`logi/`**: Logi z wykonania testów oraz raporty wydajnościowe.  
- **`raporty/`**: Podsumowania wyników testów i zidentyfikowanych problemów.  

## Cele testów
Główne cele procesu testowania:  
1. Walidacja kluczowych funkcjonalności, takich jak transfer plików, synchronizacja i aktualizacje w czasie rzeczywistym.  
2. Weryfikacja kompatybilności na różnych systemach operacyjnych (Windows, macOS, Linux).  
3. Ocena wydajności, w tym zużycia CPU i pamięci RAM w trakcie obciążenia.  

## Kluczowe funkcje do przetestowania
- Zarządzanie plikami za pomocą funkcji drag & drop.  
- Aktualizowanie struktury plików i folderów w czasie rzeczywistym.  
- Synchronizacja danych między różnymi urządzeniami.  
- Wykluczanie plików systemowych z wyników wyszukiwania.  

## Narzędzia i środowisko
- **Systemy operacyjne**: Windows 10/11, macOS Ventura, Ubuntu 22.04.  
- **Sprzęt**: Komputer z procesorem Intel i5/AMD Ryzen 5, 8 GB RAM, dyskiem SSD.  
- **Aplikacja**: Spacedrive (wersja najnowsza, pobrana z repozytorium GitHub).  

## Harmonogram
- **Listopad (tydzień 1–2)**: Przygotowanie przypadków testowych.  
- **Listopad (tydzień 3–4)**: Testy funkcjonalne.  
- **Grudzień (tydzień 1)**: Testy wydajnościowe.  
- **Grudzień (tydzień 2)**: Testy kompatybilności.  
- **Grudzień (tydzień 3)**: Analiza wyników i tworzenie raportów.  

## Repozytorium GitHub
Aplikacja Spacedrive jest dostępna pod adresem:  
[Spacedrive GitHub](https://github.com/spacedriveapp/spacedrive)  
