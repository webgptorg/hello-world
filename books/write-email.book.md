# Correction & Improvement of email

Writing email assistant

-   PIPELINE URL https://promptbook.studio/miniapps-collection/write-email.book.md
-   FORMFACTOR `Translator`
-   INPUT PARAMETER `{inputMessage}` Input text
-   OUTPUT PARAMETER `{outputMessage}` Corrected text

## Sample of incorrect text

-   SAMPLE

```text
Heloo Jirka,

I need to reshedule or meeting. Can we meet on mon 10 am?

Pavol H
```

-> `{inputMessage}`

## Sample of corrected text

-   SAMPLE

```text
Hello Jirka,

I need to reschedule our meeting. Can we meet on Monday at 10:00?

Kind regards,
Pavol H.
```

-> `{outputMessage}`

## Correct the text

-   PERSONA Jane, experienced copywriter and content creator

```markdown
Rewrite and improve the following email grammatically and stylistically:

## Rules

- Preserve T–V distinction, for example in Czech language Vykání/Tykání
- Maintain the formality of the email
- Rearrange words and sentences to make them easier to understand
- Remove duplicate information
- Correct grammatical errors
- Correct upper and lower case
- Add commas and periods
- Correcting punctuation
- Reply with corrected text only
- Add a proper opening to the email in the language in which the email is written
- Add an appropriate closing to the email, including a signature "Pavol Hejný".

## Text to correct

\`\`\`
{inputMessage}
\`\`\`

Reply with corrected text only, do not write anything else:
```

`-> {outputMessage}`


