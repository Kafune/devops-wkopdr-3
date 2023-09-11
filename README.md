# Opdracht week 3: Continuous Integration

Deze week wordt er gefocused op Continuous Integration. Deze week bouw jij een Continuous Integration flow in Gitlab CI en Jenkins. 

- [Opdracht week 3: Continuous Integration](#opdracht-week-3-continuous-integration)
  - [Opdracht](#opdracht)
  - [Gitlab CI](#gitlab-ci)
  - [Jenkins](#jenkins)

## Opdracht

Deze week moet jij als student drie continuous integration stages maken: `build`, `test`, `release`. Tijdens de `build` stage test jij of het project wel compiled. Tijdens de `test` stage wordt getest of de unit tests slagen. Als laatste is de `release` stage, in deze stage push jij een release image naar de container registry. Deze drie stages moeten worden geïmplementeerd in `Gitlab CI` en `Jenkins`

Update het mermaid diagram om de huidige CI integratie te tonen.

## Gitlab CI

Mocht jij gebruik maken van de publieke Gitlab dan heb jij gelimiteerde CI minuten. Kijk of jij de pipeline zo snel mogelijk kan maken. Denk hierbij aan Docker containers die je vanuit de container registry kan pullen ipv docker hub.

## Jenkins

1. Start een `jenkins` docker container. Mocht je een docker container willen bouwen in een docker container vergeet dan niet de `dind` service.
2. Configureer `Gitlab` met `jenkins`, [deze](https://about.gitlab.com/handbook/customer-success/demo-systems/tutorials/integrations/create-jenkins-pipeline/#task-6-generate-an-api-token-for-gitlab-integration) guide kan helpen.
