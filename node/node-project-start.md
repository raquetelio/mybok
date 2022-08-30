# Init Node project
```
npm init
npm install
```

Test:
```
npm test
```

## Node ES6 project: 
Add this in in package.json
{"type": "module"}

## package.json example:
{
  "name": "servicename",
  "version": "1.0.0",
  "type": "module",
  "description": "Service",
  "dependencies": {
    "@grpc/proto-loader": "0.5.3",
    "@grpc/grpc-js": "1.4.4"
  }
}

## Launch
```
node archivo.js
```

## Re-launch after each change
```
nodemon archivo.js 
```
