# brouter-profiles

[https://github.com/poutnikl/Brouter-profiles/wiki/Glossary](https://github.com/poutnikl/Brouter-profiles/wiki/Glossary)

Zvolíme-li analogii se zvukovou technikou, a bereme-li
Hlavní silniční síť = basy
3.trída až po zpevnené cesty - stredy
nezpevnené cesty - výšky ,

pak Nulový MTB_factor a smallpaved_factor nastaví základní preference na vyrovnaný equalizer , čímž se myslí že se uvažují základní priority nastavené v profilu .

Kladný MTB_factor zdurazní výšky a potlací basy
Záporný  MTB_factor zdurazní basy  a potlací výšky

Kladný  smallpaved_factor potlačí basy  a výšky
Záporný smallpaved_factor potlačí středy.

Všechny cesty mají v Brouter efektivní délku na 1 fyzický km >=1.0 km. Tím delší, čím méně je daná cesta žádaná. Routing engine pak hledá trasu s nejkratší efektivní délkou ( na kterou se přepočítávají i výškové změny ).

MTB_factor +1.0 zkrátí efektivní délku 1 km nezpevněné cesty o 1 km, ne však na méně než 1.0 km.
1 km silnice naopak o 1 km prodlouží. Zpevněné a polozpevněné cesty jsou někde mezi.

MTB_factor -1.0 zkrátí efektivní délku 1 km silnice o 1 km, ne však na méně než 1.0 km.
1 km nezpevněné cesty naopak o 1 km prodlouží. Zpevniné a polozpevniné cesty jsou nikde mezi.

smallpaved_factor +1.0 prodlouží efektivní délku 1 km silnic a nezpevněných cest až o 1 km.
Malé silnice, zpevněné a polozpevněné cesty prodlouženy nejsou nebo jen minimálně.

smallpaved_factor -1.0 prodlouží efektivní délku 1 km malých silnic,
zpevněných a polozpevněných cest až o 1 km.
Silnice a nezpevněné cesty prodlouženy nejsou nebo jen minimálně.

Záporný smallpaved_factor je umožněn spíše pro úplnost,
měl by smysl asi jen s výrazným kladným nebo záporným MTB faktorem,
jako prohnutí nakloněné přímky do paraboly.
