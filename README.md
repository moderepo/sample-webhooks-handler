# Sample Webhooks Handler

This is a small sample **webhooks** handler for a MODE project.

If you don't know how webhooks for MODE work, please refer to this [doc](http://dev.tinkermode.com/docs/webhooks.html).


## How to Run on Heroku

You can launch this sample webhooks handler on Heroku by following these steps:

1. Create an account on Heroku, if you don't have one already.
1. Go to the MODE Developer Console and set up a new Webhooks Smart Module for your project.
1. Set up an **Event Webhook** for the Smart Module using an URL in the format `https://HEROKU_APP_NAME.herokuapp.com/evt`, where `HEROKU_APP_NAME` should be replaced by a unique app name in the Heroku namespace.
1. Click this button --> <a href="https://heroku.com/deploy" target="_blank"><img src="https://www.herokucdn.com/deploy/button.png" title="Deploy to Heroku"></a>
1. You will land on the Heroku screen for deploying a new app. Make sure you enter the Heroku app name you used in step 3. You must also enter the appropriate values for the config variables `EVENT_KEY` (event webhook key) and `EVENT_URL` (event webhook URL). You can get these from the Smart Module settings page on the MODE console.
1. Deploy the Heroku app.

After launching the Heroku app, open the app's URL on your browser. You will see the message: `No device event.` It means the code is running. Now, you can send an event from a device, or from the Device Simulator. If `EVENT_KEY` and `EVENT_URL` are correctly set, you should see the event JSON string appearing on the browser screen, which looks like this:

~~~
{"homeId":173,"timestamp":"2016-01-04T23:26:09.521Z","eventType":"abc","eventData":{},"originDeviceId":260}
~~~

