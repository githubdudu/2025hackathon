# TypeScript Optional Configuration

This project has been configured to make TypeScript optional, allowing you to use both JavaScript and TypeScript files seamlessly.

## Key Changes Made

### 1. ESLint Configuration (`.eslintrc`)
- Moved TypeScript-specific rules to `overrides` section
- Only applies TypeScript rules to `.ts` and `.tsx` files
- JavaScript files are linted with standard ESLint rules

### 2. TypeScript Configuration (`tsconfig.json`)
- `strict: false` - Disables strict type checking
- `noImplicitAny: false` - Allows implicit any types
- `checkJs: false` - Doesn't type-check JavaScript files
- `allowJs: true` - Allows importing JavaScript files

### 3. Build Scripts (`package.json`)
- `npm run build` - Builds without TypeScript compilation
- `npm run build:ts` - Builds with TypeScript type checking

## Usage Guidelines

### For JavaScript Files
- Use `.js` for regular JavaScript
- Use `.jsx` for React components
- No type annotations required
- Standard ESLint rules apply

### For TypeScript Files
- Use `.ts` for TypeScript files
- Use `.tsx` for TypeScript React components
- Type annotations are optional but recommended
- Additional TypeScript-specific ESLint rules apply

### Migration Strategy
1. Start with JavaScript files (`.js/.jsx`)
2. Gradually migrate to TypeScript (`.ts/.tsx`) when needed
3. Add type annotations incrementally
4. Use `npm run typecheck` to verify TypeScript files

## Example Files
- `src/components/ExampleJSComponent.jsx` - JavaScript React component
- `src/components/ExampleTSComponent.tsx` - TypeScript React component

Both types of files can coexist and import each other seamlessly.
