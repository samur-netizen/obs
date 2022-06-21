---
share: true
---

> [!INFO]+
> groups: [[notes]] | [[topic notes]]
> context: [[c: general]]
> tags: 

# Pierwsze i trochę późniejsze wrażenia
- Michał ją inaczej zaimplementował niż myślałem, ale taka prostota fajnie działa.
	- Ja myślałem, że nie da się matchować klocków normalnych z klockami lewitującymi (w chmurze).
		- [[Matchowanie klocków lewitujących z normalnymi fajnie działa]]
- Jest to jasne i intuicyjne od razu. Wiadomo z tego jak działa core, że te klocki lewitujące blokują klocki normalne.
- Tworzą się fajne, nowe konstrukty na wieży.
- Bardzo zmieniają rozgrywkę - "hmm jak w to teraz grać?"

# Issues i pomysły na rozwój
## Pojedyncze wiszące klocki lewitujące nie są fajne
![[Pojedyncze wiszące klocki lewitujące nie są fajne]]


## W [[LD]] lepiej nie zapełniać nimi całego segmentu wieży
- To podobna specyfika jak z [[indestrucdible blocks]]

## Może klocki lewitujące powinny się inaczej matchować?
- Może matchowane wybuchają niszcząc klocki obok siebie?
# Klocki lewitujące wybuchają
## Pierwsze wrażenia
- Bardzo fajne! :D 

## Issues i pomysły
- Fajnie jak wybuch pojedynczego klocka rozwali chociaż jeden klocek obok. Jeszcze fajniej jak zmatchuje więcej jak jeden, bo wtedy efekty tego wybuchu się chainują.
> [! Problem]+
> Nie jest fajne jak pojedynczy klocek wybuchnie i nie zniszczy swojego sąsiada.

- Może wybuch nie powinien być na radiusie?
> [! Nie widać co się dzieje]
> Nie widać zasięgu wybuchu po samym wybuchu.
> 
![[CleanShot 2022-05-20 at 16.10.33.gif]]

[[2022-05-20]]
## Mechanika wybuchu: infekowanie sąsiada
- Trafiony klocek jest rozwalany i wybiera predefiniowany maks bezpośrednio przyległych sąsiadów
- Wybrani sąsiedzi zaznaczani są jakimś efektem (jako placeholder na chwilę pojawia się na nich X)
- Dopiero po tym jak te klocki zostaną zaznaczone X (delay, tak jak to zrobiłeś z ability) to zaczynają w losowej kolejności wybuchać
- Chodzi o to, żeby osiągnąć tą etapowość wybuchu (tak jak mamy w ability), że pierw klocki do wybuchu są oznaczane, a dopiero potem po chwili wybuchają w fajny sposób.

[[2022-05-23]]
### Ustawianie efektu infekowania - pierwsza implementacja
#### Issues
- Nie działa to tak jak myślałem. Widzę kilka rzeczy do zmiany:
	- Nie wiem czy wybieranie zainfekowanych na radiusie to najlepszy pomysł w tym wypadku. Nie możemy brać przyległych klocków i z nich wybierać?
		- Bo przez to czasami wybiera klocki odległe, a nawet jakimś cudem po innej stronie wieży (może to bug?)
		- [!] Patrz co się dzieje z ostatnim szarym klockiem![[CleanShot 2022-05-23 at 20.53.31.gif]]
	- Czasami te zainfekowane bardzo szybko znikają, nawet na wieży bez innych mechanik.
		- Wydaje mi się, że to jest związane z:
>[!PROBLEM]+ Zainfekowane mogą szybciej być zniszczone jako efekt innej mechaniki
> Zainfekowane zanim wybuchną mogą wybuchnąć zmatchowane przez inne klocki albo jak efekt innej mechaniki
> Odpowiedzią na ten problem jest: [[#Lewitujący klocek w który strzelę nie powinien od razu się rozwalać]]
# Lewitujący klocek w który strzelę nie powinien od razu się rozwalać
- Trafiony lewitujący klocek odpala efekt zainfekowania swoich sąsiadów
- Ten klocek sam staje się zainfekowany i jest niszczony dopiero wraz z niszczeniem innych zainfekowanych klocków

#### PArametry
- levitatingBlockDestoryTimeSpace - jeżeli zniszczymy mi kilka lewitujących np. przez kolor macz to jest deley co ile będę wybuchać
- delayPerSelection to jest niszczenie wybranych sąsiadów

[[2022-05-24]]
Wstrzymujemy prace nad [[Levitating blocks]] na rzecz [[Flytrap]].

[[2022-06-01]]
> [! IDEA] Rozwalony levitating block uwalnia energię która niszczy klocki w linii
>Rozwalenie levitating uwalnia z niego energię która rozwala wszystkie klocki w linii. Linią, jej kierunek mógłby określać linia matcha. Po prostu kierunek energii byłby kontynuację tego metcha, tej linii, tego ciągu 
