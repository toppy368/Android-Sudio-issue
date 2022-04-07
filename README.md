# Android-Sudio-issue
疑難雜症與處理方式合集

## Gradle 版號錯誤

錯誤訊息完整截圖如下：
![Gradle version error][https://github.com/toppy368/Android-Sudio-issue/blob/main/images/2022-04-07%2022.58.46_Gradle-version-error.jpg]


若發生以下錯誤訊息：  

    Build file '/Users/Users/AndroidStudioProjects/MyApplication2/build.gradle' line: 3  
    Plugin [id: 'com.android.application', version: '7.1.3', apply: false] was not found in any of the following sources:
    
    * Try:
    Run with --info or --debug option to get more log output. Run with --scan to get full insights.

    * Exception is:
    org.gradle.api.plugins.UnknownPluginException: Plugin [id: 'com.android.application', version: '7.1.3', apply: false] was not found in any of the following sources:

    - Gradle Core Plugins (plugin is not in 'org.gradle' namespace)
    - Plugin Repositories (could not resolve plugin artifact 'com.android.application:com.android.application.gradle.plugin:7.1.3')
        Searched in the following repositories:
        Gradle Central Plugin Repository
        Google
        MavenRepo...

請將版本號往下修改，將 `com.android.application` 及 `com.android.library` 的 version 版本號 從 `7.1.3` 改成 `7.1.2`。