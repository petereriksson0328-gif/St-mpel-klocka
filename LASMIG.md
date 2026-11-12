# UE-stämpelklocka – installation

En offline-app för arbetsledare. All data sparas i telefonen. Den behöver inget konto och ingen uppkoppling efter installationen.

## 1. Lägg upp filerna (en gång)
Appen måste ligga på en https-adress för att kunna installeras och fungera offline. Det enklaste är GitHub Pages:

1. Skapa ett nytt repo på GitHub, t.ex. `ue-klocka`.
2. Ladda upp alla filer i mappen: `index.html`, `installera.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`.
3. Gå till Settings → Pages → Source: *Deploy from a branch*, välj `main` / root och klicka Save.
4. Efter någon minut ligger appen på `https://<ditt-användarnamn>.github.io/ue-klocka/`.

Adressen innehåller ingen data, bara själva appen. Registreringarna finns bara i varje arbetsledares telefon.

## 2. Installera på telefonen (varje arbetsledare)
- **iPhone:** Öppna länken i Safari → Dela → *Lägg till på hemskärmen*.
- **Android:** Öppna länken i Chrome → ⋮ → *Installera app* / *Lägg till på startskärmen*.

Öppna appen en gång medan telefonen har täckning. Därefter fungerar den utan internet.

## 3. Första start
Under **Inställningar**: fyll i ditt namn och e-postadressen som rapporterna ska skickas till.

## 4. Skicka rapport
**Rapport** → välj period → **Skicka rapport (fil)**. Telefonens delningsmeny öppnas med CSV-filen bifogad. Välj Mail eller Outlook. Mailet skickas när telefonen får täckning.
**Mail med sammanfattning** öppnar ett mail med timmar per UE och dag samt de som gick tidigare, direkt i texten.

## Bra att veta
- Rast räknas in i arbetstiden.
- Om man rensar webbläsarens data försvinner registreringarna. Skicka rapport varje vecka och ta en **säkerhetskopia** under Inställningar ibland.
- Uppdatera appen: ladda upp ny `index.html` och höj `CACHE = "ue-klocka-v1"` i `sw.js` till `v2`.
