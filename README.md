# README

This is a test repository to reproduce an issue with GraphiQL and PostCSS, documented at https://github.com/graphql/graphiql/issues/2722.

When processing GraphQL's CSS with `postcss-preset-env`, Webpack spits out dozens of warnings along the lines of:

> WARNING in ./node_modules/graphiql/graphiql.css (./node_modules/css-loader/dist/cjs.js!./node_modules/postcss-loader/dist/cjs.js!./node_modules/graphiql/graphiql.css)
>Module Warning (from ./node_modules/postcss-loader/dist/cjs.js):
>Warning

>(333:14477) postcss-is-pseudo-class: Complex selectors in ':is(.CodeMirror-info .info-deprecation)>*' can not be transformed to an equivalent selector without ':is()'.
> @ ./node_modules/graphiql/graphiql.css 8:6-119 22:17-24 26:0-89 26:0-89 27:22-29 27:33-47 27:50-64
> @ ./src/index.js 1:0-46