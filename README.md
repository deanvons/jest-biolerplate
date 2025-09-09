# jest‑boilerplate

A minimal boilerplate template for setting up Jest testing with TypeScript (and optional Babel support).

##  Features

- TypeScript support for structuring your test files.
- Babel configuration (`babel.config.js`) for advanced transpilation needs.
- Preconfigured `package.json` with essential dependencies and scripts.
- Ready-to-run testing environment with Jest.

##  Getting Started

### Prerequisites

Ensure you have Node.js (v14+) and npm installed.

### Installation

```bash
git clone https://github.com/deanvons/jest-biolerplate.git
cd jest-biolerplate
npm install
```

### Running Tests

```bash
npm test
```

### Watching Tests

```bash
npm test:watch
```

### Test Coverage

```bash
npm run test:coverage
```

##  Suggested Scripts

In your `package.json`, you might add or adapt:

```jsonc
"scripts": {
  "test": "jest",
  "test:watch": "jest --watch",
  "test:coverage": "jest --coverage"
}
```

##  Configuration Files

- **`babel.config.js`** – Babel setup for transforming modern JavaScript/TypeScript during testing.
- **`jest.config.js`** (optional) – Consider adding this file to customize Jest behavior (e.g., handling `.ts` files via `ts-jest` or Babel, coverage thresholds, test environment).
- **`.gitignore`** – File to exclude `node_modules`, logs, and coverage output from version control.

##  Usage Example

Create a sample test in `sum.test.ts`:

```ts
// sum.ts
export function sum(a: number, b: number): number {
  return a + b;
}

// sum.test.ts
import { sum } from './sum';

describe('sum()', () => {
  it('adds two numbers correctly', () => {
    expect(sum(1, 2)).toBe(3);
  });
});
```

Then run:

```bash
npm test
```

You should see a successful test indication from Jest.

##  Recommendations / Next Steps

Depending on your needs, consider enhancing this boilerplate with:

- **TypeScript Integration** – Install `ts-jest` and optionally `@types/jest` for pure TS testing.
- **Linting** – Add ESLint + Prettier for maintaining code quality and formatting.
- **Pre-commit Hooks** – Use Husky to run linting or tests before commits.
- **Coverage Enforcement** – Enforce minimum code coverage thresholds via Jest configuration.
- **Custom Jest Config** – Add `jest.config.js` to manage path aliases, module mappings, and test environments.

##  Contribution

Contributions, issue reports, and feature requests are welcome! Please open issues or pull requests on the repo.
