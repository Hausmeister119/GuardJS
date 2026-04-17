#GuardJS
GuardJS is a lightweight Runtime Safety Engine for JavaScript and TypeScript applications.

Instead of only validating data, GuardJS focuses on:
- detecting invalid runtime data
- automatically repairing unsafe values (where possible)
- providing safe fallbacks
- optionally logging and tracking data issues

The goal is to reduce crashes caused by unexpected input in real-world applications.

## Key Features
- Runtime type safety (string, number, object, array)
- Automatic data repair (e.g. "42" → 42)
- Safe fallback values
- Schema-based validation
- Zero dependency core
- Works in Node.js and browser environments

## Philosophy
"Don’t just validate data — make it safe to use."

## Example
```ts
import { guard } from "guardjs"

const age = guard.number(inputAge, {
  min: 0,
  max: 120,
  fallback: 18
})
