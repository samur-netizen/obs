---
share: true
---
## Intencja :fas_star:
- Pomóc Pawłowi w rozwoju tego toola
- Chce się zaangażować jak najbardziej w jego rozwój, bo to jest tool:
	- który ma nam służyc do szybszego tworzenia plansz
	- który ma być dla nas, to my będziemy na codzień z niego korzystać
- Myślę, że jest jeszcze potencjał w automatyzacji tworzenia plansz, który warto wykorzystać i sens tego toola opiera się na tym założeniu

# [[2022-06-20 Mon]]
## Review pierwsze
### Konfigi
- Dobrze by było żeby konfigi z presetami były w jednym zbiorczym katalogu - presets
- Jak dodać color preset? W Level Generator (LG) nie pojawia się
- Bullets Presets:
	- O co chodzi z Number sequence w konfigu presetów bulletów?
	- Po co w ogóle są Bullet Configi? Bo mamy naprawdę sporą rozbieżność i to się stanie ten sam problem co z konfigami dla objectivów:
		- Będziemy mieli ich mnóstwo
		- Różniące się tylko parametrem ilości
		- Będzie problem z nazewnictwem tych konfigów
- Po co się podaje konfig objectiva? To jest ten sam case co powyżej z Bullet presetem - to powinno być z automatu na podstawie procentów jakie ustawia designer.
- Procenty block type powinny być liczone dla wszystkich mechanik dodanych (do 100%) i przeliczane automatycznie - tak jak to działa jak ustawiamy szansę dla transforma:
	- ![[CleanShot 2022-06-20 at 20.21.15.png]]
### Ustawianie ilości rzeczy
- Ustawianie bulletów z góry jest praktycznie niemożliwe. To powinno się przeliczać z automatu.
	- Ewentualnie możemy min/maks ustawiać, ale nie konkretną wartość, bo tego po prostu nie wiemy dopóki nie zagramy w tę planszę i tego nie ocenimy.
- Ustawiłem SwapColor na 30% a generuje ich bardzo dużo nadal. Nie wiem czy to co generuje to 30%?
	- ![[CleanShot 2022-06-20 at 20.36.27.png|200]]

> [!Idea] Powinny być makse procentowe mechanik per mechanika
> Dla przykładu:
> - Flytrap w swoim konfigu miałby ustawione, że jego 100% to 15% wszystkich klocków na wieży
> - W takim wypadku ustawiając w generatorze per level generation Flytrap na 50% ustawilibyśmy na 7.5%

> [!Idea] Procenty mechanik na dole / środku / u góry wieży
> Przydałoby się też w ustawianiu procentów mechanik żeby móc ustawić jaki chcemy mieć offset tej ilości na górze wieży, ile na dole wieży. Chodzi o to, żeby móc powiedzieć generatorowi: a na dole to wygeneruj mi dwa razy mniej tego typu albo w ogóle. To daje dużo możliwości dodatkowych imo.

> [!Idea] Określanie odstępów, clusterów dla danej mechaniki
> Można to też określać per charakter planszy - dla relaxa np. odstępy flytrapów od siebie są dużo większe niż dla plansz o charakterze choke point.

> [!Question] Nie wiem czy nie powinniśmy zrezygnować z procentów na rzecz ustawiania stepów tak jak to ustawiamy w Level Editorze
> - W stepach od razu zawarty jest dystans mechanik od siebie. To jest mega plus tego rozwiązania
> - ![[CleanShot 2022-06-20 at 21.21.33@2x.png]]
> 
### Wygenerowane plansze
- Problem z niepasującymi chunkami:
	- ![[CleanShot 2022-06-20 at 19.43.06.png|200]]

> [!Hint] Generują się fajne połączenia shapes
> Wygląda na to, że tworzenie nawet samych shapes z generatora może dodać różnorodności do gry.
- Generator objectives ustawia na scenie klony i wypakowuje prefaby. Ogólnie z tym jak mają być ustawiane objectives wolałbym popracować. Najlepiej żeby to nie było z konfiga tylko ustawiane za każdym razem przez designera, tylko step ilości dać co 5, ewentualnie jakieś presety per objective?
### Wybieranie plansz
> [!Idea] Ułatwić proces wybierania plansz
> Teraz trzeba to robić ręcznie:
> - Jeśli plansza się podoba to trzeba ją przenieść do jakiegoś tymczasowego folderu
> - Pewnie trzeba też jej zmienić nazwę
> > [!Hint] W otworzonej planszy z generatora byłby na interfejsie unity button [PICK] z ewentualnym boksem na tagi/nazwę
> > ![[CleanShot 2022-06-20 at 19.53.36.png]]
> > 
> > Z tym też jest problem, bo generator nadpisuje już wygenerowane plansze.
> 

> [!Idea] Może automatycznie powinien nazywać pliki z daty i godziny?
> Bo ciężko się połapać które to są nowe. Albo powinna być do tego dedykowana przeglądarka.
### Ważne dla komfortu pracy
> [!Warning] Okienko generatora powinno się dokować!

> [!Warning] Okienko się nie przewija!
> Na mniejszym monitorze nie da się już kliknąć generate:
> 	![[CleanShot 2022-06-20 at 20.23.39@2x.png]]
### Brakujące rzeczy
- Nie da się określić charakteru planszy!!! Przez co nie możemy wygenerować np. plansz relax.
### Bugi i dziwne zachowania
- Z jakiegoś powodu czasami generator widzi tylko 5 chunków z których może generować. Dopiero danie refresh to naprawia (widzi 66)
> [!Bug] Choose bullet się resetuje samoczynnie










