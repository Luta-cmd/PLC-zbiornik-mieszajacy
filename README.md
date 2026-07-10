# System sterowania automatycznym zbiornikiem mieszającym (TIA Portal / SCL)

Projekt zaliczeniowy z przedmiotu **Zaawansowane programowanie PLC** — program sterujący procesem technologicznym (dozowanie → mieszanie → spust) napisany w języku SCL (IEC 61131-3), zrealizowany w środowisku Siemens TIA Portal.

## Zakres projektu

Program w kompletny sposób wykorzystuje następujące konstrukcje programistyczne:

- [x] Funkcje logiczne (AND, OR, NOT)
- [x] Funkcje arytmetyczne
- [x] Instrukcje warunkowe (IF, CASE)
- [x] Pętle (FOR)
- [x] Timery (TON)
- [x] Liczniki (CTU, CTD)
- [x] Sterowanie zaworem analogowym (regulacja proporcjonalna)
- [x] Detekcja zboczy sygnałów (R_TRIG, F_TRIG)

## Opis procesu

Zbiornik technologiczny z czujnikiem poziomu analogowym, zaworem dozującym sterowanym analogowo, pompą mieszającą i zaworem spustowym. Proces przebiega jako maszyna stanów:

`IDLE → NAPEŁNIANIE → MIESZANIE → SPUST → ZAKOŃCZONO → (powrót do IDLE)`

Pełny opis działania, schemat regulacji zaworu oraz wyniki testów w symulatorze PLCSIM znajdują się w sprawozdaniu (patrz niżej).

## Struktura repozytorium

```
plc-zbiornik-mieszajacy/
├── plc/
│   ├── FB_ZbiornikMieszajacy.scl      # blok funkcyjny - główna logika procesu
│   └── OB1_Main_wywolanie.scl         # przykładowe wywołanie bloku w OB1 (Main)
├── sprawozdanie/
│   ├── main.tex                       # źródło LaTeX sprawozdania (Overleaf)
│   ├── images/                        # zrzuty ekranu z TIA Portal (kod + testy online)
│   └── sprawozdanie_podglad.pdf       # gotowy, skompilowany PDF sprawozdania
└── README.md
```


## Autor

Maciej Lutyński
