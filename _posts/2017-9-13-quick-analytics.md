---
layout: post
title: Quick Analytics
---

Firebase analytics and crash reporting is fantastic for keeping tabs on issues in your app.  

The easiest way I've found to get it up and running app wide is to extend the application class - once you've added Firebase to your project (the wizard in Android Studio makes it super simple) make a custom one like this:

~~~~
public class WideWordsApplication extends Application {
    public static FirebaseAnalytics mFirebaseAnalytics;
    @Override
    public void onCreate() {
        super.onCreate();
        mFirebaseAnalytics = FirebaseAnalytics.getInstance(this);
    }
}
~~~~

Then simply reference it in your Manifest in the root Application node:

`<application
        android:name=".WideWordsApplication"
        ...`
        
That's it - you should now start to see data appearing in your Firebase analytics console.  I think this originally came from a Stack Overflow post, but I couldn't find it to reference - thanks in any case, whoever you are :-)
