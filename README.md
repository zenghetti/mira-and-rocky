# Huisdierenoppas Curaçao

Web-app voor de dagelijkse zorg van huisdieren. De oppas vinkt taken af en de eigenaar ziet direct wat er gedaan is. Bovenaan staat schermbreed een strand met zee, een wit huisje en de dieren van de klant als avatar. Ze reageren op wat er gebeurt.

Prototype: één `index.html`, geen build, geen server. De voortgang wordt op het apparaat bewaard (`localStorage`), net als bij Ledger Island.

## Wat zit erin

- **Vandaag**: de takenlijst die uit de vragenlijst volgt (eten per dier, wandelingen, water, warmtelamp, kliko, eigen taken). Tik op het rondje om af te vinken. Via de knop *Opmerking toevoegen* kun je optioneel een keuze maken (bijvoorbeeld *Niet gegeten*) en een opmerking achterlaten.
  - Eten: *Heeft gegeten* (het dier eet de bak leeg) of *Niet gegeten* (het dier ligt naast een volle bak). Later kun je kiezen voor *Heeft alsnog gegeten*.
  - Wandelen (alleen honden): *Rustig gesnuffeld* of *Gerend & gespeeld*.
  - Om 21:00 lopen de dieren naar het huis en slapen ze. Je ziet dan alleen hun gezichtje in een raam of de deur, met een wolkje "Z z z". Om 06:00 of bij hun eerste activiteit komen ze weer naar buiten.
  - Binnen een half uur na het eten verschijnt af en toe "Lekker!" bij één dier tegelijk. Als er meerdere dieren gegeten hebben, wisselt het wie het zegt.
  - Lucht en water kleuren mee met de tijd: zonsopkomst, dag, zonsondergang en nacht. De zon en de maan lopen over de hemel.
- **Eigenaar-weergave**: alleen het belangrijkste. Een status per activiteit (eten, uitlaten, verzorging): groen = alles op tijd, oranje = opmerking of niet gegeten (met gedachtewolkje bij het dier), rood = te laat. Daaronder de opmerkingen van de oppas als kaartjes. Veeg ze weg of tik op het kruisje.
- **Seizoenen**: in december lichtjes in de palmboom, tijdens karnaval zijn de dieren verkleed (automatisch, of kies het onder Meer).
- **Vragenlijst**: dieren (hond/kat/schildpad, kleur, tekening, oren), voertijden met porties per dier, wandelingen, overige taken, medicatie, eigen taken en notities voor de oppas.
- **Berichten**: een chat tussen oppas en eigenaar, direct onder de animatie en boven de takenlijst. Beide kanten kunnen reageren.
- **Boeking**: eerst kies je of je een oppas zoekt of oppas aanbiedt.
  - Eigenaar: kies één dag, een periode of losse dagen met tijden (zoals bij een vliegticket), vul de vragenlijst in en stuur de aanvraag.
  - Oppas: de aanvraag komt binnen met alle informatie en kan geaccepteerd of geweigerd worden. Daarna zie je de boeking al staan, maar de animatie start pas bij het inchecken. Taken van vóór het inchecken staan grijs.
  - Zonder actieve boeking opent de app op dit scherm.
- **Logboek**: alle eerdere dagen.
- **Meer**: rol wisselen (oppas/eigenaar), NL/EN, licht/donker, een demo-klok om ochtend/avond/nacht te bekijken, export naar JSON voor Odoo en de voorbeelddata herstellen.

## Op GitHub Pages zetten

1. Maak een repository aan, bijvoorbeeld `huisdierenoppas`, en upload `index.html`, `README.md` en de map `docs/`.
2. Ga naar Settings → Pages → Branch: `main`, map `/ (root)` → Save.
3. Open `https://<gebruikersnaam>.github.io/huisdierenoppas/` op je telefoon en kies **Zet op beginscherm**.

## Naar Odoo

Zie [`docs/DATAMODEL.md`](docs/DATAMODEL.md) voor de modellen, velden en regels.
