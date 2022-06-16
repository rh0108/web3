# 💻 Requirements

You will need to [install the Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools) to complete this Pathway.

## 🐑 Local clone

If you cloned the `learn-web3-dapp` repo locally, pay attention to the following:

{% hint style="tip" %}
**Windows Users:** There are known compatibility issues with the Solana BPF toolchain. You will need to use the Windows Subsystem for Linux to compile Solana programs. Please refer to the [installation guide](https://docs.figment.io/network-documentation/extra-guides/solana-setup-for-windows) we have provided.\
**macOS Users:** If you are using any Apple Silicon products (M1 processor), you may need to build the Solana CLI from source. [Refer to this article for more information](https://dev.to/codenjobs/how-to-make-solana-test-validator-work-with-a-macbook-with-m1-chip-5emd).
{% endhint %}

---

# 🧩 DataHub API keys

If you wish to make use of the Pathway content using DataHub, you will need a DataHub account and a valid API key to access Solana via DataHub's infrastructure. [Sign up for a DataHub account](https://datahub-beta.figment.io/signup) and verify your email address. Once you have logged in to DataHub, you will need to create a new app and select the Solana protocol.

Click "Create New App":

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/dh_api_1.png?raw=true)

Type in a name for your app, select the **Staging** environment, then click on the **Solana** icon in the list of available protocols. \
Click "Create app" when you're finished:

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/dh_api_2.png?raw=true)

You can now find your API key on the Overview tab of the app on the [**DataHub Dashboard**](https://datahub-beta.figment.io/apps):

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/dh_api_3.png?raw=true)

To use your API key, you should copy the contents of the `.env.example` file located in the project root directory (`/learn-web3-dapp/.env.example`) into a new file named `.env.local` (`/learn-web3-dapp/.env.local`). Also, since this file will contain your API key, we have already added it to the `.gitignore`.

{% hint style="info" %}
Easily duplicate the file with the terminal command `cp .env.example .env.local`!
{% endhint %}

You can then paste your unique API key into `.env.local`, as the value for the environment variable `DATAHUB_SOLANA_API_KEY`. This will authenticate you and enable you to make requests to Solana via DataHub. **The API key shown below is only an example and cannot be used to access DataHub**.

```yaml
# DataHub API keys
DATAHUB_AVALANCHE_API_KEY=
DATAHUB_CELO_API_KEY=
DATAHUB_NEAR_API_KEY=
DATAHUB_POLKADOT_API_KEY=
DATAHUB_POLYGON_API_KEY=
DATAHUB_SECRET_API_KEY=
DATAHUB_SOLANA_API_KEY=81436edcf907b0fbb8493d281cdff5af
DATAHUB_TEZOS_API_KEY=
```

---

# 🤖 Using a Test Validator

At some point it may be necessary to run a Test Validator. For example, if you can't get airdrops because the Devnet faucet is not working. To run a local Test Validator you will need to have the Solana CLI installed. Use this command in its own terminal tab or window :

```text
solana-test-validator
```

Use `solana config set` to target a particular cluster. After setting a cluster target, any future subcommands will send/receive information from that cluster. To target a running Test Validator with the Solana CLI :

```text
solana config set --url http://localhost:8899
```

You can see which cluster the Solana command-line tool (CLI) is currently targeting and the paths to your keypair and configuration file with the command :

```text
solana config get
```

---

# 🔐 Keypair storage

During the "Create an account" step, you will need to generate a keypair for use in the tutorials (by completing the code challenge). This keypair is kept in the localstorage of your web browser, and is distinct from any keypairs generated by the Solana CLI. After the keypair is generated, it will remain visible (and copyable) at the top of the screen.

![](https://raw.githubusercontent.com/figment-networks/learn-web3-dapp/main/markdown/__images__/solana/solana-setup-02.png)

---

# 👣 Next Steps

Once you have your Solana API key saved in `/learn-web3-dapp/.env.local`, you're ready to begin.
Click on the **Next: Connect to Solana** button below.