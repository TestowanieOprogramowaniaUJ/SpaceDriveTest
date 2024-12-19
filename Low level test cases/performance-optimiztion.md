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
