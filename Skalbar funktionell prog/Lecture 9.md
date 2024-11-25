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

No references to specific minions in engine
- ska vara if du e deathrattle då ska vi köra deathrattle - gäller inte för oss längre


Bara full decision because functional - so if have a secret, hur ska vi tänka?