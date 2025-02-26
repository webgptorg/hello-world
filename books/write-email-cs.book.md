# Correction & Improvement of email

Writing email assistant

-   PIPELINE URL https://promptbook.studio/miniapps-collection/write-email-cs.book.md
-   FORMFACTOR `Translator`
-   INPUT PARAMETER `{inputMessage}` Nástřel e-mailu
-   OUTPUT PARAMETER `{outputMessage}` Vyladěný text emailu
-   OUTPUT PARAMETER `{subject}` Předmět e-mailu

## Ukázka nástřelu

-   SAMPLE

```text
Ahj Jirko, Potřebu změnit termín nebo schůzku. Můžeme se sejít v pondělí v 10 hoin?
```

-> `{inputMessage}`

## Ukázka napraveného e-mailu

-   SAMPLE

```text
Ahoj Jirko,

Potřebuji změnit termín naší schůzky. Můžeme se sejít v pondělí v 10:00?

Díky moc,
Pavol H.
```

-> `{outputMessage}`


## Rozlišení tykání a vykání

- EXPECT EXACTLY 1 Word

```markdown

Detekujte, zda je v textu použito tykání nebo vykání, pokud si nejste jisti, použijte vykání.

Odpověz **pouze** jedním slovem: "tykání" nebo "vykání".

**Text**

> {inputMessage}


```

`-> {tykaniVykani}`


## Napsání e-mailu

-   PERSONA Tomáš, zkušený a pečlivý asistent
-   POSTPROCESS `unwrapResult`

```markdown
Z návrhu e-mailu odstraň chyby a přeformuluj text do finální podoby e-mailu:

**Pravidla**

- Zachovej {tykaniVykani}
- Přepiš věty tak, aby byly srozumitelnější
- Odstraň duplicitní informace
- Oprav gramatické chyby
- Přidej vhodný pozdrav a závěr e-mailu včetně ukončení a podpisu „Pavol Hejný“

**Nástřel e-mailu**

> {inputMessage}


## Sample of response 1

\`\`\`
Ahoj Jirko,
Tady bychom možná měli být – zařizoval jsi to už?

Díky moc,
Pavol H.
\`\`\`

```

`-> {outputMessage}`


## Předmět e-mailu

-   PERSONA Tomáš

```markdown
Napiš předmět e-mailu, který bude odpovídat obsahu e-mailu:

**Text e-mailu**

> {outputMessage}

```

`-> {subject}`