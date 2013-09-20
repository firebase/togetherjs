TogetherJS + Firebase
=====================

[TogetherJS](http://togetherjs.com) is a service for your website that makes it surprisingly easy to collaborate in real-time.
Learn more at the [original Github repository](https://github.com/mozilla/togetherjs).

This repository lets you use <a href="http://firebase.com/" target="_blank">Firebase</a> as the backend for your TogetherJS sessions.

####<a href="http://firebase.github.io/togetherjs/index.html?firebase=1#&togetherjs=Eb9UueHBrs" target="_blank">Try it out!</a>

### Benefits
There are two benefits to using Firebase with TogetherJS:

* <strong>Persistence</strong> - Sessions are automatically persisted, which allows for easy replay of sessions (cursor movements, chat history, etc) if required.
* <strong>Scalability</strong> - Firebase is a robust service and is built to automatically scale with your usage.

### Usage
Include the modified version of TogetherJS along with Firebase. You may also
(optionally) set the HUB URL to your own Firebase:

```html
<script>
  TowTruckConfig_hubBase = "https://<my-firebase>.firebaseio.com/";
</script>
<script src="https://cdn.firebase.com/v0/firebase.js"></script>
<script src="http://firebase.github.io/togetherjs/togetherjs.js"></script>
```

Then use TogetherJS as you normally would:

```html
<button onclick="TowTruck(this); return false;">Start TowTruck</button>
```

If you want to build your own version of the JavaScript libraries, don't
forget to set `HUB_URL` to a valid Firebase URL (`https://together.firebaseio-demo.com` by default)
while running grunt. For example:

```bash
HUB_URL="https://<your-firebase>.firebaseio.com/" grunt --base-url="/togetherjs" devwatch
```
