# ✨ Hello World!

In this repository, you will find a simple example of how to write your first [Book](https://github.com/webgptorg/book) and run it using the [Promptbook Engine](https://github.com/webgptorg/promptbook) via CLI.

1) First, you need to install the Promptbook Ecosystem. Currently, you can install it using NPM and run it via NPX. We are also working on an option to install it globally on your system:

```bash
npm i ptbk
```

2) Configure the environment variables - provide API keys for the model providers you want to use:

```conf
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
npx ptbk run ./promptbook-collection/hello.ptbk.md
```

And you should see the result:

```bash
$ npx ptbk run ./promptbook-collection/hello.ptbk.md
√ yourName ... Paul

--- Result: ---
greeting: Hello, Paul!
```

🚀✨ Now you have successfully run **your first Book!**