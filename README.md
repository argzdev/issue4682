# issue 4682
### Github link:
- https://github.com/firebase/firebase-android-sdk/issues/4682

### Summary:
- Versions `2.9.3` and `2.9.4` on 'com.google.firebase:firebase-crashlytics-gradle` exhibits the following error.
- This issue is not present on versions `2.9.2` and below.

### Error:
- `Unstripped native library path does not exist: /Users/____/app/build/intermediates/merged_native_libs/release/out/lib. Either specify the correct unstrippedNativeLibsDir or disable Crashlytics symbol uploading.`

### Code snippet:
```
firebaseCrashlytics {
    nativeSymbolUploadEnabled = true
    strippedNativeLibsDir = "$buildDir/intermediates/stripped_native_libs/release/out/lib"
    unstrippedNativeLibsDir = "$buildDir/intermediates/merged_native_libs/release/out/lib"
}
```

