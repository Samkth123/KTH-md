
test in sepearte file

Skriv koden med funktioner du önskar att du hade sen skriv funktioner för att göra det!!!

Typ updatemana, do deathrattle osv... Om inte funktionerna finns så skriv dom själv efter du skrivit funktionen som ska kalla på dom
- power of wishful thinking är det föreläsaren refers detta till

För demo:
- testerna måste finnas

Försök förstå flow av testerna som han visade

is= (-> state
(remove-card-from-deck "p1" card) ;in this state remove the card from p1s deck
(get deck "p1") ; then get the deck from the state
)

Tänk här att state slussas vidare å ändras, och man behöver inte skapa nya states hela tiden


Bra syntax:
let [card (first(get-deck state player-id))]
	(if card  ;basically om vi har ett kort yäni if card is truthy
	om true dra
	else
		fatigue)


assoc-in means we dont care about previous value the new value should be this