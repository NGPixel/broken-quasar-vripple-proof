# broken-quasar-vripple-proof

Page crashes with error `TypeError: Cannot read properties of undefined (reading 'config')`. Removing all `v-ripple` on `q-item` elements in `src/layouts/MainLayout.vue` resolves the issue.

### Install + Run

```sh
yarn
yarn dev
```

### Refs

https://github.com/quasarframework/quasar/issues/13154#issuecomment-1159555443
