# Discord Gang Hírek

Magyar nyelvű hírportál-oldal négy rovattal (Belpolitika, Külpolitika, Tech, AI), piaci adatokkal és közelgő választásokkal.

## Hogyan frissül

- A hírek a Supabase `news_editions` táblájában vannak; az oldal megnyitáskor a legutóbbi kiadást tölti be, nyitva hagyva 10 percenként újra megnézi.
- Egy Claude routine naponta kétszer (7:00 és 18:00, budapesti idő) összegyűjti és ellenőrzi a híreket, és új kiadásként beírja a táblába.
- Ha az adatbázis épp alszik, az oldal a fájlba épített, utolsó mentett kiadást mutatja, majd magától átvált a friss adatra.

## Fájlok

- `index.html` – maga az oldal (React + htm, saját CSS, csak világos mód)
- `_headers` – Netlify fejlécek (az oldal mindig az aktuális verziót tölti)

## Telepítés

Netlify: a mappát egy új oldalként kell feltölteni (app.netlify.com/drop), vagy a repót összekötni egy Netlify oldallal (build parancs nélkül, publish könyvtár: a repó gyökere).

## Források és képek

A kártyák rövid összefoglalók, a teljes cikk az eredeti forrásnál olvasható. A képek a cikkek saját borítóképei a forrás megjelölésével, a logók a hírportálok ikonjai.
