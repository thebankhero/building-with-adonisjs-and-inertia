# Building with AdonisJS &amp; Inertia

## Project Setup
```code
npm init adonisjs@latest building-with-adonisjs-and-inertia
```

- Inertia Starter Kit
- Sessions
- PostgreSQL
- Vue 3
- SSR true

### TailwindCSS
npm i -D tailwindcss@3 autoprefixer

### Shadcn-Vue
- https://shadcn-vue.com/docs/installation.html

```code
npx shadcn-vue@radix init
```
- TypeScript > yes
- framework > Vite
- style > Default
- base color > Slate
- tsconfig.json > ./inertia/tsconfig.json
- global CSS > ./inertia/css/app.css
- CSS variables > yes
- tailwind.config > tailwind.config
- components > ~/components
- utils > ~/lib/utils
- components.json > Y

#### ลบ array ภายใน content ของไฟล์ tailwind.config.js และเพิ่มข้อมูลดังต่อไปนี้
- './inertia/{pages,components,app,layouts}/**/*.{ts,tsx,vue}',
- './resources/views/**/*.edge'

#### edit module.exports
- >>del module.exports = {}
- >>add export default {}

#### change require to import
- >>del const animate = require("tailwindcss-animate")
- >>add import animate from 'tailwindcss-animate'

### Shadcn-Vue Components
```code
npx shadcn-vue@radix add button
```

## Middleware
```code
node ace make:middleware share_example
```

## SVG Icon
https://lucide.dev/
