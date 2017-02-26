# Template

A basic vapor template for starting a new Vapor web application. If you're using vapor toolbox, you can use: `vapor new --template=kateinoigakukun/vapor-template`

## Requirement

- gulp

  `$ npm init`
  
  `$ npm install --save-dev gulp`
- gulp-vapor

  `$ npm install --save-dev gulp-vapor`

## Development

### Xcode
`$ vapor xcode -y`

### Deploy

```
$ docker build -t vapor-template docker
$ docker run -ti \
        --name $(basename $(pwd)) \
        -p 127.0.0.1:8080:8080 \
        -p 127.0.0.1:3306:3306 \
        -v mysql.data:/var/lib/mysql \
        -v $(pwd):/vapor \
        vapor-template
```

In container
`$ vapor build`
`$ ./.build/debug/App`


## 📖 Documentation

Visit the Vapor web framework's [documentation](http://docs.vapor.codes) for instructions on how to use this package.

## 💧 Community

Join the welcoming community of fellow Vapor developers in [slack](http://vapor.team).

## 🔧 Compatibility

This package has been tested on macOS and Ubuntu.
