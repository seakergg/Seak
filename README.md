# Seakk

Önálló sakkalkalmazás (HTML + JS). Az APK-t a GitHub építi.

## APK készítése
1. Hozz létre egy GitHub tárolót, és töltsd fel ennek a mappának a tartalmát (a `.github` mappával együtt).
2. Actions fül > **Android APK** > Run workflow (push a `main` ágra is elindítja).
3. A futás végén az **Artifacts** között letöltheted a `seakk-apk` csomagot, benne az `app-debug.apk` fájllal.
4. Telepítés a telefonra: engedélyezd az ismeretlen forrásból származó alkalmazásokat.

`v1.0`-hoz hasonló címke (tag) esetén az APK a Releases oldalra is felkerül.
A debug APK telepíthető, de nem Play Áruházba szánt. Ahhoz saját aláíró kulcs kell.

## PWA / PWABuilder
Actions > **GitHub Pages (PWA)** > Run workflow. Az így kapott HTTPS-cím megadható a pwabuilder.com-on.
