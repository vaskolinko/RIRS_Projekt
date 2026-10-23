# Podatkovni model
 
Rešitev uporablja relacijsko podatkovno bazo **PostgreSQL**, saj so podatki med seboj močno povezani (stavba → stanovanja → uporabniki → okvare in glasovanja).

## Povezave
 
- Stavba ima več **stanovanj**, **članov**, **vabil**, **okvar**, **glasovanj** in **obvestil** (1 : N).
- Uporabnik je prek **building_members** povezan s stavbo in, če je lastnik ali najemnik, s stanovanjem.
- Okvara se nanaša na stavbo in po potrebi na stanovanje; prijavi jo uporabnik, rešuje jo serviser.
- Okvara ima več zapisov v **zgodovini** (1 : N).
- Glasovanje ima več **glasov**, vsako stanovanje pa lahko glasuje le enkrat (`unique (poll_id, unit_id)`).

## Osnutek podatkovnega modela

 
<img width="2698" height="3209" alt="podatkovni-model" src="https://github.com/user-attachments/assets/cea4252a-5ccc-4e03-9aed-d5d83dd25163" />

