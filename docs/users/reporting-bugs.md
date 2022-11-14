# Reporting bugs

When submitting a bug report, it is often helpful to include a log. The following steps can be followed on any Linux machine to capture the logs for Password Store in a text file that you can attach to a GitHub issue.

- Download the Android Platform Tools from [here](https://developer.android.com/studio/releases/platform-tools) and extract them into a directory
- Enable developer options on your device and turn on USB debugging by following [these steps](https://developer.android.com/studio/debug/dev-options)
- Enable debug logging for Password Store by going to Settings > Misc
- Open a new terminal in the directory where you extracted the platform tools
- Run `./adb shell am force-stop app.passwordstore` to close the app
- Launch the app again and replicate the issue
- Run `./adb logcat --pid=$(./adb shell pidof -s app.passwordstore) -d > log.txt` to capture the logs up till that point
- Upload `log.txt` either to the GitHub issue or email it to `googleplay@passwordstore.app` with the issue link