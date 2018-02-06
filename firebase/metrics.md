Table of Contents: 

*In Firebase, Active Users and Sessions metrics are computed differently:*

Active users are users who used your app in a device (app should be in foreground) AND has logged a user_engagement event. More specifically:
* DAU (1 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 1 day period.
* WAU (7 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 7 day period.
* MAU (30 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 30 day period.
Note: Select the beginning & end date of the month; Read the last Day's value of the selected period (i.e. 31 Jan. 28 Feb. 30 April. etc.) 	

On the other hand, session_start event will be triggered when a user engages in your app for more than the [minimum session duration](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics#setMinimumSessionDuration(long)) after a period of inactivity that exceeds the [session timeout duration](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics#setSessionTimeoutDuration(long)). "By default, a session starts after at least 10s of user engagement (after a period of at least 30m of no triggers of user_engagement). And so, whenever users use your app for a period of less than 10s, you will accrue user engagement without a session. This often occurs after launching a new version of your app, since users download it and open it for a short amount of time (sometimes inadvertently after the upgrade) before backgrounding it" [(Source)](https://stackoverflow.com/questions/38967231/firebase-analytics-data-disparity).
* There is a reason why the App needs to be open at least 10s before session will be started. "Setting session timeout to 5 seconds practically means every time the app is backgrounded a new session will be recorded. This defeats the purpose of session"[(Source)](https://github.com/firebase/quickstart-cpp/issues/2).

To have a better representation of your DAUs and WAUs over any selected range, consider to download the Firebase Dashboard and calculate the Average of the last 30 Days. Feel free to also look at your highest high (MAX Function) and your lowest lows (MIN Function). 
* AVG 1 Day Active Users of Month (Calc)
* AVG 7 Day Active Users of Month (Calc)
* 30 Day Active Users (Filter it down by User Property = New / Returning User)

Finally you can calculate the DAU-to-MAU ratio as: 1DAU / 30MAU.
* "It is a ""Stickiness"" user engagement mentric. and is generally calculated as the ratio of Daily Active Users to Monthly Active Users. A DAU/MAU ratio of 50% would mean that the average user of your app is using it 15 out of 30 days that month."

Consider Also: 
* User Sessions and Firebase ID tokens...https://firebase.google.com/docs/auth/admin/manage-sessions
* BigQuery integration: https://stackoverflow.com/questions/46302556/calculating-active-user-metrics-for-firebase-analytics-in-bigquery?rq=1
* Auto Collected events: https://support.google.com/firebase/answer/6317485?hl=en


