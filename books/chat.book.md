#!/usr/bin/env ptbk

# ✨ Example: Chat

-   URL `https://promptbook.studio/examples/chat.book`
-   INPUT PARAMETER `{previousTitle}` Previous title of the conversation
-   INPUT PARAMETER `{previousConversationSummary}` Previous conversation summary
-   INPUT PARAMETER `{userMessage}` User message
-   OUTPUT PARAMETER `{title}` Title of the conversation
-   OUTPUT PARAMETER `{conversationSummary}` Summary of the conversation
-   OUTPUT PARAMETER `{chatbotResponse}` Chatbot response

## Create message

- PERSONA John, creative brainstormer

```markdown
Write reply to the user message in the chat:

> {userMessage}

**Rules**

- Topic of the conversation is {title}
- Write just the reply, nothing else
- Keep language of the user

**Previous conversation**

> {previousConversationSummary}

```

`-> {chatbotResponse}`

## Summarize conversation

```markdown
Summarize the conversation.

**User asked**

> {userMessage}

**Chatbot replied**

> {chatbotResponse}


**Previous conversation**

> {previousConversationSummary}

**Rules**

- Topic of the conversation is {title}
- Write just the reply, nothing else
- Keep language of the user

```

`-> {conversationSummary}`

## Make conversation title

- JOKER `{previousTitle}`
- EXPECT MIN 1 Word
- EXPECT MAX 1 Line

```markdown
Make title of the conversation.

**User asked**

> {userMessage}

**Chatbot replied**

> {chatbotResponse}

**Rules**

- Write just the title, nothing else
- Keep language of the conversation
- The title should be catchy
- Maximum 5 words long

```

`-> {title}`