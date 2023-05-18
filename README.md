# Setup Instructions

You should follow the setup instructions from the backend project (blockchain (backend)/FYP2023_P1-main/FYP2022_P4/dev/IPP) first before attempting to run this project.

You should have 3 contract keys after running your backend project. These 3 contract keys should be filled in to [constants.js](src/utils/constants.js).

You can choose any account to be the signer key in the same file. Once you are done, run `npm i && npm run start`, remember to keep your backend running at the same time `npx hardhat node`.

Voila! You should now be presented with the frontend connected to the backend blockchain. You may start creating policy, your backend terminal console should show that a contract has been created.

# What has been changed?
- [Constants](src/utils/constants.js): This is the file to centralize the hash values usage for the contract and signer. This is also to avoid any discrepancies of hash values used in the code.
- [Contracts](src/utils/contracts): This folder stores all the contract with the blockchain. The files are obtained when you set up your backend project, and do a deploy. The deployment will generate these files, called Application Binary Interface (ABI). Read more about it [here](https://www.alchemy.com/overviews/what-is-an-abi-of-a-smart-contract-examples-and-usage).
- [Web3Helpers](src/utils/web3Helpers.js): Some helper functions that have been written to centralize some common actions such as retrieving the list of policies stored.
- [policies.js](src/pages/policies.js): The function `refreshPolicies` is added to retrieve all policies from the blockchain and map to the frontend object.
- [payment.js](src/pages/payment.js): The function `refreshPayments` is added to retrieve all payments from the blockchain and map to the frontend object.
- [AddClientPolicy.js](src/pages/components/AddClientPolicy.js): The function of add policy is extended to write into the blockchain. There are other logic such as writing it into `IdMapping` and `PaymentStorage` contract. The logic is not invented, it is largely copied from the backend project `PolicyMgmtConsole.js`, the only changes is syntax change to follow the frontend syntax.
- [AddPayment.js](src/pages/components/AddPayment.js): This is similar to previous file, but this is for the payment. The logic is also copied from backend console code.

# Suggested Read
[Greeter Application with Hardhat](https://medium.com/coinmonks/build-a-web-3-application-with-solidity-hardhat-react-and-web3js-61b7ff137885)

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
