# XRP-Ledger-GPT-Chatbot
XRP-Ledger-GPT-Chatbot is a sophisticated chatbot, equipped with GPT-4 and trained using the [XRP Ledger](https://github.com/XRPLF/xrpl.js) codebase. The primary purpose of this bot is to answer any XRP Ledger related questions with specific answers and references to the relevant code files. This project's goal is to enhance the developer's experience on the XRP ledger. 

![XRP-Ledger-GPT-Chatbot UI](https://i.postimg.cc/MTRgpsBN/XRPL-gpt-ss.png)

### Prerequisites
- [Node.js](https://nodejs.org/en/download/) (v16 or higher)
- [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable)
- `wget` (installable in macOS through `brew install wget`)

### Data Ingestion
You first need to download our data source (Langchain docs) by running `sh download.sh`. After this, you can install dependencies and run the ingestion script using the command 'yarn && yarn ingest'.(If using Node v16, `NODE_OPTIONS='--experimental-fetch' yarn ingest`). The processed data is then saved under the `data/` directory.

### Running the Server
To run the development server, use the command `yarn dev`. Then, navigate to [http://localhost:3000](http://localhost:3000) to view the result.

### Deploying the server
The production version is hosted on [fly](https://chat-langchainjs.fly.dev/). For your own deployment, you may use `fly.toml` and `Dockerfile` as a starting point.

## Running on Your Example
If you want to chat your own data, you need to set up your own ingestion pipeline, and create a similar `data/` directory with a vectorstore in it. You'll also need to update the prompts used in `pages/api/util.ts` to suit your requirements.

All feedback and contributions are welcome!
