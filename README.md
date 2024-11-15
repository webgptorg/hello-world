# ✨ Hello World!

In this repository, you will find a simple example of how to write your first [Book](https://github.com/webgptorg/book) and run it using the [Promptbook Engine](https://github.com/webgptorg/promptbook) via CLI.

1) First, you need to install the Promptbook. Currently, you can install it using NPM. We are also working on an option to install it via package managers and installer files like `.msi`, `.rpm` or `.deb`:

```bash
npm i ptbk
```

2) Configure the environment variables - provide API keys for the model providers you want to use:

```conf
# Note: You just need to configure one provider:

# OpenAI
OPENAI_API_KEY=sk-proj-...

# Anthropic claude
ANTHROPIC_CLAUDE_API_KEY=sk-ant-api03-...

# Azure OpenAI
AZUREOPENAI_API_KEY=...
AZUREOPENAI_RESOURCE_NAME=...
AZUREOPENAI_DEPLOYMENT_NAME=...
```

3) Then you can run the example from this repository:

```bash
npx ptbk run ./books/hello.book.md
```

And you should see the result:

```bash
$ npx ptbk run ./books/hello.book.md
√ yourName ... The World

--- Result: ---
greeting: Hello World!
```

🚀✨ Now you have successfully run **your first Book!**