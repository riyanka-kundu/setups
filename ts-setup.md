# TypeScript Project Setup Guide

Follow these steps to set up a TypeScript project with pnpm:

## 1. Initialize the Project

Run the following command to initialize the project:

```bash
pnpm init
```

## 2. Install Dependencies

Run the following command to install the required dependencies:

```bash
pnpm add -D typescript tsx
```

## 3. Initialize TypeScript Configuration

Run the following command to initialize `tsconfig.json`:

```bash
pnpm tsc --init
```

## 4. Configure TypeScript

Paste the following configuration into `tsconfig.json`:

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "ESNext",
    "outDir": "./dist",
    "strict": true,
    "declaration": false,
    "sourceMap": false,
    "verbatimModuleSyntax": false
  },
  "include": ["src"]
}
```

## 5. Add Scripts to package.json

Add the following scripts to your `package.json`:

```json
"scripts": {
  "dev": "tsx src/main.ts",
  "build": "tsc",
  "start": "node dist/main.js"
}
```

## Usage

- **Development Server**:
  Run the following command

```bash
pnpm dev
```

to start the development server

- **Build the project**:
  Run the following command

  ```bash
  pnpm build
  ```

  to build the project

- **Production server**:
  Run the following command
  ```bash
  pnpm start
  ```
  to start the production build

## Run standalone files

### Using tsx

Run the following command to run a standalone file:

```bash
pnpm tsx src/main.ts
```

### Using node and tsc

Run the following command to run a standalone file:

```bash
pnpm tsc && node dist/main.js
```
###Install pnpm once globally
```bash
npm install -g pnpm

