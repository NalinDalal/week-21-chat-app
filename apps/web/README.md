This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load Inter, a custom Google Font.

## Chat App

We are using a monorepo next.js part for a chat app
introduce 2 more repos http-server, ws-server

apps/web/app/page.tsx; introduced a ui folder in packages so that the buttons, and all other things are generalised

update ui/package.json so that there is some efficiency in collecting the other
things, basically allowing me to use benefits of turbo repo

create a input textbox and initial chat page, initiate a package.json in ui and
add all the u know things like @ to export and import

### BackEnd

go to http-server and initialise express and ts; same for ws-server
initialise http-server routes, create cmd for running, building, specify build
step and dev step in package.json

1. Initialised a monorepo
2. We learned how to create a design system/ re-use/import things from a 'ui' module.
3. We learnt about "exports" in package.json
4. We created a vary minimal frontend for our chat app
   imported tsconfig from ws into http, hence it thought about ws so create a
   solutin by extends in http-server

```json
"extends": "@repo/typescript-config/backends.json"
```

5. introduce prisma in packages/db
   note: we need to cache backends also, caches only src not dist folder

6. server ki turbo.json add dist as output to store

7. add a turbo.json in a react cause it is dist(html,css,js file); default says `.next`; so it different
   run command: `npm run build`
