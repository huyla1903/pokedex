# Pokédex CLI

An interactive command-line Pokédex built with TypeScript and Node.js. It uses
the [PokéAPI](https://pokeapi.co/) to explore location areas, encounter Pokémon,
and collect them in an in-memory Pokédex.

## Features

- Browse forward and backward through PokéAPI location areas
- Explore an area to discover its Pokémon
- Catch Pokémon with odds based on their base experience
- Inspect the stats and types of caught Pokémon
- List every Pokémon caught during the current session
- Cache API responses in memory with automatic expiration

## Requirements

- Node.js 22 (the repository includes an `.nvmrc`)
- npm

## Getting Started

```bash
git clone https://github.com/huyla1903/pokedex.git
cd pokedex
nvm use
npm install
npm run dev
```

If the requested Node.js version is not installed, run `nvm install` first.

## Commands

| Command | Description |
| --- | --- |
| `help` | Display all available commands |
| `map` | Show the next page of location areas |
| `mapb` | Show the previous page of location areas |
| `explore <location_name>` | List the Pokémon found in an area |
| `catch <pokemon_name>` | Attempt to catch a Pokémon |
| `inspect <pokemon_name>` | View details about a caught Pokémon |
| `pokedex` | List all caught Pokémon |
| `exit` | Close the application |

Example:

```text
Pokedex > explore pastoria-city-area
Exploring pastoria-city-area...
Found Pokemon:
 - tentacool
 - tentacruel
 - magikarp

Pokedex > catch caterpie
Throwing a Pokeball at caterpie...
caterpie was caught!
You may now inspect it with the inspect command.

Pokedex > pokedex
Your Pokedex:
 - caterpie
```

The Pokédex is stored in memory, so caught Pokémon are reset when the program
exits.

## Development

Build the TypeScript source:

```bash
npm run build
```

Run the test suite:

```bash
npm test
```

Run the compiled application:

```bash
npm start
```

## Tech Stack

- TypeScript
- Node.js
- Vitest
- PokéAPI
