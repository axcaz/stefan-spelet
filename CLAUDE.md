# Stefan i shorts

Ett litet pixelspel i en enda fil (`index.html`, HTML + JavaScript + canvas, inga beroenden utöver Google Fonts). Födelsedagspresent till Stefan.

## Så funkar koden
- Intern upplösning 320x240, rutor på 16 px, uppskalat med `image-rendering: pixelated`.
- Sprites ritas från textmatriser (`HEAD_D`, `BODY_D`, `LEGS_D` osv.) med paletten `PAL`. Stefan har varianter för ner, upp och sida, plus en variant med hjärtsolglasögon.
- Scener definieras med `def(id, {...})`: golv, väggar, dekor, utgångar och entiteter. Entiteter har `draw` och valfri `act` (interaktion).
- Dialoger är async: `await say(namn, text)` och `await ask(namn, text, [val])` som returnerar valets index.
- Mätare: adrenalin sjunker hela tiden, köld beror på scenens `cold`-värde.
- Tre stjärnor (svets, dockan, fallskärm) låser upp festen med tårtan och slutskärmen.
- `AVSANDARE` högst upp i skriptet styr texten "Kram från ...".

## Nästa steg (förslag)
1. `git init`, skapa repo på GitHub (`gh repo create stefan-spelet --public --source=. --push`) och slå på GitHub Pages från main.
2. Dela upp i filer (scener, sprites, dialog) när det växer.
3. Fler miljöer: camping i novemberregn, äventyrsbana, fjällvandring.
4. Garderob: rutiga byxorna och svarta skjortan som upplåsbara kläder.
5. Ljud (Web Audio, enkla pip), spara framsteg i localStorage.
