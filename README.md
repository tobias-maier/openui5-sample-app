# Sample ui5 app
Dieses repo ist ein fork von https://github.com/SAP/openui5-sample-app

## Voraussetzungen
- Zum Bauen und Starten wird die **UI5 CLI (Command Line interface)** von [UI5 Tooling](https://github.com/SAP/ui5-tooling#installing-the-ui5-cli) verwendet.
- **IDE**: Visual Studio Code

**Installation**: 
- Installiere *node.js* in der Version 10 oder höher
- Installiere die *ui5 cli*:
    ```
    # Global installation to have the command available
    npm install --global @ui5/cli

    # Additional local install in your project
    npm install --save-dev @ui5/cli

    # Verify installation
    ui5 --help
    ```
- Clone das Repository:
    ```
    git clone https://github.com/tobias-maier/openui5-sample-app
    cd open-ui5-sample-app
    ```
- Installiere alle Abhängigkeiten:
    ```
    npm install
    ```
- Starte einen lokalen Server (http://localhost:8080/index.html)
    ```
    ui5 serve -o index.html
    ```

## Testing
* Run [ESLint](https://eslint.org/) code validation
    ```sh
    npm run lint
    ```
* Start the [Karma Test Runner](https://karma-runner.github.io/latest/index.html) with the [UI5 Plugin](https://github.com/SAP/karma-ui5) and execute the tests automatically after every change
    ```sh
    npm run watch
    ```
* Run both ESLint and Karma in CI mode
    ```sh
    npm test
    ```
## Building
### Option 1: Standard preload build
- Führe folgende build Anwweisung aus
    ```sh
    ui5 build -a
    ```
- Run the result
    1. Run a local HTTP server on the build results (`/dist` directory)  
	(**Note:** This script is using the [local-web-server](https://www.npmjs.com/package/local-web-server) npm module, but you can use any HTTP server for that)
        ```sh
        npm run serve-dist
        ```
    1. Open the app at http://localhost:8000

