# CzUIzqjDEN

Install npm module
<ol>
<li><code>npm install react-native-maps --save</code></li>
<li><code>react-native link react-native-maps</code></li>
</ol>

<hr/>
android/build.gradle

<pre><code>// Top-level build file where you can add configuration options common to all sub-projects/modules.

buildscript {
    repositories {
        jcenter()
        google()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.0.1'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}
</pre>
<hr />

android/gradle/wrapper/gradle-wrapper.properties

<b>Change distributionUrl</b>
<pre><code>distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists
distributionUrl=https\://services.gradle.org/distributions/gradle-4.1-all.zip
</code></pre>
<hr/>

android/app/build.gradle

<pre><code>android {
  compileSdkVersion 25
  buildToolsVersion "25.0.1"
  ...
  dependencies {
    compile (project(':react-native-camera'))  <-- remove this
    compile fileTree(dir: "libs", include: ["*.jar"])
    compile "com.android.support:appcompat-v7:24.0.0" <--- v7:23.x.x change 24.0.0
    compile "com.facebook.react:react-native:+"  // From node_modules
    implementation project(':react-native-maps') <-- add this
}
</code></pre>
