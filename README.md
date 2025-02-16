# Useful Commands

## Index

- [Node.js](#nodejs)
    - [1. Version & Environment](#1-version--environment)
    - [2. Running Node.js Files](#2-running-nodejs-files)
    - [3. Package Management (npm)](#3-package-management-npm)
    - [4. Running Scripts (Defined in package.json)](#4-running-scripts-defined-in-packagejson)
    - [5. Using npx (Run Packages Without Installing)](#5-using-npx-run-packages-without-installing)
    - [6. Debugging & Monitoring](#6-debugging--monitoring)
    - [7. Managing Environment Variables (Windows)](#7-managing-environment-variables-windows)
    - [8. Working with Dependencies](#8-working-with-dependencies)
    - [9. Checking & Fixing Issues](#9-checking--fixing-issues)
    - [10. Creating and Running a Simple Server](#10-creating-and-running-a-simple-server)

## Node.js

### 1. Version & Environment
- `node -v` - Check Node.js version
- `npm -v` - Check npm version
- `npx -v` - Check npx version
- `where node` - Find the Node.js installation path
- `where npm` - Find the npm installation path

### 2. Running Node.js Files
- `node filename.js` - Run a Node.js script
- `node` - Start the Node.js REPL (interactive shell)

### 3. Package Management (npm)
- `npm init -y` - Initialize a new package.json file
- `npm install` - Install all dependencies from package.json
- `npm install <package>` - Install a package locally
- `npm install -g <package>` - Install a package globally
- `npm uninstall <package>` - Uninstall a package
- `npm list --depth=0` - List installed packages (without dependencies)
- `npm outdated` - Check for outdated packages
- `npm update` - Update all packages
- `npm cache clean --force` - Clear npm cache

### 4. Running Scripts (Defined in package.json)
- `npm start` - Run the "start" script from package.json
- `npm test` - Run the "test" script from package.json
- `npm run <script-name>` - Run a custom script from package.json

### 5. Using npx (Run Packages Without Installing)
- `npx eslint .` - Run ESLint on the current project

### 6. Debugging & Monitoring
- `node --inspect filename.js` - Run with debugging enabled
- `node --inspect-brk filename.js` - Run & pause execution at the first line for debugging
- `node --trace-warnings` - Show detailed warning traces

### 7. Managing Environment Variables (Windows)
Set environment variables in CMD:
```shell
set NODE_ENV=production
```
Set environment variables in PowerShell:
```powershell
$env:NODE_ENV="production"
```
Access environment variables in Node.js:
```javascript
console.log(process.env.NODE_ENV);
```

### 8. Working with Dependencies
- `npm install <package> --save` - Install as a dependency (default in npm 5+)
- `npm install <package> --save-dev` - Install as a dev dependency
- `npm prune` - Remove unused dependencies
- `npm dedupe` - Remove duplicate dependencies

### 9. Checking & Fixing Issues
- `npm audit` - Check for security vulnerabilities
- `npm audit fix` - Automatically fix vulnerabilities
- `npm doctor` - Check npm configuration and system health

### 10. Creating and Running a Simple Server
```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello, Node.js!');
});

server.listen(3000, () => console.log('Server running on port 3000'));
```
Run the server:
```shell
node server.js
```
Then open [http://localhost:3000/](http://localhost:3000/) in a browser.
