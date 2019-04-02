# ABBYRTRDemo
ABBY Real-Time Recognition SDK. This is a demo of Real time text recognition demo app in built in java with android studio.
Follow this link to implement RTR SDK .
https://rtrsdk.com/documentation/android/quick-start-guide/
Explore your Android OCR library distribution
In the download package of the Android OCR SDK you can find:

the Android OCR library itself (libs/abbyy-rtr-sdk-1.0.aar)
the resource files:
assets/dictionaries — dictionary support for some of the recognition languages; using a dictionary improves recognition quality
assets/patterns — recognition databases
License — your license file and license agreement for our Android OCR SDK
sample-textcapture — a code sample illustrating the use of the Android OCR library for capturing the text from the camera preview
sample-datacapture — a code sample illustrating the use of the Android OCR library for capturing data that matches a regular expression

To create an application which uses ABBYY Real-Time Recognition SDK to capture text from the camera preview, you will need to add the library and its assets to your project. This is required for new projects only — packaged code samples work out of the box.

If you are using a Maven or Ivy repository, add the ABBYY Real-Time Recognition SDK package there. If not, you can copy the library file (abbyy-rtr-sdk-1.0.aar) to your project or another folder and add this location as a flat repository. For example, add the following to the top-level build.gradle file in your project:
repositories {
    flatDir {
        dirs '<path to folder with the .AAR file>'
    }
}
Add the library dependency to the module-level build.gradle file. For example:
dependencies {
    compile(name:'abbyy-rtr-sdk-1.0', ext:'aar')
}
Copy the assets you need from the distribution to your project's assets (by default, app/src/main/assets). There are three types of resources used by the library: dictionaries, patterns, and translation dictionaries. See Minimize Your Memory Footprint for a short description of the necessary resources.
 Important! With common licenses, your Android OCR application needs an Internet connection to gather the information about the current state of the library. Include the following line into your AndroidManifest.xml:

<uses-permission android:name="android.permission.INTERNET" />
