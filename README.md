# Wolfram | Beta

Source code available publicly at [Codeberg](https://codeberg.org/woflydev/wolfram-beta/).

A Node.js package that uses [Puppeteer](https://pptr.dev) to grab step-by-step solutions from [Wolfram | Alpha®](https://www.wolframalpha.com) queries directly in your terminal (with HTML support) without needing an API key. **Wolfram | Beta** provides a command-line interface to input queries, fetch and parse data from Wolfram | Alpha®, and is fully hackable for future adaptation!

Jump to [Usage on Codeberg](https://codeberg.org/woflydev/wolfram-beta/#usage). Alternatively, [stay on Github](#usage).

## Intent

This project aims to merely serve as an educational demonstration of extending the capabalities of an existing service to the terminal environment.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [More Info](#more-info)

## Installation

### From Source
Make sure you have `yarn` or `npm`. Project was built in Node v18 but should be back compatible.

Clone the repository:
```bash
git clone https://codeberg.org/woflydev/wolfram-beta.git
cd wolfram-beta
yarn
```

### From NPM
Simply install globally via the package manager of your choice:
```bash
npm i wolfram-beta -g
```

## Usage
Run the script with the desired options to query Wolfram Alpha and display the results in the terminal.

```bash
yarn start [options]
```

or

```bash
wolfram-beta [options]
```

## How It Works

The package leverages Puppeteer to launch a headless browser instance, essentially 'piggybacking' off of the wonderful work of contributors over at [Wolfree | Alpha](https://codeberg.org/wolfree) to provide step-by-step solutions. The resulting JSON is scraped with CSS selectors and contains answer results which are parsed and sorted.

## More Info

Check the main repository at [Codeberg](https://codeberg.org/woflydev/wolfram-beta) for stuff regarding contributing and other info.
