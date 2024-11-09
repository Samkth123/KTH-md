

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

##### FÖRSTA {} är första splarene andra e andra spelarnen
(def stateReal (create-game [{}]))

(def gamestate (firestone.construct/create-game [{:deck ["Sheep"]}]))


**call function and put output to something**
`(def result (increment 5))`


**call function that changes state**
(add-card-to-deck state player-id card :deck)

**add many things at the same time:**
(def stateNew  
  (-> state  
      (add-card-to-deck player-id "Leper Gnome" )  
      (add-card-to-deck player-id "Leper Gnome" )))


(def state  {:player-id-in-turn             "p1"
             :players                       {"p1" {:id       "p1"
                                                   :deck     []
                                                   :hand     []
                                                   :minions  []
                                                   :fatigue  1
                                                   :max-mana 8
                                                   :mana     8
                                                   :hero     {:name         "Jaina Proudmoore"
                                                              :id           "r"
                                                              :damage-taken 0
                                                              :entity-type  :hero}}
                                             "p2" {:id       "p2"
                                                   :deck     []
                                                   :hand     []
                                                   :minions  []
                                                   :fatigue  1
                                                   :mana     8
                                                   :max-mana 8
                                                   :hero     {:name         "Gul'dan"
                                                              :id           "h2"
                                                              :damage-taken 0
                                                              :entity-type  :hero}}}
             :counter                       1
             :minion-ids-summoned-this-turn []})
