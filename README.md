# Úszoda foglaltsági rendszer 🏊

Interaktív, kattintható foglaltsági nézet a **Pilisvörösvári Tanuszoda** nyári beosztásához
(2026. június 14. – augusztus 31.). Egy Excel-táblából (képről kiolvasva) készült, könnyen
kezelhető web-felület.

👉 **Élő demó:** ha GitHub Pages-re teszed, az `index.html` magától betöltődik (lásd lentebb).

---

## Funkciók

- **Két nézet, egy kapcsolóval** (jobb felső sarok):
  - **▦ Rács** – a klasszikus, Excel-szerű heti hőtérkép (asztali gépre).
  - **☰ Lista** – mobilbarát, pályánkénti idővonal kártyákkal (telefonon automatikusan ezzel indul).
- **Heti navigáció** – a felső sávban kiválaszthatod a kívánt hetet (a teljes dátumtartománnyal),
  vagy az **Összes hét** gombbal egyben láthatod mindet. Indításkor az **aktuális hét** kerül fókuszba.
- **Idősáv-kereső** – add meg, mettől meddig keresel szabad időpontot (pl. `15:00 – 17:00`).
  A rendszer:
  - kiemeli a keresett ablakot, a szabad cellákat **zöldre** váltja, a tartományon kívülieket halványítja,
  - a teljesen szabad pályákat **✓ / „Szabad a sávban"** jelzéssel látja el,
  - hetente kiírja, hány pálya szabad (külön az úszó- és a tanmedencére).
- **Heti statisztika** – minden hétnél külön foglaltsági % az **úszó-medencére** (6 pálya) és a
  **tan-medencére** (2 pálya).
- **Részletek** – vidd az egeret (vagy érintsd meg) egy sávot a pontos időpontért és állapotért.
- **Teljesen offline** – az `index.html` egyetlen, önálló fájl, nincs hálózati függősége.

### Jelmagyarázat
- 🟥 **Foglalt** &nbsp;&nbsp; 🟦 **Szabad** &nbsp;&nbsp; 🟩 **Szabad a keresett idősávban**

---

## Fájlok

| Fájl | Leírás |
|------|--------|
| `index.html` | **Kész, önálló alkalmazás** – ezt tedd a GitHubra / nyisd meg. |
| `Uszoda foglaltsag v2.dc.html` | A forrás (szerkeszthető verzió, rács + lista kapcsolóval). |
| `Uszoda foglaltsag.dc.html` | Korábbi verzió (V1) – csak rács nézet. |
| `README.md` | Ez a leírás. |

---

## Az adatok módosítása

A foglaltsági adatok a forrásfájlban (`Uszoda foglaltsag v2.dc.html`) a `RAW` tömbben vannak.
Felépítés: **10 hét × 8 pálya × 28 félórás sáv** (06:00–20:00).

- Soronként egy 28 karakteres szöveg, ahol `1` = foglalt, `0` = szabad.
- Az első 6 sor az **úszó-medence** (1–6. pálya), az utolsó 2 a **tan-medence** (1–2. pálya).

Módosítás után az önálló fájlt újra kell generálni a forrásból.

---

## Testreszabható beállítások

A forrás Design Component beépített beállításai:

- **Téma** – színséma: `Klasszikus` (piros / sötétkék), `Tenger`, `Kontraszt`.
- **Sormagasság** – a rács celláinak magassága (20–44 px).
- **Hétköznap-felirat** – a „hétfő – péntek" megjegyzés ki/be kapcsolása.

---

_Az adatok a feltöltött heti beosztás-képről lettek kiolvasva; ellenőrzött pontossággal, de
hivatalos foglalás előtt érdemes egyeztetni az uszodával._
