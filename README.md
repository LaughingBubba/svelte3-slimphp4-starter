## Installation

- Clone this repo
- CD to repo folder
- `npm install`
- `npm run build`
- `composer require`

## Commands

Build the production ready image:   
```bash
docker build . -f Dockerfile.prod -t s3s4-starter
```

Run the production ready image:   
```bash
docker run -p 3000:8080 s3s4-starter
```

## Dev Mode

This builds and starts the web app:

Build/Run the production ready image in (local) DEV mode:
```bash
docker-compose up
```

Changes to PHP / HTML / CSS in the `./public` folder will be reflected straight away.

When modifying Svelte code, remember to run `npm run build` to rebuild the `./public/build` folder.

### Livereload
- Install browser extension: https://github.com/ritwickdey/live-server-web-extension (FF or Chrome only)   
- Create a separate cli in VSC and run `npm run dev` and copy the host and port : `http://localhost:5000`   
- Create a separate cli in VSC and run `docker-compose up` 
- Navigate to the PHP host via the browser: `http://localhost:3000`
- Click on the live-sever button in browser menu bar
- Update live-server address with : `http://localhost:5000`
- Enjoy!
