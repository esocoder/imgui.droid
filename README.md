Imgui.droid
=============

Imgui.droid is a bare-bones, 2021.06 implementation of Android native-only C++ dear imgui implementation (OpenGL ES 3).

Derived from Google's NDK [Native Activity](http://developer.android.com/reference/android/app/NativeActivity.html) example (Native Plasma).

Then [Dear imgui](https://github.com/ocornut/imgui) was added. The imgui demo code executes upon startup and will push 60 fps, even on some emulator configurations.

.vscode is only for my personal local development and should be ignored/modified to suit your needs.

NOTE: the functions that deal with activating on-screen keyboard input (originally in Kotlin) has been commented out and disabled in lieu of a better solution.

Tested on emulator(s) and a one android device w/ satisfactory results.
