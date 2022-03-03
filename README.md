Ukeoppgaver JavaScript 3
Oppgave 1
Lag en enkel HTML-side der du kan skrive inn navnet og alderen din i to forskjellige
tekstbokser. Skriv så JavaScript-kode i samme fil for å vise navnet og alderen når en knapp
trykkes. Lag så en sjekk på aldersfeltet om feltet inneholder et tall som er større enn null.
Dersom det ikke er det skal det skrives ut en feilmelding enten via en «alert»-boks eller i et
eget felt.


Oppgave 2
Lag en HTML-side som konverterer fra farenheit til celsius. Formelen er:

C = (5/9)*(F-32)
Legg også til mulighet for å konvertere andre veien (fra celsius til farenheit) hvor formelen er:

F = (9/5)*C+32
Lag innputfelter for C og F.
Dersom det skrives inn noe i inputfeltet for C så skal tilsvarende verdi i F legges ut i dette feltet.
Dersom det skrives inn noe i inputfeltet for F så skal tilsvarende verdi i C legges ut i dette feltet.
JavaScript skal brukes ved beregning og utlegging av resultater.

Oppgave 3
Lag en HTML-kalkulator med to inputfelt og fire knapper, en for hver av regneartene +, - ,* og /.
Lag så JavaScript-kode som avhengig av hvilken knapp som er trykket viser resultatet av
regnestykket. Det skal også valideres at inputfeltene bare kan inneholde tall (også dette i form
av JavaScript-kode). Feilmeldinger skal også vises dersom det blir skrevet inn noe annet enn tall i
inputboksene.

Oppgave 4
Utvid ukeoppgaven fra i forrige uke (personregister) med å ha mulighet for å lese inn persondataene via tekstbokser også legge disse objektene inn i arrayet. Dette skjer ved en ny knapp. Samme funksjonalitet for å vise arrayet (via egen knapp).

Ekstraoppgaver
Disse ekstraoppgavene kan være litt mer krevende.

Ekstraoppgave 1
Lag en gjøremålsliste (todo-liste). Det skal være et tekstfelt hvor brukeren kan legge til gjøremål. Ved onchange skal verdien av skriv inn feltet legges til som et gjøremål i en HTML-liste. Ved siden av hvert gjøremål skal det være en sjekkboks som brukeren kan krysse av hvis oppgaven er ferdig.
Tips: Bruk metoden dinTabell.insertAdjacentHTML('beforeend', "todo html her") i stedet for innerHTML siden det vil resette alle sjekkboksene hver gang det legges til et element.

Ekstraoppgave 2
Utvid forige oppgave med å lage enda en liste. Den første listen skal nå kun inneholde uferdige gjøremål og den andre kun ferdige. Du skal også markere alle ferdige gjøremål med en strek gjennom de. Bruk textDecoration = "line-through".
Tips: Gi en unik id til alle gjøremålene og kall en funksjon med denne id'en som parameter hvis sjekkboksen sjekkes/usjekkes. Du kan flytte et element fra en liste til en annen med metoden denAndreListen.appendChild(dittGjøremål)

Ekstraoppgave 3
<button onclick="skrivUtOppgaver()">Ta test!</button>
<ul id="liste"></ul>
<script>

    const liste = document.getElementById('liste')
        const oppgaver = []

        const oppgave1 = {
            sporsmol: "Når er frist for oblig 1?",
            alternativer: ['1. Februar', '6. Februar', '12. Februar'],
            riktigIndex: 2
        }

        const oppgave2 = {
            sporsmol: "Hvor mange obliger er det i dette faget?",
            alternativer: ['3', '5', 'ingen', '2'],
            riktigIndex: 0
        }

        const oppgave3 = {
            sporsmol: "Hva står API for?",
            alternativer: ['App Program Instruction', 'Application Programming Interface', 'Det er ikke en forkortelse'],
            riktigIndex: 1
        }

        oppgaver.push(oppgave1)
        oppgaver.push(oppgave2)
        oppgaver.push(oppgave3)
</script>
Ta utgangspunkt i koden over og lag en quizz-applikasjon. Når brukeren klikker "Ta test!" skal hver oppgave listes ut med spørsmålet og hvert svaralternativ som en radioknapp. På bunnen av siden skal det komme opp en "Sjekk svar" knapp. Brukeren skal så kunne klikke på de alternativene som vedkommende tenker er riktig og deretter klikke "sjekk svar". "Sjekk svar" skal telle opp hvor mange oppgaver som er riktige og lage en alert-boks med for eksempel: "2 av 3 svar riktig!"  

Tips: Gi hver radio knapp et navn som tilsvarer den oppgaven den hører til (feks: "oppgave-1") og bruk document.querySelectorAll('[name="oppgave-1"]') for å samle alle radio knappene til den oppgaven i en node liste (fungerer omtrent som en array)
