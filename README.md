# Yvori Releases

Public binaries and Sparkle update feeds for Yvori apps. Application source
code is maintained in separate repositories.

## Update feeds

| App | Appcast | Release tag prefix |
| --- | --- | --- |
| App Sniper | [`appcasts/app-sniper.xml`](appcasts/app-sniper.xml) | `app-sniper-v` |

Each app has its own appcast on `main`. Release assets use immutable,
app-specific tags such as `app-sniper-v1.1.0`. An appcast item points directly to
its versioned asset URL. A release for another app cannot change the feed URL
or the download URL for App Sniper.

Only publish archives signed with the app's Developer ID and Sparkle EdDSA key.
Notarize and verify the macOS app before uploading it. Upload the exact archive
whose signature appears in the appcast; changing its bytes afterward invalidates
the signature. Keep private signing keys out of this repository.
