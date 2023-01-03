# hello-world-pwa
____
## If you want to set up the project from scratch...
See [Tutorial](https://www.youtube.com/watch?v=15Yr-J4X34M)

```
vue create hello-world-pwa
```

Options
- Select "Manually select features"
- Select PWA (spacebar to select options) then enter
- Select version of vue (this uses @2)

____

## 1st time project setup
```
yarn install
```
____
## For Development
### Development for hot-reloads
```
yarn serve
```
### Development for hot-reloads in "production" mode
```
yarn serve-prod
```
## For Production

### pre-requisite install "serve" package
```
npm install -g serve
```
### Run prod
```
yarn build
serve dist/
```

____
### Linting
```
yarn lint
```
____
### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
<br />
Config overrides can be made in file `vue.config.js`
<br />
Example "name" override
```
pwa: {
    name: 'Name override'
  }
```
____

## PWA Up and running
After serving './dist' folder in browser...
- In Chrome there is a download icon which appears in the browser search bar. Clicking this icon will download the PWA to your desktop.
- Clicking on the desktop icon will open the PWA (which is browser window with no header or search bar)
- You should also be able to refresh page in offline mode (Applciation/Service Worker/offline) and still see the app (Service worker gets what it needs from cache)
## Useful Browser tools (inspector)
### Network:
- refresh page for the PWA
- see what is being loaded and from where
- if cached asset being used, column "size" will show "ServiceWorker"
### Application:
- see service worker and what has been used for Application build
- unregister service worker
- Service worker section, you can go "offline"
- Cache: > Cache storage: should the files which have been cached by Service worker.
### Service worker:
- The service worker will only register if its served on localhost or https (not http)
____
