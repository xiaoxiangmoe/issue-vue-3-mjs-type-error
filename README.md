# vue-3-mjs-type-error

```sh
yarn tsc
# type check works well

node src/vue3.cjs 
# print [Function: createApp]
# cjs works as intended

node src/vue3-named-import.mjs
# print [Function: createApp]
# mjs named import works as intended

node src/vue3-default-import.mjs
# file:///Users/me/issue-vue-3-mjs-type-error/src/vue3-default-import.mjs:2
# import vueDefaultImport from 'vue'
#        ^^^^^^^^^^^^^^^^
# SyntaxError: The requested module 'vue' does not provide an export named 'default'
#     at ModuleJob._instantiate (node:internal/modules/esm/module_job:124:21)
#     at async ModuleJob.run (node:internal/modules/esm/module_job:190:5)
# 
# Node.js v19.3.0
# mjs default import not works
```
