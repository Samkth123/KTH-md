

(def state
  {:player-id-in-turn "p1"
   :players {"p1" {:id "p1"
                   :deck [{:name "Loot Hoarder" :id "c1"}
                          {:name "Fireball" :id "c2"}] ; player 1's deck
                   :hand [{:name "Fireball" :id "c3"}
                          {:name "Loot Hoarder" :id "c4"}] ; player 1's hand
                   :minions [{:name "Leper Gnome" :id "m1" :position 0}] ; player 1's board
                   :hero {:name "Jaina Proudmoore" :entity-type :hero :damage-taken 0 :id "h1"}}
            "p2" {:id "p2"
                  :deck [{:name "Leper Gnome" :id "c5"}] ; player 2's deck
                  :hand []  ; player 2's hand is empty
                  :minions []  ; player 2 has no minions on board
                  :hero {:name "Jaina Proudmoore" :entity-type :hero :damage-taken 0 :id "h2"}}}
   :counter 1
   :minion-ids-summoned-this-turn []})



`(def result (increment 5))`
