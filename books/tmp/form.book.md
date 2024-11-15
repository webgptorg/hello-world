# Zpracování formuláře


-   URL `https://promptbook.studio/examples/form.book`
-   INPUT PARAMETER `{fullname}` Jméno zákazníka
-   INPUT PARAMETER `{businessProblem}` Popsaný problém
-   OUTPUT PARAMETER `{email}` Email pro zakaznika

## Vycisteni problemu

-   PERSONA Paul, analytic who can simplify the problem

```
Simplify the problem from customer, get rid of unimportant information:

> {businessProblem}

```

`-> {filteredBusinessProblem}`

## Ideace

-   PERSONA John, creative brainstormer
-   EXPECT MIN 5 Lines
-   EXPECT MAX 25 Lines
<!-- TODO: !!! -   KNOWLEGDE ./company-strategy.pdf -->

```
Write me a list of ideas connected with problem

> {filteredBusinessProblem}

```

`-> {ideas}`

## Analyza

-   PERSONA Anička, copywriterka, co umí přemýšlet businessově a má smysl pro humor
-   EXPECT MIN 1 Sentence
-   EXPECT MAX 1 Page
<!-- TODO: !!! -   KNOWLEGDE ./company-strategy.pdf -->

```
Napiš mi email pro zákazníka, který má tento problém:

> {filteredBusinessProblem}

Nápady co použij:

- {ideas}

```

`-> {email}`
