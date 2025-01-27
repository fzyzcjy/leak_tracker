Coming soon! See https://github.com/flutter/devtools/issues/5606.

The text below is under construction.

# Memory usage tracking and auto-snapshotting

This page describes how to configure memory usage tracking.
See other information on memory leaks [here](../README.md).

Dart and Flutter applications can be confugured to automatically
trigger memory usage events and, in case of memory overuse, to save
memory heap snapshots to hard drive.
The snapshots can be later analysed in DevTools.

https://user-images.githubusercontent.com/12115586/234953319-6f864d25-9854-4126-b4d6-8e114b9045ff.mov

## Configure usage tracking

Use the function `trackMemoryUsage` to configure usage events and auto-snapshotting.

See [example](../more_examples/autosnapshotting/).

We recommend to have auto-snapshotting off by default, with possibility
to enable it via command line arguments in case of reported memory issues.

## Analyse snapshots

TODO (polina-c): add link to DevTools help section.

## Auto-snapshotting limitations

### By platform

Usage tracking does not work for web platform.

### By build mode

While usage tracking events are available for all modes, auto-snapshotting
is on or off depending on the build mode:

* **Enabled for:** Flutter debug and profile modes (equivalent to Dart debug and release modes).
* **Disabled for:** Flutter release mode (equivalent to Dart product mode).

See [Dart build modes](https://github.com/dart-lang/site-www/issues/4436)
or [Flutter build modes](https://docs.flutter.dev/testing/build-modes).
