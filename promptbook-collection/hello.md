# ✨ Example: Write Hello for a user

-   PIPELINE URL https://promptbook.studio/examples/hello.ptbk.md
-   INPUT PARAMETER `{yourName}` Name of the user
-   INPUT PARAMETER `{greeting}` Greeting for the user

## Writing Greeting

-   PERSONA Jane, HR professional with prior experience in writing emails
-   EXPECT MAX 1 Word
-   EXPECT MAX 1 Line

```markdown
You are writing a greeting for {yourName}.

## Rules

-   Write just the greeting, nothing else
```

`-> {greeting}`