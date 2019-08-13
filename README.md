This project demonstrates https://github.com/rails/webpacker/issues/2197

If you clone this repo, and run `bin/rails s` and go to http://localhost:3000/,
you'll see the following in the js console:

    Uncaught Error: Module build failed (from ./node_modules/css-loader/dist/cjs.js):
    ValidationError: Invalid options object. CSS Loader has been initialised using an options object that does not match the API schema.
     - options has an unknown property 'localIdentName'. These properties are valid:
       object { url?, import?, modules?, sourceMap?, importLoaders?, localsConvention?, onlyLocals? }
        at validate (:3000/home/jeremy/tmp/css-loader-issues/node_modules/css-loader/node_modules/schema-utils/dist/validate.js:49)
        at Object.loader (:3000/home/jeremy/tmp/css-loader-issues/node_modules/css-loader/dist/index.js:34)
        at Object../node_modules/css-loader/dist/cjs.js?!./node_modules/postcss-loader/src/index.js?!./app/javascript/src/application.css (application.css:20)
        at __webpack_require__ (bootstrap:19)
        at Object../app/javascript/src/application.css (application.css:2)
        at __webpack_require__ (bootstrap:19)
        at Module../app/javascript/packs/application.js (application.js:1)
        at __webpack_require__ (bootstrap:19)
        at bootstrap:83
        at bootstrap:83
    ./node_modules/css-loader/dist/cjs.js?!./node_modules/postcss-loader/src/index.js?!./app/javascript/src/application.css @ application.css:20
    __webpack_require__ @ bootstrap:19
    ./app/javascript/src/application.css @ application.css:2
    __webpack_require__ @ bootstrap:19
    ./app/javascript/packs/application.js @ application.js:1
    __webpack_require__ @ bootstrap:19
    (anonymous) @ bootstrap:83
    (anonymous) @ bootstrap:83

