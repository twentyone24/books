---

<div align="center" markdown="1">

---

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/frappe/books)](https://github.com/frappe/books/releases)
![Platforms](https://img.shields.io/badge/platform-mac%2C%20windows%2C%20linux-yellowgreen)
[![Publish](https://github.com/frappe/books/actions/workflows/publish.yml/badge.svg)](https://github.com/frappe/books/actions/workflows/publish.yml)

<img src="https://user-images.githubusercontent.com/29507195/207267857-4ae48890-3fb2-4046-80cf-3256b46c72a0.png" alt="Frappe Books Preview"/>

</div>

## Index

<details>
<summary><code>[show/hide]</code></summary>

1. [Features](#features)
2. [Installation](#installation)
3. [Development](#development)
4. [Contributions and Community](#contributions-and-community)
5. [Links](#links)
6. [Translation Contributors](#translation-contributors)
7. [License](#license)

</details>

## Features

1. Double-entry accounting
1. Invoicing
1. Billing
1. Payments
1. Journal Entries
1. Dashboard
1. Works Offline
1. Financial Reports
   - General Ledger
   - Profit and Loss Statement
   - Balance Sheet
   - Trial Balance

## Installation

Download and install the latest release for your platform from the [releases
page](https://github.com/frappe/books/releases) or the [download
page](https://frappebooks.com/download).

## Development

Frappe Books is built on Vue.js and Electron. It is offline by default and uses
a local SQLite file as the database.

### Pre-requisites

To get the dev environment up and running you need to first set up Node.js version
16.14.0 and npm. For this, we suggest using
[nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

Next, you will need to install [yarn](https://classic.yarnpkg.com/lang/en/docs/install/#mac-stable).

### Clone and Run

Once you are through the Pre-requisites, you can run the following commands to
setup Frappe Books for development and building:

```bash
# clone the repository
git clone https://github.com/frappe/books.git

# change directory
cd books

# install dependencies
yarn
```

#### Development

To run Frappe Books in development mode (with hot reload, etc):

```bash
# start the electron app
yarn dev
```

**Note: First Boot**

When you run `yarn dev` electron will run immediately but the UI will take a
couple of seconds to render this because of how dev mode works. Each file is
individually served by the dev server. And there are many files that have to be
sent.

**Note: Debug Electron Main Process**

When in dev mode electron runs with the `--inspect` flag which allows an
external debugger to connect to port 5858. You can use chrome for this by
visiting `chrome://inspect` while Frappe Books is running in dev mode.

See more [here](https://www.electronjs.org/docs/latest/tutorial/debugging-main-process#external-debuggers).

#### Build

To build Frappe Books and create an installer:

```bash
# start the electron app
yarn build
```

**Note: Build Target**
By default the above command will build for your computer's operating system and
architecture. To build for other environments (example: for linux from a windows
computer) check the _Building_ section at
[electron.build/cli](https://www.electron.build/cli).

So to build for linux you could use the `--linux` flag like so: `yarn build --linux`.

## Contributions and Community

If you want to contribute to Frappe Books, please check our [Contribution Guidelines](https://github.com/frappe/books/blob/master/.github/CONTRIBUTING.md). There are many ways you can contribute even if you don't code:

1. If you find any issues, no matter how small (even typos), you can [raise an issue](https://github.com/frappe/books/issues/new) to inform us.
2. You can help us with language support by [contributing translations](https://github.com/frappe/books/wiki/Contributing-Translations).
3. You can join our [telegram group](https://t.me/frappebooks) and share your thoughts.
4. If you're an ardent user you can tell us what you would like to see.
5. If you have accounting requirements, you can become an ardent user. 🙂

If you want to contribute code then you can fork this repo, make changes and raise a PR. ([see how to](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork))

## License

[GNU Affero General Public License v3.0](LICENSE)
