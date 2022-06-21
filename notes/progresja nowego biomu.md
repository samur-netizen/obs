---
share: True
---
# Dystans
*Patrz: [[statystyki biomów#dystans pomiędzy choke pointami]]*
Od biomu 5 zaczynamy wprowadzać distance 4 pomiędzy planszami [[choke point]].

dystans 4 to minimalny dystans pomiędzy choke pointami chociażby dlatego, że bardzo mało można wsadzić pomiędzy.

W biomie 6 dystans 4 będzie tak samo często jak w biomie 5, czyli:
- dystans 4 pojawi się: 6 razy, 
- dystans 5 pojawi się: 5 razy

Różnica będzie w tym że dystans 4 pojawi się wcześniej.

# Inne parametry
Ilość plansz challengowych
- Dotychczas robiliśmy 5 plansz challenge per biome.
- Raczej nie ma sensu robić ich progresji bo tutaj trzeba po prosątu kombinować i ciężko znaleźć połączenia które zadziałają bez prototypowania.

Na początku biomu dajemy zawsze 3x relax
- Patrz: [[biom 6 - początek za trudny]]

## [[progresja nowego biomu]], [[biom podzielony na etapy]]
Dzieląc biom na etapy trzeba odpowiednio zaprojektować progresję, zaznaczając dla każdego etapu [[akcenty progresji]]:
- początek progresji
- koniec progresji

## Very high lenght type
![[very high]]

# tool do analizy progresji wyeksportowanej z Notion to:
Progression Table Stats Module
[link do toola na Google Spreadsheets](https://docs.google.com/spreadsheets/d/1SCSOwzlMMPONOtbNwt_Lf6_zevuQULAf26zijsW-bpY/edit#gid=1916506038])

Importujemy eksport z Notion, ustawiamy jak na screenie: Iclude databases -> Everything
![[CleanShot 2022-06-01 at 14.39.51.png]]

zatępując dane arkuszu RawData mając zaznaczoną komórkę A1. Z opcji importu wybieramy:
- Zastąp dane, zaczynając od zaznaczonej komórki
- Typ separatora: przecinek
- Odznaczamy boks: konwertuj tekst na liczby, itd.
![[CleanShot 2022-06-01 at 14.46.16.png|400]]

Jak zostały dodane nowe kolumny do Tabeli Progresji w Notion to przesunęły się kolumny i trzeba poprawić w Converter, żeby znajdował kolumny odpowiednie do wartości z !DataMap której szuka

- Usuwamy filtr na wszystkich kolumnach i tworzymy go ponownie, żeby znajdywał wszystkie komórki
- Tworzymy filtr i usuwamy wszystko co nas nie interesuje w RawData
- Sortujemy pozostałe plansze
- I voila! W zakładce "Overall stats" będziemy mieli statystyki badanego biomu.

[[statystyki biomów]]

# Feedback i review notes
[[wnioski z analizy funnela (paź 2021)]]
[[Feedback session 31-08-21#progresja nowego biomu]]

# History
[[Design progresji do v 1.6]]

# [[2022-06-14 Tue]]
Fajnie w [[Biom 8]] pojawiają się cages 3hp. Pojawiają się rzadko, a jak już się pojawiają to akcentują charakter planszy.
# [[2022-06-21 Tue]]
W późniejszych biomach plansze [[relax]] to mogą być po prostu plansze z klasycznymi mechanikami, które gracz już bardzo dobrze zna (np. bomb, smok, cages).