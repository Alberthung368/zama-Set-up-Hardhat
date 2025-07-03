# zama-Set-up-Hardhat
Set up Hardhat
In this section, you’ll learn how to set up a FHEVM Hardhat development environment using the FHEVM Hardhat template as a starting point for building and testing fully homomorphic encrypted smart contracts.

Create a local Hardhat Project
Install a Node.js TLS version
Ensure that Node.js is installed on your machine.

Download and install the recommended LTS (Long-Term Support) version from the official website.

Use an even-numbered version (e.g., v18.x, v20.x)

Hardhat does not support odd-numbered Node.js versions. If you’re using one (e.g., v21.x, v23.x), Hardhat will display a persistent warning message and may behave unexpectedly.

To verify your installation:

Copy
node -v
npm -v
Create a new GitHub repository from the FHEVM Hardhat template.
On GitHub, navigate to the main page of the FHEVM Hardhat template repository.

Above the file list, click the green Use this template button.

Follow the instructions to create a new repository from the FHEVM Hardhat template.

See Github doc: Creating a repository from a template

Clone your newly created GitHub repository locally
Now that your GitHub repository has been created, you can clone it to your local machine:

Copy
cd <your-preferred-location>
git clone <url-to-your-new-repo>

# Navigate to the root of your new FHEVM Hardhat project
cd <your-new-repo-name>
Next, let’s install your local Hardhat development environment.

Install your FHEVM Hardhat project dependencies
From the project root directory, run:

Copy
npm install
This will install all required dependencies defined in your package.json, setting up your local FHEVM Hardhat development environment.

Set up the Hardhat configuration variables (optional)
If you do plan to deploy to the Sepolia Ethereum Testnet, you'll need to set up the following Hardhat Configuration variables.

MNEMONIC

A mnemonic is a 12-word seed phrase used to generate your Ethereum wallet keys.

Get one by creating a wallet with MetaMask, or using any trusted mnemonic generator.

Set it up in your Hardhat project:

Copy
npx hardhat vars set MNEMONIC
INFURA_API_KEY

The INFURA project key allows you to connect to Ethereum testnets like Sepolia.

Obtain one by following the Infura + MetaMask setup guide.

Configure it in your project:

Copy
npx hardhat vars set INFURA_API_KEY
Default Values

If you skip this step, Hardhat will fall back to these defaults:

MNEMONIC = "test test test test test test test test test test test junk"

INFURA_API_KEY = "zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz"

These defaults are not suitable for real deployments.

Missing variable error:
If any of the requested Hardhat Configuration Variables is missing, you'll get an error message like this one:Error HH1201: Cannot find a value for the configuration variable 'MNEMONIC'. Use 'npx hardhat vars set MNEMONIC' to set it or 'npx hardhat var setup' to list all the configuration variables used by this project.

Congratulations! You're all set to start building your confidential dApp.

Optional settings
Install VSCode extensions
If you're using Visual Studio Code, there are some extensions available to improve you your development experience:

Prettier - Code formatter by prettier.io — ID:esbenp.prettier-vscode,

ESLint by Microsoft — ID:dbaeumer.vscode-eslint

Solidity support (pick one only):

Solidity by Juan Blanco — ID:juanblanco.solidity

Solidity by Nomic Foundation — ID:nomicfoundation.hardhat-solidity

Rest set the Hardhat project
If you'd like to start from a clean slate, you can reset your FHEVM Hardhat project by removing all example code and generated files.

Copy
# Navigate to the root of your new FHEVM Hardhat project
cd <your-new-repo-name>
Then run:

Copy
rm -rf test/* src/* tasks/* deploy ./fhevmTemp ./artifacts ./cache ./coverage ./types ./coverage.json ./dist
