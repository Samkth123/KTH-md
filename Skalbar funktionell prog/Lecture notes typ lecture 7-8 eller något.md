
Atoms - create and reset! and deref
(def my-favorit-number atom (atom 13))

dereference is a getter ;get
(deref my-favorit-number-atom)

we can also change our mind with setter ;set
(reset! my-favorit-number-atom 21)

How would we like to cahnge state?
in oop we just set and set and set, but we would not want to do it like this. Because the old states will be invalid and we cant get them and the previous states will not be valid. 

; single source of truth  - complex example

(def bank {id1 balance 5k} {id2 balance 0} {id3 balance 50k})

defn transfer
[bank from-account to-account amount]
-> bank
	(update-in [from-account :balance] - amount) ; update value inside
	(update-in [to-account :balance] + amount)

(transfer bank :accountid1 :accountid2 10)

; total money
function that takes bank in and check total money of bank defn total-money

; Naive version - get the value, update it, then push it back
; doing it from many threads, so one picks form bank and does transfer, but the threads ignore each other - therefore we need logging
(dotimes [_ 10]
	(future)
)

;Intermediate version: can we understand when things go 
; instead of doing reset, we can do logging. ex compare-and-set! which is only set new value if old value is what i want it to be. Here we need to have the old value of the bank

;the spin loop when-not can compare-and-set, we will retry with recur and loop from the start
; the language does the locking itself

;swap! can be used to swap bank-atom to a function of bank which does the body of the previous code.

;vi måste göra swap! i vår kod för swap! is a function used to atomically update the value of an atom by applying a function to its current value
;basically säger till att update göras atomically

;no code for stateful stuff as its single source of code


;Back to favorite number

; can add logging watcher

;set-validator! validator function checks whether a new value can be set for that reference. If the validator function returns nil, the value is accepted; if it returns any other value, the operation will be rejected, and an exception will be thrown


;create game - should we handle mana here and send it from end-turn!