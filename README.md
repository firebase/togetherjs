TogetherJS + Firebase
=====================

[TogetherJS](http://togetherjs.com) is a service for your website that makes it surprisingly easy to collaborate in real-time.
Learn more about it at the [original Github repository](https://github.com/mozilla/togetherjs).

This repository adds a [Firebase](https://www.firebase.com) powered messaging channel. This lets you run TogetherJS against your
own Firebase. Just set `HUB_URL` to any Firebase URL (`https://together.firebaseio-demo.com` by default) while running grunt
to generate the library. For example:

    HUB_URL="https://<your-firebase>.firebaseio.com/" grunt --base-url="/togetherjs" devwatch

There are two benefits to using Firebase as a messaging channel for TogetherJS sessions:

* Sessions are automatically persisted, which allows for easy replay of sessions if required.
* Firebase will automatically scale with your usage, eliminating the need to run your own Hub server.
