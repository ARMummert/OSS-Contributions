_FreeCodeCamp Issue - Build Documentation for Commands within the FreeCodeCamp project.  I completed this issue as part of Oregon State
University for CS 464.  This issue was closed while I completed this documentation so there was no pull request. My contribution
starts at `challenge-editor:server`_
# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command: `audit-challenges`

The `audit-challenges` command is used to ensure the integrity and correctness of the challenges within the project. It consists of two distinct steps:

1. **Configuration Setup**: The command starts by setting up the project's configuration using the `ppm` (or package manager) tool with the argument `Tun create:config`. This step ensures that the necessary configuration settings are established for the auditing process.

2. **Challenge Auditing**: After the configuration setup, the command utilizes the `ts-node` TypeScript execution environment to run a specific TypeScript script located at `tools/challenge-auditor/index.ts`. This script is responsible for thoroughly auditing the challenges within the project. It likely analyzes challenge-related data, identifies potential issues, and generates reports to ensure that challenges are functioning correctly.

**Usage:**

To execute the `audit-challenges` command, follow these steps:

```bash
npm run audit-challenges

```

## Command: `analyze-bundle`

The `analyze-bundle` command allows you to analyze the webpack bundle of the project using the "webpack-bundle-analyzer" tool. This tool provides valuable insights into the composition and size of the bundle, enabling you to optimize and better understand your project's frontend asset distribution.

**Usage:**

To utilize the `analyze-bundle` command, follow these steps:

```bash
npm run analyze-bundle
```

## Command: `prebuild`

The `prebuild` command is executed automatically before the actual build process begins. It is responsible for performing certain preparatory steps or tasks to ensure a smooth and successful build. In this specific case, the command executes the `npm-run-all` tool with the argument `create`.

**Usage:**

The `prebuild` command is invoked automatically before the build process. Therefore, you do not need to run it explicitly. It is configured to perform necessary setup or preparation that is essential for the subsequent build steps.


## Command: `build`

The `build` command is a key step in the project's development workflow. It is used to trigger the build process, which compiles, bundles, and prepares the project's source code for deployment or distribution.

**Usage:**

To initiate the build process, execute the following command:

```bash
npm run build

```

## Command: `build workers`

The `build workers` command is used to trigger the build process specifically for the workers in the project. Workers are components or modules designed to perform background tasks or parallel processing.

**Usage:**

To initiate the build process for workers, execute the following command:

```bash
cd ./client && pnpm run prebuild
```

## Command: `build:client`

The `build:client` command is used to initiate the build process specifically for the client-side of the project. This process involves compiling, bundling, and preparing the client code for deployment or distribution.

**Usage:**

To start the client build process, execute the following command:

```bash
cd ./client && pnpm run build
```

## Command: `build:curriculum`

The `build:curriculum` command is used to initiate the build process specifically for the curriculum section of the project. This process involves compiling, bundling, and preparing the curriculum-related content for deployment or distribution.

**Usage:**

To start the curriculum build process, execute the following command:

```bash
cd ./curriculum && pnpm run build
```

## Command: `build:server`

The `build:server` command is used to initiate the build process specifically for the server-side of the project. This process involves compiling, bundling, and preparing the server code for deployment or distribution.

**Usage:**

To start the server build process, execute the following command:

```bash
cd /api-server && pnpm run build
```
# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command: `challenge-editor`

The `challenge-editor` command is used to manage and interact with the challenge editor component of the project. This command likely orchestrates various tasks related to editing challenges, including user interface setup, configuration, and interactive functionality.

**Usage:**

To utilize the `challenge-editor` command, execute the following command:

```bash
npm-run-all -p challenge-editor:*

```

## Command: `challenge-editor: server`    

The `challenge-editor:server` is used to interact with the challenge editor server component of this project.  

**Usage:**

To utilize the `challenge-editor:server` command, execute the following command:

`cd ./tools/challenge-editor/api`

```bash
pnpm start
```
## Command: `challenge-editor: client`

The `challenge-editor: client` is used to interact with the challenge editor client component of this project.

**Usage:**

`cd ./tools/challenge-editor/client`

```bash
pnpm start
```
# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command: `clean`

The `clean` command cleans the cache of a specified component.  

**Usage:**

```bash
npm-run-all -p clean:client clean:server clean:curriculum --serial clean:packages
```

## Command: `clean-and-develop`

The `clean-and-develop` command cleans the cache and then runs the development server

**Usage:**

```bash
pnpm run clean && pnpm install && pnpm run develop
```

## Command: `clean:api`

The `clean:api` command cleans the api cache

**Usage:**

`cd ./api`

```bash
pmpn clean
```

## Command `clean:client`

The `clean:client` command cleans the client cache

**Usage:**

`cd ./client`

```bash
pmpn run clean
```

## Command `clean:curriculum`

The `clean:curriculum` command cleans the curriculum cache

**Usage:**

```bash
rm -rf ./config/curriculum/json
```

## Command `clean:packages`

The `clean:packages` command cleans the packages cache

**Usage:**

```bash
rm -rf ./node_modules ./**/node_modules
```

## Command `clean:server`

The `clean:server` command cleans the server cache

**Usage:**

```bash
rm -rf ./api-server/lib
```

#  Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `create:config`

The `create:config` command creates a config file

**Usage:**

```bash
tsc -p config && pnpm run ensure-env && pnpm run download-trending
```

## Command `create:utils`

The `create:utils` command creates command line utilities

**Usage:**

```bash
tsc -p utils
```

# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `precypress`

The `precypress` command pre-installs cypress front end testing environment

**Usage:**

```bash
node ./cypress-install.js
```

## Command `cypress:dev:run`

The `cypress:dev:run` command runs cypress testing environment in dev mode

**Usage:**

```bash
pnpm run cypress run
```


## Command `cypress:dev:watch`

The `cypress:dev:watch` command opens cypress testing environment in watch mode

**Usage:**

```bash
pnpm run cypress open
```


## Command `cypress:install-build-tools`

The `cypress:install-dev-tools` command installs cypress testing environment developer tools

**Usage:**

```bash
sh ./cypress-install.sh
```

# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `predevelop`

The `predevelop` command creates a build:cirruculum environment

**Usage:**

```bash
npm run all -p create:* -s build:cirruculum
```

## Command `develop`

The `develop` command runs developer mode

**Usage:**

```bash
npm run all -p develop:** 
```

## Command `develop:client`

The `develop:client` command runs the client in developer mode

**Usage:**

```bash
cd ./client && pnpm run develop
```

## Command `develop:server`

The `develop:server` command runs the server in developer mode

**Usage:**

```bash
cd ./api-server && pnpm run develop
```

## Command `docs:server`

The `docs:server` servers the documents via docsify

**Usage:**

```bash
docisfy serve ./docs -o --port 3400
```

# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `e2e`

The `e2e` command runs end to end testing on the project

**Usage:**

```bash
pnpm run  e2e:dev:run
```

## Command `e2e:dev:run`

The `e2e:dev:run` command starts tests in developer mode running `cypress:dev:run`

**Usage:**

```bash
start-test develop 'localhost:3000/status/ping|localhost:8000' cypress:dev:run
```

## Command `e2e:dev:watch`

The `e2e:dev:watch` command starts tests in developer mode running `cypress:dev:watch`

**Usage:**

```bash
start-test develop 'localhost:3000/status/ping|localhost:8000' cypress:dev:watch
```

## Command `e2e:prd:run`

The `e2e:prd:run` command starts tests in production mode running `cypress:dev:run`

**Usage:**

```bash
pnpm run build && start-test 'localhost:3000/status/ping|localhost:8000' cypress:dev:run
```

## Command `e2e:prd:watch`

The `e2e:prd:run` command starts tests in production mode running `cypress:dev:watch`

**Usage:**

```bash
pnpm run build && start-test 'localhost:3000/status/ping|localhost:8000' cypress:dev:watch
```

# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `download-trending`

The `download-trending` command writes trending downloads to a file

**Usage:**

```bash
ts-node ./tools/scripts/build/download-trending.ts
```

## Command `ensure-env`

The `ensure-env` command ensures that the required env variables are set

**Usage:**

```bash
cross-env DEBUG=fcc:* ts-node ./tools/scripts/build/ensure-env.ts
```

# Command Documentation

This document provides detailed information about the available commands in the project and how to use them effectively. Clear documentation for these commands is essential for enabling contributors to understand their functionalities and contribute more effectively.

## Command `format`

The `format` command formats both the eslinter and uses prettier as a code formatter 

**Usage:**

```bash
run -s format:eslint format:prettier
```

## Command `format:curriculum`

The `format:cirriculum` formats the cirriculum with both the eslinter and uses prettier as a code formatter 

**Usage:**

```bash
run -s format:curriculum:eslint format:curriculum:prettier
```

## Command `format:curriculum:eslint`

The `format:cirriculum:eslint` formats the cirriculum the eslinter and fixes linting errors

**Usage:**

```bash
eslint ./curriculum --fix
```

## Command `format:curriculum:prettier`

The `format:cirriculum:prettier` formats the cirriculum prettier and writes prettier code

**Usage:**

```bash
prettier --write ./curriculum
```

## Command `format:eslint`

The `format:eslint` formats with the eslinter removing linting errors 

**Usage:**

```bash
eslint --fix
```

## Command `format:prettier`

The `format:prettier` formats with prettier and writes prettier code

**Usage:**

```bash
prettier --write
```

## Command `knip`

The `knip` finds unused files

**Usage:**

```bash
pnpm d1x knip@1 --include files
```