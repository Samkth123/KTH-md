

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
(def stateReal (create-game [{:minions ["Leper Gnome"]}{:minions ["Leper Gnome"]}]))
(def gamestate (firestone.construct/create-game [{:deck ["Sheep"]}]))

(def stateReal (firestone.construct/create-game [{:minions ["Leper Gnome"]}{:minions ["Leper Gnome"]}]))

(firestone.core-api/attack-minion stateReal "p1" "m1" "m3")


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



Deathratltle test leper gnoem before:
{:test (fn []  
         (let [game-state (create-game [{:hero "Gul'dan"} {:hero "Jaina Proudmoore"}])]  
           (is= (-> game-state  
                    (deathrattle-leper-gnome)  
                    (get-hero "h2")  
                    (:damage-taken))  
                2)                                        ;2 dmg  
           (is= (-> game-state  
                    (deathrattle-leper-gnome)  
                    (get-hero "h1")  
                    (:damage-taken))  
                0)                                        ; 0 dmg for p1  
  
           (is= (-> game-state                            ; test cummulative dmg  
                    (deathrattle-leper-gnome)  
                    (deathrattle-leper-gnome)  
                    (get-hero "h2")  
                    (:damage-taken))  
                4)                                        ;4 dmg  
           (is= (-> game-state                            ; if hero took dmg before leeper gnome dmg  
                    (update-in [:players "p2" :hero :damage-taken] + 3)  
                    (deathrattle-leper-gnome)  
                    (get-hero "h2")  
                    (:damage-taken))  
                5)  
           (is= (-> game-state                            ; hero dmg after lepper gnome dmg  
                    (deathrattle-leper-gnome)  
                    (update-in [:players "p2" :hero :damage-taken] + 3)  
                    (get-hero "h2")  
                    (:damage-taken))  
                5)  
           )  
         )  
 }