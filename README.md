# Onda — brasiliansk portugisisk

Puggeverktøy for muntlig trening. Norsk står alltid synlig; portugisisk og uttale ligger skjult under en «bølge» (*onda*) du drar, trykker eller bruker tastaturet på for å avsløre, rad for rad.

Nettsiden ligger på **https://mariusdevo.github.io/portugisiskpugg/**.

## Filer

| Fil | Hva den gjør |
|---|---|
| `index.html` | Selve appen. Endres sjelden. |
| `pensum.md` | Alle gloser og setninger. **Dette er fila du oppdaterer.** |
| `README.md` | Denne fila. |

Appen leser `pensum.md` hver gang sida lastes. Du trenger aldri å røre `index.html` for å legge til nytt stoff.

På mobilen: åpne adressen, og velg «Legg til på Hjem-skjerm» i nettlesermenyen. Da får du et ikon som åpner verktøyet i fullskjerm.

## Legge til nye gloser

1. Åpne `pensum.md` i repoet på GitHub.
2. Trykk blyantikonet (**Edit this file**).
3. Legg til en rad i riktig tabell:
   ```
   | norsk ord | portugisisk ord | [ot-TA-le] |
   ```
4. Trykk **Commit changes**.
5. Last inn nettsida på nytt. Den nye glosen er der.

Vil du ha en fullverdig editor i nettleseren: trykk `.` (punktum) når du står i repoet, så åpnes GitHub sin innebygde VS Code.

## Format som må følges

Tolkeren i appen forventer denne strukturen:

- Hvert kapittel starter med `## Tittel` — f.eks. `## 4. Tid`.
  Titler som begynner med «Appendiks» havner i egen gruppe i nedtrekksmenyen.
- Før hver tabell står en av disse merkelappene, som styrer hvor radene havner:
  - `**Gloser**` og `**Infinitiv — …**` → *Gloser*-fanen
  - `**Setninger**` og `**Eksempler**` → *Setninger*-fanen
- Hver tabell må ha nøyaktig denne overskriftsrada:
  ```
  | Norsk | Portugisisk | Uttale |
  |---|---|---|
  ```
- Uttale skrives i klammer: `[o NO-mi]`. Klammene fjernes automatisk i visningen.

Tabeller med andre overskrifter — for eksempel bøyningstabellene (`| Person | Presens | Fortid |`) og sammentrekningstabellene — hoppes over med vilje.

Hvis en tabell er feilformatert, sier sida fra øverst med kapittelnavn og linjenummer i stedet for å feile stille.

## Ekstra pugg

Trykk på det norske ordet i en hvilken som helst rad for å legge den i **Ekstra pugg** — en samleliste på tvers av kapitler, der gloser og setninger blandes. Trykk igjen for å fjerne.

Lista lagres i nettleserens eget lager (`localStorage`). Det betyr at:

- Hver besøkende får sin egen liste, uten innlogging.
- Lista overlever at du lukker fana.
- Den følger **ikke** med mellom mobil og PC — hver enhet har sin egen.
- Tømmer du nettleserdata, forsvinner lista.

## Merk

Sida må ligge på en webserver (som GitHub Pages). Åpner du `index.html` direkte fra skrivebordet, nekter nettleseren å hente `pensum.md`, og du får en feilmelding som forklarer det.
