TogetherJS + Firebase
=====================

[TogetherJS](http://togetherjs.com) is a service for your website that makes it surprisingly easy to collaborate in real-time.
Learn more at the [original Github repository](https://github.com/mozilla/togetherjs).

This repository lets you use <a href="http://firebase.com/" target="_blank">Firebase</a> as the backend for your TogetherJS sessions.

### Benefits
There are two benefits to using Firebase with TogetherJS:

* <strong>Persistence</strong> - Sessions are automatically persisted, which allows for easy replay of sessions (cursor movements, chat history, etc) if required.
* <strong>Scalability</strong> - Firebase is built to scale with your usage, eliminating the need to run and manage your own Hub server.

### Usage
Set `HUB_URL` to any Firebase URL (`https://together.firebaseio-demo.com` by default) while running grunt
to generate the library. For example:

    HUB_URL="https://<your-firebase>.firebaseio.com/" grunt --base-url="/togetherjs" devwatch
