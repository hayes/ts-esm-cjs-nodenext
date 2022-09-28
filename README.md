# Typescript nodenext with separate dts directory


node_modules are checked into this repo with an example dependency, so running an npm install may break the reproduction


the "example-package" has a class as a default export.  It defines exports for both esm and cjs, and defines types in a shared "dts" directory.

"src/index.ts" uses the cjs import, and works correctly, src/index.mts and "src/esm/index.ts" both use the esm import, and have an error saying `Type 'typeof import("{path}/node_modules/example-package/dts/index")' has no construct signatures.`
