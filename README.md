# System Parkingowy z Automatycznym Naliczaniem Opłat

## Opis projektu
System parkingowy wykorzystujący Raspberry Pi 5, kamerę Raspberry oraz serwomechanizm do automatycznego naliczania opłat na podstawie zczytanych numerów tablic rejestracyjnych.

## Wymagania sprzętowe
- **Raspberry Pi 5**
- **Kamera do Raspberry Pi**
- **Servo motor**
- **Czujnik przerwania wiązki**
- **Guzik**

## Funkcjonalności

### **Wjazd**
1. Kamera skanuje tablicę rejestracyjną pojazdu i weryfikuje jej poprawność.
2. Tablica rejestracyjna zostaje dodana do bazy danych wraz z czasem wjazdu.
3. Serwomechanizm podnosi szlaban, umożliwiając wjazd na parking.
4. Jeśli czujnik przerwania wiązki nic nie rejestruje to zamyka się szlaban

### **Wyjazd**
1. Kamera skanuje tablicę rejestracyjną pojazdu i weryfikuje jej poprawność.
2. System sprawdza tablicę w bazie danych.
3. Na podstawie różnicy czasu wjazdu i wyjazdu obliczana jest opłata zgodnie z ustalonym cennikiem.
4. Po opłaceniu należności serwomechanizm podnosi szlaban, umożliwiając wyjazd.
5. Jeśli czujnik przerwania wiązki nic nie rejestruje to zamyka się szlaban


## Struktura bazy danych
Baza danych powinna zawierać następujące pola:
- **Numer tablicy rejestracyjnej**
- **Czas wjazdu**
