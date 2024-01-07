## React env setup for 2024

1. node -v(volta list)
2. npm create vite@latest smaple-app -- --template react-swc-ts
3. npm run dev, build, preview
4. tsconfig.json

```json
"compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@/*": ["src/*"]
    }
  },
```

5. npm i -D vite-tsconfig-paths (これで vite.config.ts は編集する必要なし)
6. vite.config.ts

```ts
import react from "@vitejs/plugin-react-swc";
import { defineConfig } from "vite";
import tsconfigPaths from "vite-tsconfig-paths";

export default defineConfig({
  plugins: [react(), tsconfigPaths()],
});
```
7. vitest or testing-libray or jest
8. 