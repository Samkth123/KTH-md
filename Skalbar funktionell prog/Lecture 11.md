näst sista
start sprint 4

Undo button:
- Store states in database
- If list then we work on front of list
- state (first (:state))
Need swap state button
conj state and next state

Redo button:
cant drop anyhting
need to maybe store in another list?
if tick reset, but if redo then move back
use a db-atom
update :states (fn[states])
if drop one then add one to redo state list :redo-states and here conj states and first (:states db)

should only have 1 atom we handle db in (db-atom)

no inter-op