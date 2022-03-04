# Example app using nested components

This example is used to reproduce a bug in the dev process of cypress.

## March 3rd, 2020

steps to reproduce the bug

```sh
git clone https://github.com/elevatebart/create-nested-components.git
cd create-nested-components
yarn install
cd ..
git clone https://github.com/cypress-io/cypress.git
cd cypress
git checkout 10.0-release
yarn install
yarn cypress:open --project ../create-nested-components --component
```

Finally:

- start component testing with chrome
- create the first spec file from post.js

`Error [ERR_IPC_CHANNEL_CLOSED]: Channel closed`

## How was this repo created?

```sh
yarn create next-app --example --example nested-components create-nested-components
cd create-nested-components
yarn add -D @cypress/react @cypress/webpack-dev-server
```