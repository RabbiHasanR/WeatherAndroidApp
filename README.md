# Title 
WeatherAndroidApp
# Description
It's a weather app.It's provide weather information based on location.Used weather API in this application.Also use responsive and material design.
It's a very simple android weather app.Aslo use android notification.
## Features
### Show daily weather information
### provide notification when weather update
### Change location
### Change temparature Unit
### Responsive
### Show map location
### Enable/Disable notification
### Share Information

# Usages

### Permissions in mainfest.xml
``````````
<uses-permission android:name="android.permission.INTERNET"/>
``````````

### ### create service and provider in mainfest.xml
``````
<!-- Our ContentProvider -->
        <provider
            android:name=".data.WeatherProvider"
            android:authorities="@string/content_authority"
            android:exported="false"/>

        <!--This is required for immediate syncs -->
        <service
            android:name=".sync.SunshineSyncIntentService"
            android:exported="false" />

        <!-- This is the Service declaration used in conjunction with FirebaseJobDispatcher -->
        <service
            android:name=".sync.SunshineFirebaseJobService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.firebase.jobdispatcher.ACTION_EXECUTE"/>
            </intent-filter>
        </service>
``````
### build.gradle(app)
````````
 implementation 'com.android.support:recyclerview-v7:26.1.0'
    implementation 'com.android.support:preference-v7:26.1.0'

    implementation 'com.android.support.constraint:constraint-layout:1.0.0-beta3'

    implementation 'com.firebase:firebase-jobdispatcher:0.5.0'
````````
