# NORDMAX

Nordisk kunskapsplattform för hållbar utveckling inom hud, hår, träning, sömn, kost, stil och ansiktsproportioner. Varumärket använder en mörk, exklusiv och avskalad nordisk form. Innehållsbiblioteket hämtar publicerade artiklar från Supabase och har ett inbyggt administrationsgränssnitt.

## Delar

- `index.html`: NORDMAX-startsida, communityforum, innehållsbibliotek och administratörsgränssnitt.
- `facemath.html`: FaceMath, ett experimentellt verktyg för förenklade geometriska ansiktsmätningar.
- Startsidan innehåller fördjupade kunskapsguider, säkerhetsinformation och en stegvis handlingsplan.
- Supabase: innehållsdatabas, medlemskonton, forumtrådar, svar, inloggning och bildlagring.
- Forumet har ämneskategorier, medlemsprofiler, trådskapande och svar. Forumfunktionerna kräver medlemskonto; läsning är öppen.
- Forumtabellerna `member_profiles`, `forum_threads` och `forum_replies` skyddas med RLS. Medlemmar kan bara skapa och ändra egna profiler/inlägg enligt respektive policy.

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


## Redaktionell information

Kunskapsinnehållet är allmän vägledning och ersätter inte individuell bedömning av legitimerad vårdpersonal. FaceMath är inte diagnostik eller ett vetenskapligt mått på attraktivitet. Den lilla signaturen längst ned anger att webbplatsen är grundad av Roman Kelder. Ingen medicinsk yrkestitel påstås.
