# FunStory
# InteractiveStory

How to publish an app





developer.android.com
- Develop -> Tools -> Workflow -> Publishing
-> Preparing for Release


app -> src -> build.gradle
runProguard is false by default, we set it to true
Switch file to proguard-android-optimize.txt and synchronize the project with gradle files. 

Now edit the proguard-rules.pro file, add:
-assumenosideeffects class android.util.Log {
    public static boolean isLoggable(java.lang.String, int);
    public static int v(...);
    public static int i(...);
    public static int w(...);
    public static int d(...);
    public static int e(...);
}

Now Building a Release-Ready APK


APK, Android Application Package
Ususally built with a Debug Certificate, but when we want to publish it we need to digitally sign the APK with a self-signed certificate.

- In Android Studio, with App's project open, click on Build, Generate Signed APK

../Coding/AndroidStudio/cludetree*.jks




To create a new emulator
- AVD Manager
- 