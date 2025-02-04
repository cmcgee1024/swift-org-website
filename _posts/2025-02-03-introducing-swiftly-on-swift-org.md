---
layout: post
published: true
date: 2025-02-04 6:00:00
title: Introducing Swiftly on swift.org
author: [chris-mcgee]
---

Swiftly, the Swift toolchain manager is now available on swift.org.

## Introducing Swiftly

Swiftly has been around for some years as a tool that Swift developers have used to manage their toolchain with Linux. Originally conceived by Patrick Freed as a Swift on Server project, it was adopted by the Swift language family on GitHub last year. Since that time it's gained a new supported platform, macOS. There are new features, such as listing available toolchains using the swift.org API. And now it is the recommended tool for working with Swift toolchains on both platforms on swift.org.

## Quick tour

After downloading and installing swiftly you can list the available toolchains:

```
swiftly list-available
```

Install a toolchain from the list.

```
swiftly install 6.0.3
```

Swiftly will provide directions after installation if there are any system packages, or shell commands for smooth operation of the new toolchain. Use the toolchain so that the usual commands come from that one.


```
swiftly use 6.0.3
swift --version
--
Apple Swift version 6.0.3 (swiftlang-6.0.3.1.2 clang-1600.0.28.6)
Target: arm64-apple-macosx15.0
```

You can also find nightly "snapshot" toolchains leading up to the next release to try it out.

```
swiftly list-available main-snapshot
--
Available main development snapshot toolchains
----------------------------------------------
main-snapshot-2025-02-02
...
```

Install the snapshot toolchain using its name.

```
swiftly install main-snapshot-2025-02-02
--
Installing main-snapshot-2025-02-02
```

Run lldb from that snapshot by name with the special '+' parameter:

```
swiftly run lldb +main-snapshot-2025-02-02
--
(lldb) _
``

And run it using the 6.0.3 toolchain installed above:

```
swiftly run lldb +6.0.3
```

## More information

If you're curious about swiftly, you can find more information in these places:

* [Swiftly Repo](https://github.com/swiftlang/swiftly)
* [Swiftly DocC](https://swiftpackageindex.com/swiftlang/swiftly/0.4.0-dev/documentation/swiftlydocs)

Download the latest version from the [swift downloads page](https://www.swift.org/install).
