[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/OfWcHlDv)
# Opdracht week 3: Continuous Delivery

Deze opdracht heeft een kort stuk theorie over 12Factor en praktijk van Continuous Integration. Je bouwt Continuous Integration flow in Gitlab CI en Jenkins. 

- [Opdracht week 3: Continuous Integration](#opdracht-week-3-continuous-integration)
  - [Opdracht](#opdracht)
  - [Gitlab CI](#gitlab-ci)
  - [Jenkins](#jenkins)

## Opdracht

Deze week moet jij als student drie continuous integration stages maken: `build`, `test`, `release` voor je applicatie uit vorige opdracht. Deze drie stages implementeer je in in `Gitlab CI`, `Jenkins Pipelines` of `GitHub Actions`. In overleg met de docent bepaal je je keuze.

### Maak een duo/team en zorg dat je samenwerkt in repo

Fork hiertoe deze repo naar een gedeelde private repo op [gitlab.devopsaimsites.nl](https://gitlab.devops.aimsites.nl/).
Zet in je README stapsgewijs  de benodigde stappen en benodigde git commando's (die vorige weken GitHub Classroom deels voor je deed).

### Deploy je .NET app (service + db) als Docker containers op VPS

Als je in opdracht 2 je applicatie nog niet (als docker container) hebt opgeleverd op eigen VPS, dan is dit nu een extra subopdracht van deze week.

- A. Tijdens de `build` stage test jij of het project wel compiled.
- B. Tijdens de `test` stage wordt getest of de unit tests slagen.
- C. In de `release` stage, in deze stage push jij een release image naar de container registry.
- D. Optioneel: Push je de image uit container registry dan naar bij vorige opdracht opgezette Docker container
- E. Optioneel: Voeg je een 'lint' stap voor waarin je je code checkt op afgesproken smells e.d.
- F. Optioneel: Kijk je naar mogelijkheden om stap D volgens een pull aanpak te doen i.p.v. push
- G. Theorieopdracht 12factor
- H. Update je Mermaid uit week 1 diagram om je uiteindelijk gerealiseerde CI integratie te tonen (pas ook kopje aan, zet weer een tag)

Eis is dat je een of meer pipeline configuratie bestanden IN je repository hebt staan en gebruikt. Liefst één. Dus enkel via grafische UI inregelen van je pipeline of een ander soort sandbox omgeving is niet de bedoeling (hoogstens een opstapje om concepten te verkennen en te gebruiken commando's voor de stappen uit te proberen. Zet in je README een link naar dit config bestand of deze bestanden en geef een korte bespreking ervan. Probeer de configuratie zo simpel mogelijk te houden, maar ook wel duidelijk (clean code/config). Dus refactor en hertest het hiervoor nog indien nodig, nadat je het eerst werkend hebt gekregen.

Voor hogere beoordeling kun je ook meerdere van de 3 pipeline systemen doen, en dan in je README iets documenteren/toelichten over verschillen/overeenkomesten (conceptueel is het erg hetzelde).

## Gitlab CI

Als je gebruik maakt van de publieke Gitlab dan heb je gelimiteerde CI minuten. Maar zelfs op 'self hosted' gitlab is het goed je pipeline zo lean en snel mogelijk kan maken. Denk hierbij aan Docker containers die je vanuit de container registry kan pullen ipv Docker hub.

## Tips bij Jenkins

1. Start een `jenkins` docker container. Mocht je een docker container willen bouwen in een Docker container vergeet dan niet de `dind` service.
2. Configureer `Gitlab` met `jenkins`, [deze](https://about.gitlab.com/handbook/customer-success/demo-systems/tutorials/integrations/create-jenkins-pipeline/#task-6-generate-an-api-token-for-gitlab-integration) guide kan helpen **(Note 9-2021: Handleiding vermeldt zelf dat deze 'deprectated' is: "These steps no longer work on the GitLab Demo Systems.")**.

## Theorie opdracht 12factor app

Hieronder een link naar een lijstje met een aantal (soms fictieve) quotes die een ICT'er zou kunnen uitspreken. Bepaal voor de jullie toegewezen quote of quotes welke factor uit de [12factor app](https://12factor.net) principles hierbij hoort. Elk punt is ofwel conform dit 12factor principe of gaat er juist tegenin. Ook kan het nog zijn dat de quote niet klopt ('beware of fake news'. Neem in de README.md van je applicatie een kopje `## 12factor app` op en zet hierin als eerste de quote en daaonder jullie antwoorden op 3 onderstaande vragen. De beschrijving bestaat uit circa 3 goedlopende paragrafen en is op zichzelf leesbaar, ook voor wie deze opdrachtbeschrijving niet kent. Verdiep je tot slot ook kort in de overige van de 12 factors door te kijken welke andere factoren relevant zijn, en evt. verbeter- of actiepunten voor je opleveren.

- A. Welke factor hoort het punt bij?<sup>*</sup> (Geef naam en korte uitleg in eigen woorden)
- B. Is het punt conform de 12factor app regel of gaat het er juist tegen in? (Leg uit, noem evt. tegengestelde punt/voorbeeld)
- C. Ben je het eens met het punt en waarom wel of niet? (Geef evt. voor en tegens)
- D. Welke van de andere 12factors zijn relevant voor deze opdracht? (Welke heb je aan gehouden? Welke zijn verbeterpunten (en hoe)? Bespreek minstens 4 v.d. 12)

<sup>*</sup>Indien je meerdere kandidaten vindt die passen, kies dan de meest bijpassende. Bij twijfel heeft het zeker meerwaarde om de andere kandidaten te noemen en waarom deze ook passen en beschrijf kort je argumenten je toch voor de ene hebt gekozen en niet de andere. Argumentatie is altijd belangrijker dan antwoord.

[Lijst met quotes](lijst-met-quotes.md)
