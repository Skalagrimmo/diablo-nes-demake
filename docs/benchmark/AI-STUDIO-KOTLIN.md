# Participant addendum — Google AI Studio (native Kotlin / Android)

**Required implementation platform: native Android with Kotlin.** This is a deliberate part of the experiment: do not deliver a browser game as the main result.

Read [COMMON-PROMPT.md](COMMON-PROMPT.md) and the shared brief first. Everything in those documents applies.

## Platform-specific task

Build **The Last Reactor** as a standalone native Android application written in Kotlin.

- Implement the game itself in Kotlin. Do not use a WebView, embedded HTML/JavaScript game, remote web page or thin APK wrapper around the supplied `index.html`.
- The supplied browser prototype is the design and gameplay baseline, not a runtime dependency. Reimplement or adapt its game systems natively.
- Target **Android 8.0 / API 26 or newer** as the compatibility floor.
- Produce a complete Android Studio/Gradle project and a buildable debug APK.
- The app must work offline after installation. Do not require Google Play Services, sign-in, a server or an internet connection.
- Use a simple, low-overhead rendering approach suitable for modest Android devices.

## Suggested technical approach

You may choose the exact architecture, but a good starting point is:

- Kotlin for game state, entities, combat, progression, world logic and persistence.
- A custom Android `View` or `SurfaceView` using `Canvas` for the game renderer. A fixed virtual canvas close to the source's 256×240 presentation, scaled with aspect-ratio preservation and letterboxing, is a reasonable option.
- A fixed-step simulation or otherwise stable update loop; avoid an uncontrolled busy loop and avoid allocating large numbers of temporary objects every frame.
- Touch controls drawn as a dedicated overlay or rendered in the game view. Make movement and action buttons comfortable to use and prevent UI controls from blocking the playfield unnecessarily.
- Compose may be used for menus, settings or inventory UI, but do not force the real-time game renderer through a heavyweight recomposition loop.
- Android `SoundPool` or another lightweight local audio solution for sound effects. Music can use an appropriate local/system audio path; do not attempt to emulate hardware sound chips.
- Versioned local save data using SharedPreferences, a file or another dependable on-device mechanism. No cloud save.
- Keep game logic separated from rendering and input so it can be tested without an Activity.

These are recommendations, not a rigid framework mandate. If you choose a different native Kotlin architecture, explain why and demonstrate that it works on the target API level.

## Required Android deliverables

In addition to the common delivery package, provide:

1. Full Android Studio project, including Gradle wrapper and all source/resources.
2. Exact `minSdk`, `targetSdk`, Kotlin and Android Gradle Plugin versions.
3. The command to build from a clean project, preferably `./gradlew assembleDebug`.
4. The resulting debug APK (for example, `app/build/outputs/apk/debug/app-debug.apk`).
5. Installation and launch instructions using Android Studio or `adb install -r`.
6. A brief compatibility note covering API 26+ and any device-specific limitations.
7. Actual test evidence from an emulator or physical Android device. If no device test is possible, say so plainly and provide build/test output instead.

## Android acceptance checks

- [ ] The project builds as a native Android APK.
- [ ] The APK launches without a network connection.
- [ ] Gameplay is implemented in Kotlin, not hosted in a WebView.
- [ ] Touch movement and action controls respond reliably.
- [ ] The game handles Activity pause/resume without corrupting the game state.
- [ ] Screen scaling and orientation are deliberate; controls remain accessible.
- [ ] Save/continue survives app process termination and relaunch.
- [ ] No required Google service, account or online asset is present.
- [ ] Rendering and update work is not tied to a rapidly recomposing UI tree.
- [ ] The project contains clear build instructions and reports what was actually tested.

## Priorities

1. A working native Kotlin game loop and responsive touch controls.
2. A visually coherent industrial-fantasy district.
3. A complete playable loop: explore, encounter, earn, upgrade, interact and face a major encounter.
4. Reliable save/resume and stable lifecycle behaviour.
5. Clean enough architecture to add districts and systems later.

Do not spend the entire budget building an elaborate framework before the first playable scene exists. Establish a minimal end-to-end playable loop early, then improve it.
