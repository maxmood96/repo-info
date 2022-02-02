## `gradle:7-jdk`

```console
$ docker pull gradle@sha256:142efb316ba3d4e163bf66fd526da28d8478b2a821087354bc3167917b289d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:aeeb5b434881bae15ecc6b0ec20567965dda6a678beb3d92e86daf64c3da6d1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.8 MB (422802136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667f822667828d52270eeaa09e4c970d06885fa385709b9821af964bce3390f7`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:59:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:15 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 03:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 03:00:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 03:00:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 03:00:27 GMT
CMD ["jshell"]
# Wed, 02 Feb 2022 09:42:22 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 09:42:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 09:42:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 09:42:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 09:42:24 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 09:42:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 09:42:41 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 09:42:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 09:42:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2670b5a474c24f63b09c71ff7444033a3440b5ad3d67eb1aca9e315ff31cab`  
		Last Modified: Wed, 02 Feb 2022 03:03:28 GMT  
		Size: 28.6 MB (28562645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58e009a65c7f0689d888244926a2181cc57c9187249489f165fb0397ce11c48`  
		Last Modified: Wed, 02 Feb 2022 03:04:09 GMT  
		Size: 193.0 MB (193011347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68c730bca5b9d974834ddac19217da5a0e76cc52f52c68ad4ccc4f5fa658ee`  
		Last Modified: Wed, 02 Feb 2022 03:03:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e16051f483d149869ad7efe809c42201a7440b100f26b018540ffcd001d889`  
		Last Modified: Wed, 02 Feb 2022 09:45:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250244b00512e8f179084dcbeb1abe17fd9625a70529567186fa8c31aed2b0e9`  
		Last Modified: Wed, 02 Feb 2022 09:45:23 GMT  
		Size: 56.9 MB (56874527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d566a044bc60d05a0cf9db3aa724e1f06f631dcd031a03f426a75fe0b386570f`  
		Last Modified: Wed, 02 Feb 2022 09:45:22 GMT  
		Size: 115.8 MB (115785000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d73aacd9235b7c4f67c5f006a4fabc7d4caa4c359f0f1bb0b71989cea3531e75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409157136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a082bc36d6970d243e5b23eda41d746ce7ab7199b4a26b19af757a949f0bcd4`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:50:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:51:08 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 02:51:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:51:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 02:51:41 GMT
CMD ["jshell"]
# Wed, 02 Feb 2022 05:17:54 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 05:17:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 05:17:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 05:17:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 05:17:58 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 05:18:56 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 05:18:57 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 05:18:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 05:19:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0154b8e60d06ef2e654b6fc885e6b2f15bdad4767412580dc35e38d769ec3`  
		Last Modified: Wed, 02 Feb 2022 02:56:28 GMT  
		Size: 27.4 MB (27368116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f5db094d582e842589bc382a2296eebdafdb129dcb60a4eb14f71a4cfd09a`  
		Last Modified: Wed, 02 Feb 2022 02:58:51 GMT  
		Size: 190.0 MB (190040341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81662ef551f6d7a72b6a95dc68e3a541a1f0588dcc5f010a9ff2046d7928c8c`  
		Last Modified: Wed, 02 Feb 2022 02:57:37 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e3bf878e8775487c11617df812b18afa747113e4dcf71ce0653910b3b4183d`  
		Last Modified: Wed, 02 Feb 2022 05:24:14 GMT  
		Size: 4.3 KB (4342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f404eaabf3f486196691153adc4903ca565ac4772928244f98a991e6b48d54e`  
		Last Modified: Wed, 02 Feb 2022 05:24:51 GMT  
		Size: 51.9 MB (51896377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62322f345c950324a3373b13a35f6d6a76850053f1b9d39d86b9ee10c0cda34d`  
		Last Modified: Wed, 02 Feb 2022 05:24:47 GMT  
		Size: 115.8 MB (115785048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0b77fcfcb6d3fefa491182271fbf544112f09961bd23b694f298a03fb3da5a68
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.8 MB (418776033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8e7b97563bb86147d77a946a05e9b40e3f2f6d58797ef2d609cb72fdac0da`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 05:04:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:04:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:04:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:04:27 GMT
CMD ["jshell"]
# Wed, 02 Feb 2022 07:18:01 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 07:18:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 07:18:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 07:18:04 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 07:18:05 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 07:18:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 07:18:26 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 07:18:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 07:18:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30d06458f35ec294f2441fb9f45188c88e217201cc30e2baee1a00f165107e`  
		Last Modified: Wed, 02 Feb 2022 05:08:05 GMT  
		Size: 29.4 MB (29377028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95752d16178872c9e5f34811bd97c83d50941229bb0d4cea7fcbb09d4d3bc6a`  
		Last Modified: Wed, 02 Feb 2022 05:08:57 GMT  
		Size: 189.9 MB (189944690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74948799fe0acb05bf469b4fffd0689940628fc96f47e4f267b8c96ebef5e9`  
		Last Modified: Wed, 02 Feb 2022 05:08:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f14cbbd72282c24fb1045d74f3602d2b69d10dd309e7d55df8df19398b6b193`  
		Last Modified: Wed, 02 Feb 2022 07:21:26 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4d139655ce6fb1630b1e58e461b55c66637eebf8c1d3cb663dc8888fc1a79f`  
		Last Modified: Wed, 02 Feb 2022 07:21:35 GMT  
		Size: 56.5 MB (56495574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c097088225bfed34e047f2dc96598ccdd7af170b842c79d9b025f5706649bb`  
		Last Modified: Wed, 02 Feb 2022 07:21:33 GMT  
		Size: 115.8 MB (115784661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:7817bbf76d8a56060f02b80069519e5122f2ceab97c0970e7ec49406952c5b85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434760423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c213995e76b4ee7d5c6b3b35b01018b080f4b56278f900d0efc6106669a1ad`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:20:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Feb 2022 22:21:58 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 01 Feb 2022 22:22:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 01 Feb 2022 22:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 22:22:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 01 Feb 2022 22:22:40 GMT
CMD ["jshell"]
# Tue, 01 Feb 2022 22:52:56 GMT
CMD ["gradle"]
# Tue, 01 Feb 2022 22:52:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 01 Feb 2022 22:53:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 01 Feb 2022 22:53:08 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 01 Feb 2022 22:53:10 GMT
WORKDIR /home/gradle
# Tue, 01 Feb 2022 22:55:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 01 Feb 2022 22:55:23 GMT
ENV GRADLE_VERSION=7.3.3
# Tue, 01 Feb 2022 22:55:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Tue, 01 Feb 2022 22:55:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68048c5f723dff42c861f929c10dd67f192df5e872bf74f8d1bf6d2c67fb879`  
		Last Modified: Fri, 07 Jan 2022 03:26:29 GMT  
		Size: 31.1 MB (31123694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827db9da7009a7dd2d0c14c1e3f9010d7748aa866d82c6b515f36e1e29766e45`  
		Last Modified: Tue, 01 Feb 2022 22:30:14 GMT  
		Size: 190.0 MB (189983498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2280477aaf91f2b8152dd38a3b4a64c9bfe542963f1a238e025e2d6dc5478702`  
		Last Modified: Tue, 01 Feb 2022 22:29:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33896a299d9a315585dfed3b4bacdf246a994551214318b9188f9fc280296acb`  
		Last Modified: Tue, 01 Feb 2022 22:59:30 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f311b92d1414e16c11afe53c164e3321a3fcdc306914f0e020689f04c60018`  
		Last Modified: Tue, 01 Feb 2022 22:59:44 GMT  
		Size: 64.6 MB (64576802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973db6faddb486313dcb142bd6a7ffb5afe120355c0e49a43d5bf5803a0f55d`  
		Last Modified: Tue, 01 Feb 2022 22:59:41 GMT  
		Size: 115.8 MB (115785007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:62f92cdc8f491e0515d5d2a2a6a0558ea694d1c1c5c7ff250ca4681322c5b952
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.4 MB (407439386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820b549d18a6331e8c4bfbd84503816696a9d1e354a56a515af0051f03f7beb`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:22:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:24:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:24:41 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 02:24:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:25:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:25:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 02:25:01 GMT
CMD ["jshell"]
# Wed, 02 Feb 2022 04:39:12 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 04:39:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 04:39:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 04:39:13 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 04:39:13 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 04:41:33 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 04:41:38 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 04:41:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 04:41:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1759c477ed4396a58633b60f32e9ec18132879182ced16e097eccef500139a18`  
		Last Modified: Wed, 02 Feb 2022 02:26:54 GMT  
		Size: 27.9 MB (27942553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61974a23bb5d5acb0aa111264ab430e0dc84f3f62d747a9347fafd9ee6595c5c`  
		Last Modified: Wed, 02 Feb 2022 02:27:27 GMT  
		Size: 180.4 MB (180427209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3c9a9f59cb88c696027b903bfb06d31ab3d36c48d995c338a32923df155468`  
		Last Modified: Wed, 02 Feb 2022 02:27:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc56ac770c36b266fcc34f4544d2c05f3f767bc495af3fd33dd6dd4e92f8df2`  
		Last Modified: Wed, 02 Feb 2022 04:43:47 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6719d6490147a74fc326cfa8752ffb78e7bbaa7a14fd9f6d752012c49e25ef19`  
		Last Modified: Wed, 02 Feb 2022 04:43:56 GMT  
		Size: 56.2 MB (56161338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9381d1e551a0802a86c3ddb225a60984dee678b34b5e9d11fa98c60cfd7ee51`  
		Last Modified: Wed, 02 Feb 2022 04:43:55 GMT  
		Size: 115.8 MB (115785024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
