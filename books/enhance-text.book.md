# Correction & Improvement

Show how to use a simple prompt

-   PIPELINE URL https://promptbook.studio/miniapps-collection/enhance-text.book.md
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
Rephrase and improve the following text grammatically:

## Rules

-   Rearrange the words and sentences to make them easier to understand
-   Remove duplicate information
-   Correct grammatical errors
-   Correct upper and lower case letters
-   Add commas and periods
-   Correct punctuation
-   Reply with corrected text only

## Text to correct

\`\`\`
{inputMessage}
\`\`\`

Reply with corrected text only, do not write anything else:
```

`-> {outputMessage}`


