# Svelte Chat Langchain (Template)

This is a minimal version of "Chat LangChain" implemented with SvelteKit, Vercel AI SDK and or course Langchain!

The Template is held purposefully simple in its implementation while still beeing fully functional.

It is best used as reference to learn the basics of a QA chatbot over Documents or a starting point for your own custom implementation.

Deployed version: https://svelte-chat-langchain.vercel.app/

If you are completely new to Chatbots or any of the technologies used in this repository, this blog post is a good starting point: https://simon-prammer.vercel.app/blog/post/sveltekit-langchain

For more advanced features such as Indexing / Record Management, user feedback and stream parsing to display sources, I highly recommend checking out the original Chat Langchain repository(https://github.com/langchain-ai/chat-langchain).

This app features:

- Ingestion
  - Document Loading (from Langchain JS docs https://js.langchain.com/docs/get_started/introduction)
  - Document Splitting
  - Embedding using VercelPostgres as Vector Database
- Retrieval
- Langchain Expression Language (Sequences & Conditional Chaining)
- Streaming (simplified with Vercel AI SDK)

This repository is fully inspired by the original Chat Langchain repository.

Langchain Chat Website:
https://chat.langchain.com/

Langchain Chat Github:
https://github.com/langchain-ai/chat-langchain

Langchain Blog:
https://blog.langchain.dev/building-chat-langchain-2/

## Setup

### IMPORTANT - Set environment variables in a .env file (see .env.example for reference).

In the current configuration, you need:

- An OpenAI API Key
- A Vercel account
- A Vercel Postgres database instance to run the app (https://vercel.com/)
- Optionally (but highly encouraged) you can add a Langsmith API Key (https://docs.smith.langchain.com/) for debugging and testing chains.

### Install dependencies.

```sh
pnpm i
```

### Run the development server at http://localhost:5173/.

```sh
pnpm run dev
```

## Important note

If you build your own example, note that this repos uses a modified vite.config.ts which is necessary to use the environment variables in local development without explicitly declaring them in the code. This is not necessary in production.
