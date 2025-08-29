
## Prerequisites

Before getting started, make sure you have the following installed and configured:

* **Node.js**
* **Hardhat** (Ethereum development environment)
* **OpenAI API key**

---

## Project Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/steto1/gpt-token.git
   cd gpt-token
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `contracts` folder (empty at first).

4. Create a `.env` file in the root directory and add the following variables:

   ```
   OPENAI_API_KEY=<your-openai-api-key>
   GOERLI_PRIVATE_KEY=<your-goerli-private-key>
   GOERLI_URL=<your-goerli-rpc-url>
   ```

---

## Customizing GPT Behavior

The **`deploygpt4.ts`** script (located in the `scripts` folder) controls all GPT interactions.

* **API Key** → Retrieved at **Line 11** from the `.env` file.
* **OpenAI API Calls** → Implemented at **Line 17** and **Line 96**. Modify the request payload or headers to adjust GPT responses.
* **DALL·E Integration** → For image generation, see **Line 277** to customize how DALL·E is used.

---

## Running the Project

* **Local execution:**

  ```bash
  npx hardhat run scripts/deploygpt4.ts
  ```

* **Deploy to blockchain (Goerli testnet):**

  ```bash
  npx hardhat run scripts/deploygpt4.ts --network GOERLI
  ```

---

⚡ This setup allows you to experiment with AI-driven smart contracts, integrate GPT/DALL·E, and deploy seamlessly to Ethereum testnets.
