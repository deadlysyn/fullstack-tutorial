# fullstack-tutorial

Artifacts from https://youtu.be/I6ypD7qv3Z8

# Dev Setup

```console
npm init -y
npm i -D @types/node typescript ts-node nodemon
# see package.json for scripts to configure...
create `src/index.ts` with `console.log('hello world')` to test
npx tsconfig.json (package with starter typescript config)
npm start # run index.ts directly
npm run watch # compile typescript to `dist`
node dist/index.js # run compiled javascript directly
```

# Dependencies

```console
npm i @mikro-orm/cli @mikro-orm/core @mikro-orm/migrations
npm i @mikro-orm/postgresql pg # or mysql, mongo, etc...
# development only...
mkdir -p pgdata && docker run --rm -d \
    --name postgres \
    -p 5432:5432 \
    -e POSTGRES_PASSWORD=postgres \
    -e PGDATA=./pgdata \
    -v pgdata:/var/lib/postgresql/data \
    postgres
```

