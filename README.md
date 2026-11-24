# React Developer Quick Start

## Create a project

Install [Node.js](https://nodejs.org/), then run:

```bash
npm create vite@latest my-react-app -- --template react
cd my-react-app
npm install
npm run dev
```

Open the local URL shown in the terminal. For a TypeScript starter, use `react-ts` instead of `react`.

## Create components

A React component is a JavaScript function that returns JSX. Component names begin with a capital letter. Use props to pass data in:

```jsx
function Greeting({ name }) {
	return <h1>Hello, {name}!</h1>;
}

export default function App() {
	return <Greeting name="React developer" />;
}
```

## Add interactivity

Use state for values that change over time. For example, `useState` keeps a counter value and updates it when the button is clicked:

```jsx
import { useState } from 'react';

function Counter() {
	const [count, setCount] = useState(0);
	return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

Call Hooks such as `useState` at the top level of a component, not inside conditions or loops.

## JSX basics

- Use `{expression}` to include JavaScript expressions.
- Use `className` rather than `class` for CSS classes.
- Return one parent element, or wrap siblings in a fragment (`<>...</>`).
- Render collections with `.map()` and give each item a stable `key`.

## Run and build

Vite projects commonly provide these commands:

```bash
npm run dev      # Start the development server
npm run build    # Create a production build
npm run preview  # Preview the production build locally
```

Keep components focused and reusable. Check `package.json` for the scripts available in your project.
