# React + TypeScript + Vite + Shadcn UI

This is a React Typescript Project with Shadcn UI.

## Steps to Setup

1. Setup the React Project with `npm create vite@latest`.
2. Install depencies for tailwindcss `npm install -d tailwindcss postcss autoprefixer` and init the tailwindcss `npx tailwindcss init -p`.
3. Add the following file in tsconfig.json

```js
{
  "compilerOptions": {
    // ...
    "baseUrl": ".",
    "paths": {
      "@/*": [
        "./src/*"
      ]
    }
    // ...
  }
}

```

4. Update the vite.config.ts

```js
npm i -D @types/node
```

```js
import path from "path";
import react from "@vitejs/plugin-react";
import { defineConfig } from "vite";

export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  },
});
```

5. Run the `shadcn-ui` init command

   ```js
   npx shadcn-ui@latest init
   ```

6. You can now start adding components to your project.

```js
npx shadcn-ui@latest add button
```

```js
import { Button } from "@/components/ui/button";

export default function Home() {
  return (
    <div>
      <Button>Click me</Button>
    </div>
  );
}
```
