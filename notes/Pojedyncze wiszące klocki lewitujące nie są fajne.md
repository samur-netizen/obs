---
share: True
---
???+ INFO
	groups: [[notes]] | [[topic notes]]
	context: [[c: general]]
	tags: 

# Issues
???+ NOTE ""
	Gracz jest zmuszany do ich rozwalania i często musi rozwalać pojedyncze klocki

## Przyciągać lewitujące klocki do siebie
- [!]  
![[CleanShot 2022-05-19 at 19.35.17.png]]

- [x] Klocki lewitujące, które nie mają sąsiadów w ustalonym radiusie powinny być przyciągane przez najbliższe klocki. **todo**{: #todo .hash} ✅ 2022-05-23
	- Pytanie które można przyciągać?
		- Całkiem puste? Tylko, że jest jeszcze częsty problem ze strukturą: lewitujący z jednym klockiem regularnym na nim.
		- Może przyciąganie tylko pustych starczy.
		- ![[CleanShot 2022-05-19 at 20.14.27.png]]
		- Przyciąganie w tej sytuacji nic nie da... Bo większy potencjał że coś z tych klocków lewitujących się zmatchuje jest na dole, poza tym wtedy też mogą spaść łatwo.

## Rozwalać te klocki samoczynnie jak będą za wysoko
- [!] Tak to działa w [[side towers]] i nie jest to intuicyjne...

## Klocki nie stykające się z innymi opadają
- [?] Może to będzie łatwiejsza, wyraźniejsza zależność do pokazania?
- [ ] Klocki lewitujące, które nie mają sąsiadów w ustalonym radiusie powinny opadać

## Klocki które mają pod sobą pustkę albo tylko klocki lewitujące powinny powoli opadać

![[CleanShot 2022-05-19 at 20.05.41.png]]

- [ ] Klocki lewitujące, które nie stoją na żadnych klockach powinny opadać 
	- To sprawia, że klocki znajdujące się na nich też opadają.