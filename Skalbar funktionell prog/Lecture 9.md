gå igenom kod

yserra random uses randomness with seed
- använd inte rand-int som förit kan ge hidden-state

dont want 2 atoms we will have intermediate states - dont want

**pairprogramming i början sen dela upp mer**
- också vad är progsam kommande dagarna


koden ska verkligen spegla hur saker händer
- inte bara massa kod utan ska vara väldigt modulärt med bra funktion namn som säger exakt vad som ska göras

deathrattle-loot-hoarder - **låt va ba**
- reusable entity is draw-card
- redo into def-test-test-loothoarder
- vad ska vi göra istället?
- owner-id ska ändras till player-id eller något
- Ha funktion som säger get player-id of owner eller något


create-minion
- cond maybe shouldnt be cond as minions might have more abilities - ex if have taunt and stealth


deftest testing-deathrattle
- gör en sån?
- gör en sån för loot-hoarder?


Hero kanske har armour... Tänk på detta också


sprint 3:
- spel för att kunna ge deathrattle till en minion
- Abusive sergent - kan välja BARA THIS TURN att ge attack
	- if no minion then no dmg
- Kill COmmand är beast ska finnas on board
- På secret ska vi ha som egen :secret på hero? typ om secret är active
- Ragnaros cant attack. must handle valid attacks - how to describe this in data
	- MEN DETTA ÄR INTE ATTACK, SÅ SECRET SOM SÄGER IF HERO ATTACKED KOMMER INTE KÖRAS IGÅNG
	- DÄRFÖR KAN VI INTE STARTA EN SECRET PÅ DAMAGE TAKEN ELR NÅGOT SÅNT
- Early exit också ifall minion attackerar hero men dör innan pga secret så ska inte hero ta dmg
- Play minion
- Draken sätter bara health, inte max health
- knife jungler triggers on moroes summon of miniions as it does on summon minion not play minion
- Position är nu viktigt också, man måste kunna lägga kort på rätt position pga direwolf alpha ger adjacent minions extra attack, men det ändras vad som är bredvid så försvinner attack
	- usually people give +1 attack then remove and they track
	- Det är inte give, utan det är bredvid
	- kanske ska vara if dire-wolf-adjacent då ska vi ha 1 mer attack
	- calculate during runtime if this minion is beside me
	- get-attack function if direwolf-adjacent SKA DET VARA

No references to specific minions in engine
- ska vara if du e deathrattle då ska vi köra deathrattle - gäller inte för oss längre


Bara full decision because functional - so if have a secret, hur ska vi tänka?

If non pure functions we 