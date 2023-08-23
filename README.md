# Wolfram | Beta

Source code available publicly at [Codeberg](https://codeberg.org/woflydev/wolfram-beta/).

A Node.js package that uses [Puppeteer](https://pptr.dev) to grab step-by-step solutions from [Wolfram | Alpha®](https://www.wolframalpha.com) queries directly in your terminal (with HTML support) without needing an API key. **Wolfram | Beta** provides a command-line interface to input queries, fetch and parse data from Wolfram | Alpha®, and is fully hackable for future adaptation!

Jump to [Usage](#usage).

## Intent

This project aims to merely serve as an educational demonstration of extending the capabalities of an existing service to the terminal environment.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

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
npm i wolfree-beta -g
```

## Usage
Run the script with the desired options to query Wolfram Alpha and display the results in the terminal.

```bash
yarn start [options]
```

or

```bash
wolfree-beta [options]
```

Alternatively, you can quickly launch specific flags (repo clone only).

```bash
yarn dev [options] # launches with -d
yarn help [options] # launches with -h and exits
yarn test [options] # launches with -t and uses default input
```

Available options:

- `-d, --dev`: Show technical information JSON for debugging.
- `-s, --source`: Show source information of the query.
- `-o, --open`: Open the generated HTML file in the default browser.

### Example
```bash
> node wolfree-beta
$ What do you want to calculate or know about?
> population of spain
$
$ processing...
$ Query Result Information:
$
$ Input interpretation
$ Spain | population
$
$ Result
$ 47.5 million people (world rank: 32nd) (2023 estimate)
$ Image(s) Found!
$ https://www6b3.wolframalpha.com/Calculate/MSP/MSP13381208dc8g4d56degb0000627c66d4a46301hf?MSPStoreType=image/gif&s=4
$
$ ...(there's more)
```

The best part? It formats it all nicely with colours and headings, to make it easier to read. It also outputs all of the parsed content (including images) to an HTML file in the same directory, which would be better for viewing multiple plots in one go. The HTML file is **always generated** but you can pass in the `-o` flag to open it automatically on completion.

## How It Works

The package leverages Puppeteer to launch a headless browser instance, essentially 'piggybacking' off of the wonderful work of contributors over at [Wolfree | Alpha](https://codeberg.org/wolfree) to provide step-by-step solutions. The resulting JSON is scraped with CSS selectors and contains answer results which are parsed and sorted.

## Contributing

Contributions are more than welcome! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.

1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-name`
3. Make your changes and commit them: `git commit -m 'some feature or fix'`
4. Push the changes to your fork: `git push origin feature-name`
5. Submit a pull request.

## License

Do whatever you want with it under GPL-v3.
