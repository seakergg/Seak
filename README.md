# Seakk

Önálló sakkalkalmazás (HTML + JS). Webes (GitHub Pages) és Android (APK) változat ugyanabból a kódból.

## GitHub Pages (weboldal és PWA)
1. Hozz létre egy GitHub tárolót, és töltsd fel ennek a mappának a tartalmát (a `.github` mappával együtt).
2. Settings > Pages > **Source: GitHub Actions**.
3. A `main` ágra érkező push automatikusan közzéteszi az oldalt: `https://FELHASZNÁLÓ.github.io/TÁROLÓ/`.
   Minden közzététel új gyorsítótár-verziót kap, így a telepített PWA a következő megnyitáskor frissül.
4. A cím megadható a pwabuilder.com-on, és telefonon a böngészőből is telepíthető („Hozzáadás a kezdőképernyőhöz”).

## APK készítése
Actions > **Android APK** > Run workflow. A futás végén az Artifacts között találod az `app-debug.apk` fájlt.
`v1.0`-hoz hasonló címke esetén az APK a Releases oldalra is felkerül. A debug APK telepíthető, de nem Play Áruházba szánt.

## Lichess-bejelentkezés (OAuth)
Nincs regisztráció és titkos kulcs, az app PKCE-t használ. A weben a visszatérési cím az oldal saját címe (a Pages-cím),
az APK-ban a `hu.seakk.app://oauth` (a workflow beállítja az AndroidManifest.xml-ben).
