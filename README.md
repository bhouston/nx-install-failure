# This will often get installation failures related to the nx package

Machine setup:
* MacOS 15 Beta 1 (24A5289h), but I do not think it is connected to the beta.
* MacBook Air M3
* Node 22.2.0

Do this until the error occurs, it happens around 50% of the time, so if you are able to do the below more than 3 times in a row, it likely isn't happening on your machine:

```sh
# fully clean previous install
npm run clean 
# do a new install
npm install
```

The error that I get is this one:

```
bhouston@Ben-MacBook-Air-M3 nx-install-failure % npm install  
npm error code 1
npm error path /Users/bhouston/Coding/nx-install-failure/node_modules/lerna/node_modules/nx
npm error command failed
npm error command sh -c node ./bin/post-install
npm error /Users/bhouston/Coding/nx-install-failure/node_modules/lerna/node_modules/nx/src/native/native-bindings.js:244
npm error     throw loadError
npm error     ^
npm error
npm error Error: dlopen(/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node, 0x0001): tried: '/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node' (code signature invalid in <2ED4CDDA-275E-30B4-ACF0-E00AC37DB0B7> '/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node' (errno=85) sliceOffset=0x00000000, codeBlobOffset=0x005E3690, codeBlobSize=0x0000BCF8), '/System/Volumes/Preboot/Cryptexes/OS/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node' (no such file), '/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node' (code signature invalid in <2ED4CDDA-275E-30B4-ACF0-E00AC37DB0B7> '/Users/bhouston/Coding/nx-install-failure/.nx/cache/18.3.5-nx.darwin-arm64.node' (errno=85) sliceOffset=0x00000000, codeBlobOffset=0x005E3690, codeBlobSize=0x0000BCF8)
npm error     at Module._extensions..node (node:internal/modules/cjs/loader:1544:18)
npm error     at Module.load (node:internal/modules/cjs/loader:1249:32)
npm error     at Module._load (node:internal/modules/cjs/loader:1065:12)
npm error     at Module._load (/Users/bhouston/Coding/nx-install-failure/node_modules/lerna/node_modules/nx/src/native/index.js:58:27)
npm error     at Module.require (node:internal/modules/cjs/loader:1271:19)
npm error     at require (node:internal/modules/helpers:123:16)
npm error     at Object.<anonymous> (/Users/bhouston/Coding/nx-install-failure/node_modules/lerna/node_modules/nx/src/native/native-bindings.js:135:29)
npm error     at Module._compile (node:internal/modules/cjs/loader:1434:14)
npm error     at Module._extensions..js (node:internal/modules/cjs/loader:1518:10)
npm error     at Module.load (node:internal/modules/cjs/loader:1249:32) {
npm error   code: 'ERR_DLOPEN_FAILED'
npm error }
npm error
npm error Node.js v22.2.0
```


