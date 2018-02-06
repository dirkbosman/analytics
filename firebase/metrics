Table of Contents: 

*Active Users and session_start event metrics are computed differently:*

Active users are users who used your app in a device (app should be in foreground) AND has logged a user_engagement event. More specifically:
* DAU (1 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 1 day period.
* WAU (7 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 7 day period.
* MAU (30 Day Active Users)	The number of unique users who has engaged with your app in the device foreground AND has logged a user_engagement event within the (last) 30 day period.
Note: Select the beginning & end date of the month; Read the last Day's value of the selected period (i.e. 31 Jan. 28 Feb. 30 April. etc.) 	

On the other hand, session_start event will be triggered when a user engages in your app for more than the minimum session 
duration after a period of inactivity that exceeds the session timeout duration. 

By default, a session starts after at least 10s of user engagement (after a period of at least 30m of no triggers of user_engagement). And so, whenever users use your app for a period 
of less than 10s, you will accrue user engagement without a session. This often occurs after launching a new version of your app, since users download it and open 
it for a short amount of time (sometimes inadvertently after the upgrade) before backgrounding it[Source](https://stackoverflow.com/questions/38967231/firebase-analytics-data-disparity).





https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics#setMinimumSessionDuration(long)
https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics#setSessionTimeoutDuration(long)


Firebase User Retention is calculated on user_engagement and not session_start ? 








