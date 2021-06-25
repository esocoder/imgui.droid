Imgui.droid
=============

Imgui.droid is a bare-bones, 2021.06 implementation of Android native-only C++ dear imgui implementation.

Derived from Google's NDK [Native Activity](http://developer.android.com/reference/android/app/NativeActivity.html) example (Native Plasma).

Then [Dear imgui](https://github.com/ocornut/imgui) was added. The imgui demo executes upon add startup and will push 60 fps even on emulators.

.vscode is only for my personal local development and should be ignored/modified to suit your needs.

NOTE: the functions that deal with activating on-screen keyboard input (originally in Kotlin) has been commented out and disabled in lieu of a better solution.

Tested on emulator(s) only w/ satisfactory results; actual on-device tests not done as of 2021.06.05.
