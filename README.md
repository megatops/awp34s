# Android WP-34s Calculator

![No AI](https://img.shields.io/badge/%F0%9F%A4%97-No_AI-green) [![DeepWiki](https://img.shields.io/badge/DeepWiki-awp34s-blue)](https://deepwiki.com/megatops/awp34s) ![GitHub License](https://img.shields.io/github/license/megatops/awp34s?logo=license) ![GitHub top language](https://img.shields.io/github/languages/top/megatops/awp34s) ![GitHub contributors](https://img.shields.io/github/contributors-anon/megatops/awp34s) ![GitHub forks](https://img.shields.io/github/forks/megatops/awp34s) ![GitHub Repo stars](https://img.shields.io/github/stars/megatops/awp34s)

This is a fork of [Pablo Martín Medrano's Android WP-34s port](https://github.com/odkq/awp34s). My changes:

- New features & enhancements:
  - Brand new high-res retro skin, with key press feedback.
  - Update the WP-34s code from [r3913](https://sourceforge.net/p/wp34s/code/3913/) (2019-11-24) to [r3927](https://sourceforge.net/p/wp34s/code/3927/) (2025-10-20).
  - Support <kbd>CPX</kbd> <kbd>R/S</kbd> (`STOPW`, stopwatch), <kbd>STO</kbd> <kbd>CPX</kbd> (`STOM`, mode data store) and <kbd>RCL</kbd> <kbd>CPX</kbd> (`RCLM`, mode data recall).
  - Automatically save the state of the WP-34S when the app is switched to the background to prevent data loss.
  - Keep screen on only when stopwatch is running, otherwise follow the system settings.
  - Upgrade to Android SDK 34.
- Bug fixes:
  - Prevent `SEND*` and `RECV` (serial I/O) commands hang, now it will report `I/O error` since there is no serial port on Android.

This fork can only be built with Android Studio, run `apply_patch` in `app/src/main/cpp` before build. Signed APKs are provided under releases, support Android 5.1+.

> ℹ **Disclaimer**
>
> All product names, logos, and brands such as _HP_, _Hewlett-Packard_, are property of their respective owners. Their use in this project is for identification and reference only and does not imply any endorsement or partnership.

Below is the original README (Note: some information is outdated):

---

WP 34s Calculator Port to Android

<img src="doc/awp34s-a2.jpg" alt="Screenshot" width="300"/>

Port of the WP 34S calculator (open source firmware for the HP 30b/20b
calculators) to Android.

Install latest tag directly from GooglePlay at:
https://play.google.com/store/apps/details?id=com.odkq.wp34s

You can build a debug .apk and install it manually in the device following the
instructions at [BUILDING.md](BUILDING.md).

Any contribution/pull request is of course welcome. There is a
[TO-DO list](TODO.md) on future plans

Information on WP 34S:

  - [Wikipedia Entry](https://en.wikipedia.org/wiki/HP_30b#WP_31S,_WP_34S_and_WP_34C)
  - [SourceForge Project](https://sourceforge.net/projects/wp34s/)
  - [Online Seller](https://commerce.hpcalc.org/34s.php)
  - [Original Wiki](http://www.wiki4hp.com/doku.php?id=34s:repurposing_project)

At [this directory on SF](https://sourceforge.net/projects/wp34s/files/doc/)
you will find a beginners guide
[WP_34S_Beg_Guide.pdf](https://pilotfiber.dl.sourceforge.net/project/wp34s/doc/WP_34S_Beg_Guide.pdf)
and a comprehensive manual
[Manual_wp_34s_3_1.pdf](https://deac-ams.dl.sourceforge.net/project/wp34s/doc/Manual_wp_34s_3_1.pdf")
The manuals apply in its entirety to this port.

The WP 34S project has an iPhone app but no Android app. Wanting to learn
about Android and NDK development, I did this.

I labeled this as a port rather than as an emulator as it is not
emulating the CPU of the physical device. The firmware itself originally
written in portable C is compiled along with the
Android Native Development Kit (NDK).

The code for the interface and modifications to the WP 34s firmware are
Free Software and released under the GNU Public License v3, as the WP
34S code itself.

Thanks to Walter Bonin, Paul Dale, Marcus von Cube and the rest of the WP 34S
contributors for the excellent calculator.
