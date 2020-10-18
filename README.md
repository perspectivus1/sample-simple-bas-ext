# sample-simple-bas-ext

This repo contains a SAP Business Application Studio (BAS) sample simple extension.

It demonstrates how to load a custom vscode extension (`.vsix`) into your dev spaces.

## Deploying this simple sample BAS extension
1. Create a **Basic** SAP Business Development Studio dev space.
1. From within the `~/projects` folder of your dev space, clone [this repository](https://github.com/perspectivus1/sample-simple-bas-ext).
1. From within the `~/projects/sample-simple-bas-ext/bas-ext` folder, run `npm i`. This installs the lastest version of the `wex` tool that you'll use to deploy your extension.
1. Update the `extension.json`file as needed. For example, the `namespace` property should be based on your SAP Cloud Platform subaccount's subdomain (`ext-<subdomain>`). Ask your admin for this info.
1. Run `npm run deployExt` to deploy your extension.
1. Create another SAP Business Development Studio dev space:
    * This time check the `sample-simple-bas-ext` extension.
1. Open your new dev space.
1. Press `F1` or `ctrl+p` to run the `Hello BAS` command.
## Publishing your own vscode extension
In this example, we made our `.vsix` file available as a [GitHub release](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/about-releases) asset.

If you wish to make your own vscode extension available to the BAS simple extension mechanism, you can create your own GitHub repo or fork this one, and upload your `.vsix` as an asset to your forked repo.

The `vscdoe-ext` folder contains an example of a very simple vscode extension.
