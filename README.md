# LOOKSMAX

Enkel webbplats med innehåll som hämtas från Supabase och en inbyggd administratörssida.

## Delar

- `index.html`: startsida, innehållsbibliotek och administratörsgränssnitt.
- `facemath.html`: den tidigare FaceMath-funktionen, bevarad som ett separat verktyg.
- Supabase: innehållsdatabas, inloggning och bildlagring.

## Publicering

Webbplatsen är statisk och kan publiceras med GitHub Pages. Öppna **Settings → Pages** i GitHub och välj `main` som källa med `/ (root)` som mapp.

## Administratör

Administratörsadressen är `ninjafjanten1@gmail.com`.

1. Öppna webbplatsen och välj **Admin**.
2. Skapa kontot med administratörsadressen och ett starkt lösenord.
3. Bekräfta e-postadressen via meddelandet från Supabase.
4. Logga in via Admin.

Supabase Auth måste tillåta webbplatsens publicerade adress som Site URL/Redirect URL. Lägg till både den exakta webbplatsadressen och vid behov dess `/**`-variant under **Authentication → URL Configuration**.

## Säkerhet

- Webbplatsen använder endast Supabases publika nyckel. Ingen hemlig servernyckel finns i webbläsarkoden.
- RLS begränsar public läsning till publicerat innehåll.
- Skrivning, ändring, borttagning och bilduppladdning kräver en inloggad användare vars verifierade e-postadress är administratörsadressen ovan.
- Bilder lagras i den publika lagringsbehållaren `lookmax-media`. Ladda inte upp privata eller känsliga bilder.

## Innehåll

Administratören kan skapa, redigera, publicera och ta bort guider, rutiner, resurser och produkter. Textinnehåll sparas i databasen. Bilder kan laddas upp eller länkas externt.

## FaceMath

FaceMath körs i webbläsaren. Dess resultat är ungefärliga geometriska mätningar, inte vetenskapliga omdömen om skönhet, hälsa eller människovärde. Bilder skickas inte till webbplatsens databas.
