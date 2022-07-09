# README

## Android ライブラリの作り方

1. [File] > [New] > [New Module]

2. Select template to Android Library

3. Input Library name, module name, package name, language and Min version.

```gradle:settings.gradle
+ include ':<module name>'
```


**appモジュールからライブラリを参照するためには？**

```gradle:build.gradle(app)
dependencies {
    implementation project(":mylibrary")
}
```


4. release
```sh
cd <project root>
./gradlew clean build publish
```


5. usage


## Ref

[Android LibraryをGitHub ActionsでビルドしGitHub Packagesで公開する](https://qiita.com/Horie1024/items/be2b5eb768f36794c4f1)
[github-packages-android-sample](https://github.com/horie1024/github-packages-android-sample)
