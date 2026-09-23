# Pokémon Trivia Game

A small Pokémon trivia game built with **Vue 3**, **TypeScript**, **Vite**, and **Tailwind CSS**.

The main goal of this project is to put into practice fundamental Vue concepts such as component communication, conditional rendering, composables, props, emits, and TypeScript integration.

The application presents a Pokémon and challenges the player to identify the correct answer from the available options.

## Live Demo

The application is deployed on Netlify and can be tested here:

[View Live Demo](https://pokemon-trivia-game.netlify.app/)

## Technologies Used

- Vue 3
- TypeScript
- Vite
- Tailwind CSS
- Axios
- Vitest
- Vue Test Utils
- ESLint
- Oxlint
- Prettier
- Canvas Confetti

## Concepts Covered

This project was developed as a practical exercise to reinforce several Vue and TypeScript concepts.

### Conditional Rendering

Vue conditional rendering is used to dynamically display different parts of the interface depending on the current state of the game.

This includes showing or hiding elements based on conditions and updating the UI as the player interacts with the application.

### Props

Props are used to pass data from parent components to child components.

This allows components to receive the information they need while keeping them reusable and independent.

### Emits

Custom events are emitted from child components to communicate actions back to their parent components.

This pattern is used to keep component responsibilities separated while maintaining communication between different parts of the application.

### Composables

Reusable application logic is extracted into Vue composables.

Composables help separate business logic from the UI and make functionality easier to maintain and reuse across components.

### TypeScript Interfaces

Interfaces are used to define the structure of objects and API data.

This provides better type safety, improves editor support, and helps prevent errors when working with structured data.

### TypeScript Enums

Enumerations are used to represent predefined sets of values in a type-safe way.

They help make the code more readable and avoid relying on arbitrary strings or numeric values throughout the application.

### Tailwind CSS

Tailwind CSS is used to build and style the user interface using utility classes.

It allows the application layout and visual states to be created directly from the component templates while maintaining a consistent design.

## API Requests

The project uses **Axios** to perform HTTP requests and retrieve the data required by the game.

The retrieved information is then processed by the application and displayed through Vue components.

## Project Setup

### Requirements

Before installing the project, make sure you have Node.js installed.

The project requires:

```text
Node.js ^20.19.0 or >=22.12.0
```

You can verify your installed version with:

```sh
node --version
```

### Clone the Repository

Clone the repository and navigate to the project directory:

```sh
git clone https://github.com/trejoscr/vue-pokemon-trivia-game.git

cd pokemon-game
```

### Install Dependencies

```sh
npm install
```

## Development

Start the Vite development server:

```sh
npm run dev
```

Vite will display the local URL where the application is running, typically:

```text
http://localhost:5173/
```

## Production Build

Run the TypeScript type checking process and create an optimized production build:

```sh
npm run build
```

The generated production files will be available in the `dist` directory.

## Preview Production Build

To locally preview the production build:

```sh
npm run preview
```

## Unit Tests

The project uses **Vitest** and **Vue Test Utils** for unit testing.

Run the tests with:

```sh
npm run test:unit
```

## Linting

The project uses **ESLint** and **Oxlint** for static code analysis.

Run the configured linters with:

```sh
npm run lint
```

## Code Formatting

The project uses **Prettier** for code formatting.

Format the source files with:

```sh
npm run format
```

## Available Scripts

| Command              | Description                                             |
| -------------------- | ------------------------------------------------------- |
| `npm run dev`        | Starts the Vite development server                      |
| `npm run build`      | Type-checks and builds the application for production   |
| `npm run build-only` | Builds the application without running the type checker |
| `npm run preview`    | Previews the production build locally                   |
| `npm run test:unit`  | Runs unit tests with Vitest                             |
| `npm run type-check` | Runs TypeScript type checking with `vue-tsc`            |
| `npm run lint`       | Runs the configured linters                             |
| `npm run format`     | Formats source files with Prettier                      |

## Purpose of the Project

This project was created as a practical exercise to consolidate the Vue concepts learned so far by applying them to a small interactive game.

The project focuses on component-based development, communication between components, reusable logic, TypeScript type safety, API integration, conditional UI states, and styling with Tailwind CSS.
