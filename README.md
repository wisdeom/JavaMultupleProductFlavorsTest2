# Example of AppCenter lack of support for Flavors
This is an empty "new project" created via Android Studio. Nevertheless it fails to build on [appcenter.ms](https://appcenter.ms)
due to having 2 flavors defined. (`app/build.gradle` -> `productFlavors`)

Error message:
```
Task 'assembleFirst.dimensionRelease' not found in project ':app'.
```
Which is caused by appcenter trying to execute invalid Gradle command: `assembleFirst.dimensionRelease` instead of `assembleFirstRelease`

Currently there seems to be no way to select a valid variant via UI:
![AppCenterDashboard](AppCenterBuildConfiguration.png)

There is also no obvious way to execute full `build` command (that would work in gradle projects without need for AppCenter to detect flavors)


### Microsoft support reply:
`I had a discussion with the build team, they confirm that multiple flavor dimensions is not supported`
