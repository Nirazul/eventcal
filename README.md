# Facebook Event Calendar
Subscribe to a subset of your Facebook events using ical

Facebook provides a way to export and sync all your events to a third party calendar application such as Google Calendar.
However you can't choose which events you want to sync and that's where this service steps in. Right now it simply
removes events you have not responded to yet. If you want to filter events in some other way, let me know on
[Google+](https://google.com/+simonbengtsson) or [twitter](https://twitter.com/someatoms).

### Deploy
To deploy this website, simply upload everything in the `app` folder to your server. This can for example be done with rsync.

`rsync -a --chown=www-data:www-data app/ username@flown.io:/var/www/eventcal.flown.io`

### Develop
The easiest way to start development is by using php's built in web server.

`php -S localhost:8080 -t app`

### Facebook API
It is possible to get event information from the Facebook Graph API and create an ical file from that. This would
make it easier for the user to sign up for the service, but would require a re-login every 60 days as that is the
 maxium period an access token is valid for.

### Contribute
Feature request, pull request and issues are welcome.
