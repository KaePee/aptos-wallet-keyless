# Aptos Keyless Wallet Example

Aptos Keyless Wallet Example provides a seamless way to abstract the complexities of account generation for public and private keys. This project enables users to log in using Single Sign-On (SSO) methods like Google, offering a streamlined process for obtaining wallet addresses without the need to manage private or seed phrases.

## Features

- **SSO Integration**: Log in with Google to automatically receive a wallet address.
- **Key Management Abstraction**: No need to handle private keys or seed phrases.
- **Test Transactions**: Easily send APT to another address for testing purposes.

## Installation


## Configuring Google

Here are the step-by-step instructions for obtaining OAuth credentials for Google:

1. Go to the [Google Cloud Console](https://console.cloud.google.com/welcome) and sign in to your account.
2. Once you’re signed in, click on the project dropdown menu in the top navigation bar and select or create the project you want to use for your OAuth credentials.
3. Click the search bar at the top of the page and search for **"OAuth consent screen"**.
4. Complete the **"Configure Consent Screen"** instructions if you haven’t completed this before.
5. On the left, click **"Credentials"**. Towards the top of the screen click the **"Create Credentials"** dropdown and select **"OAuth client ID"**.
6. Select the **"Web application"** application type.
7. Enter a name for your OAuth client ID, such as **"Local Development"**.
8. In the **"Authorized JavaScript origins"** field, enter the origin of your web application: `http://localhost:5173`
9. In the **"Authorized redirect URIs"** field, enter the URI that Google should redirect users to after they authorize your application. This should be: `http://localhost:5173/callback`.
10. Click the **"Create"** button to create your OAuth client ID.
11. After creating your OAuth client ID, you should see a **"Client ID"** and **"Client Secret"** on the **"Credentials"** page. Copy the **"Client ID"** and paste it into `src/core/constants.ts`

That's it! You should now be able to authenticate with Google in your application.

If you need more help with configuring the Google OAuth App check their docs [here](https://support.google.com/cloud/answer/6158849).


Ensure you have copied your google client id above into the `src/core/constants.ts` file

To get started with the Aptos Keyless Wallet Example, follow these steps:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/KaePee/aptos-wallet-keyless.git
   cd aptos-wallet-keyless
   ```

2. **Install Bun**

   Follow the instructions on the [Bun website](https://bun.sh) to install Bun.

3. **Install Aptos**

   Install Aptos using npm:

   ```bash
   npm install aptos
   ```

## Usage

Run the project locally:

```bash
bun dev
```

This will start a development server at `http://localhost:5173`. Users can connect their Google account to acquire a wallet address and perform test transactions by sending APT to another address.

## Contributing

We welcome suggestions and contributions to the repository. Please open an issue or submit a pull request with any improvements or feature requests.

## Sample

![Sampple screen](https://github.com/KaePee/aptos-wallet-keyless/blob/main/demo/aptos-keyless-demo.gif)
---

