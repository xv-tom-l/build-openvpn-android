
## PREPARE

* Install Android SDK and NDK

```
brew install android android-ndk ant makedepend
```

* Edit `~/.bashrc` and add:

```bash
# Android SDK
export ANDROID_SDK_ROOT=/usr/local/Cellar/android-sdk/23.0.2
export ANDROID_NDK_ROOT=/usr/local/Cellar/android-ndk/r10b
```

* Install `gradle` and `hg`

```bash
brew install gradle hg
```

* Get latest `ics-openvpn` source

```bash
hg clone https://code.google.com/p/ics-openvpn/
```

## BUILD

```bash
cd ics-openvpn
cd main
./misc/build-native.sh
ANDROID_HOME=$ANDROID_SDK_ROOT gradle build
```