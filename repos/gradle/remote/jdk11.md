## `gradle:jdk11`

```console
$ docker pull gradle@sha256:c10da1b48fcd574b96f5f6e2f97c86d912692f8133f5f70944ec1857cf09e3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:88ba97eaabf853cd95cc801561df56ca0b8c2ca9d132cf20a0731559123bf494
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420058573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75571ce3cb2d51b2221c03f0edb1d231fcf33f513bec7d64fb33a2ea4446f39`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:04:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:05:03 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 02:05:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:05:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:05:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 02:05:11 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 08:53:21 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 08:53:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 08:53:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 08:53:21 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 08:53:22 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 08:53:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 08:53:42 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 08:53:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 08:53:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11e2aa9202b3c11a943dfa8adc2bef4462ab2165124b84051d10250faff2a0`  
		Last Modified: Fri, 22 Apr 2022 02:08:16 GMT  
		Size: 16.0 MB (16030117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad84658d52fe149e3020e7261c93298780f9b9f04585861a5e27c5755d1fae2`  
		Last Modified: Fri, 22 Apr 2022 02:09:07 GMT  
		Size: 193.9 MB (193949730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8284780b418ad5b8dc9537277429854aef2ede1ccf5fc9ec82dfd6fc45b740c`  
		Last Modified: Fri, 22 Apr 2022 02:08:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463b795e18d40e62d3fddefb0b70567febc5a50a9b96f0310b20582295522b92`  
		Last Modified: Fri, 22 Apr 2022 08:56:48 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8789fd157aa817c0a3e937ecee0f7a1a799c506ac6fe1fc13b40711313c0c4c`  
		Last Modified: Fri, 22 Apr 2022 08:57:00 GMT  
		Size: 65.6 MB (65641212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec0c6b5b95f7c3d213defd32fcdeddcf58e16b09039704e4f8f01b931cbbfd1`  
		Last Modified: Fri, 22 Apr 2022 08:56:55 GMT  
		Size: 115.9 MB (115866995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:1b178e7711f8a7600a32b509cebcd1ed8de8bab63514bc67e0448273befa317b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396711879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fe831a9dd46acb6383092eb2c6eb47f18fdc5ffa10e57ce811f9a68187c926`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 Apr 2022 21:52:21 GMT
ADD file:9f59ddec8394f9caab43f06cc89a42cf98b954a4704adcde23a874a6fbb1c15d in / 
# Fri, 22 Apr 2022 21:52:22 GMT
CMD ["bash"]
# Sat, 23 Apr 2022 00:16:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 23 Apr 2022 00:17:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 23 Apr 2022 00:18:50 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 23 Apr 2022 00:19:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 23 Apr 2022 00:19:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Apr 2022 00:19:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 23 Apr 2022 00:19:19 GMT
CMD ["jshell"]
# Sat, 23 Apr 2022 06:58:49 GMT
CMD ["gradle"]
# Sat, 23 Apr 2022 06:58:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Apr 2022 06:58:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 23 Apr 2022 06:58:52 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Apr 2022 06:58:52 GMT
WORKDIR /home/gradle
# Sat, 23 Apr 2022 06:59:44 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 23 Apr 2022 06:59:45 GMT
ENV GRADLE_VERSION=7.4.2
# Sat, 23 Apr 2022 06:59:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Sat, 23 Apr 2022 06:59:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:cae38e1acea3c4adf05af9bcb2081c5bd7b91154184db4b1cdc06deb53699b45`  
		Last Modified: Tue, 19 Apr 2022 13:14:36 GMT  
		Size: 24.1 MB (24074069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3370d7b9d77ae5385f189dfcf90d988f7c40b2805c83edeff9d58de940f5135`  
		Last Modified: Sat, 23 Apr 2022 00:26:13 GMT  
		Size: 14.9 MB (14901158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5044893d50ecebc9ce589c1b57ebf23a2aedfe765dbc344bcb76f776805b11da`  
		Last Modified: Sat, 23 Apr 2022 00:28:46 GMT  
		Size: 181.8 MB (181831101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368c8ad786f96661929b3333efec484fd3fd1c2b045da4f91ecf67c47ebb1a34`  
		Last Modified: Sat, 23 Apr 2022 00:27:36 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1533cf870f400a857d2edfba00925fbc665a13e68abd8bbc7edfe7b3eb8a72`  
		Last Modified: Sat, 23 Apr 2022 07:08:15 GMT  
		Size: 4.4 KB (4351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f86d7522d751dfb836a8b70cb8c7bb24c6678871c4ecc336085f67c468a1c7`  
		Last Modified: Sat, 23 Apr 2022 07:08:57 GMT  
		Size: 60.0 MB (60034078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b3dc595b62cd719edd0686b227f365f459547e1a1deba5aa1f8cec833074b`  
		Last Modified: Sat, 23 Apr 2022 07:08:48 GMT  
		Size: 115.9 MB (115866960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:afd4e7894123d3b95732f66add4ee12d8d60a175dbfeea78ffef2c569472418d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (414975357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a72a1785705c2000ddefaba2b8a48c2491f3334524042980a4cb68bda78d3e6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 Apr 2022 00:54:11 GMT
ADD file:6ca4a270cea388f6267a1c7739fd787a34793f48bf8480740a383b5e73299af2 in / 
# Fri, 22 Apr 2022 00:54:11 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:56:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:56:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:57:27 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 02:57:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:57:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:57:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 02:57:40 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 08:17:49 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 08:17:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 08:17:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 08:17:51 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 08:17:52 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 08:18:14 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 08:18:15 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 08:18:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 08:18:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:61e1864f78be077e322819a4ce1e09da9389c8119cf552629dc048b713a3f42b`  
		Last Modified: Tue, 19 Apr 2022 13:13:57 GMT  
		Size: 27.2 MB (27169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89015ff109b922c48ff7f1847b2e63f33dc54bd022e11f479dbed2eb7fb5da0`  
		Last Modified: Fri, 22 Apr 2022 03:02:05 GMT  
		Size: 15.9 MB (15895876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0583ced0a0f5ee8da09f48548bfcff5152185c9dceaf6dd971b90e71e6bb183b`  
		Last Modified: Fri, 22 Apr 2022 03:03:04 GMT  
		Size: 190.7 MB (190684900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446baebacc4f1062ced5d72ed5d94ae87a784ed870325a7cce17f55a6c90dc1e`  
		Last Modified: Fri, 22 Apr 2022 03:02:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8913adfbcafcca47a3fc12c188a33e3721e2df1e88e5f7782e6dfbdafabb2a`  
		Last Modified: Fri, 22 Apr 2022 08:22:06 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b3f70ccfa39ce2e02fe3cd770524504ec4f1deb4f49c279d42b1dd77fcb554`  
		Last Modified: Fri, 22 Apr 2022 08:22:17 GMT  
		Size: 65.4 MB (65354159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4348cf1aa0e4a79d0a84508891be59590767f51f6a2cd70a1a94fe293a7a0ba9`  
		Last Modified: Fri, 22 Apr 2022 08:22:14 GMT  
		Size: 115.9 MB (115866840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:9a01ac22ac52c8a6fb0e7514b6eaeebaf89db47c5286ad8991ccb3b6eb973ab1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416221436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c64fc6a9062a7cf77b85b17d5c1ca54914654d1e4dde369761e4a520dddb4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 Apr 2022 08:08:14 GMT
ADD file:f1c44e93e7a6c0fb06800e11460dc680e252dff4a20297ab2eed86e559398616 in / 
# Fri, 22 Apr 2022 08:08:17 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 09:45:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 09:46:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:48:21 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 09:48:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 09:48:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 09:48:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 09:48:52 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 13:34:34 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 13:34:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 13:34:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 13:34:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 13:34:59 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 13:38:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 13:38:34 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 13:38:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 13:39:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:30c729c4ac9a0cf192e6c3e5618b0e930ca2ecdd73c01d9c5fed5b0707eb8836`  
		Last Modified: Tue, 19 Apr 2022 13:15:19 GMT  
		Size: 33.3 MB (33290375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc56b8d6fd0bb34b3c200e96dec3af60f79a6f302365ccc050f056b1d5993a3`  
		Last Modified: Fri, 22 Apr 2022 09:58:22 GMT  
		Size: 17.2 MB (17204271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181f30ca4884426b0332bd539fd7426892f1845df8600112b994114abe8b5ba4`  
		Last Modified: Fri, 22 Apr 2022 09:59:31 GMT  
		Size: 175.8 MB (175842428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d03404a0d0d2384af64af9c3eae41c8c99e28e56dcaf4508a3d5284df916b3`  
		Last Modified: Fri, 22 Apr 2022 09:59:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7493016de4263406cdd8f8fc48644daa5693ddd9934feae75f4a5c72f24dca96`  
		Last Modified: Fri, 22 Apr 2022 13:55:49 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc7b8425b2d326177383513864d9e140e6fc362b679ebe67d41090568042ade`  
		Last Modified: Fri, 22 Apr 2022 13:56:04 GMT  
		Size: 74.0 MB (74012833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b06910757c7d64874fccb7ca8ccd636b68cf409e5e514cca8eb2547dbd3984`  
		Last Modified: Fri, 22 Apr 2022 13:55:59 GMT  
		Size: 115.9 MB (115867002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:810bbddcec1ede5a648dc13bb22b6fca09356d831f01028e1cb4facc06f4a27d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391882216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305db4364e086811c2ca7a65f72171a3287285fba41d15a960d365e46892b975`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:54:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 01:55:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:55:42 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 01:56:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 01:56:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 01:56:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 01:56:19 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 06:17:16 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 06:17:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 06:17:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 06:17:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 06:17:20 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 06:18:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 06:18:27 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 06:18:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 06:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad99882b01b0ab3e7045a65b2c93f1319b8763364d776de22578aaade5be51`  
		Last Modified: Fri, 22 Apr 2022 02:02:24 GMT  
		Size: 15.7 MB (15738876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3294de8307a38f2c4061d12cf71b6382efb9e046c70432db9e5a14e8e348d987`  
		Last Modified: Fri, 22 Apr 2022 02:02:33 GMT  
		Size: 168.4 MB (168352457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457b92a9eb5921a8ab283e8d97618c145c24ca549b54a08dc193bfba91563d6`  
		Last Modified: Fri, 22 Apr 2022 02:02:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39335925e264109537e714d1a2fc9a19f6468e95d4b4c58b69c41f8324c116fa`  
		Last Modified: Fri, 22 Apr 2022 06:24:07 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff9f511e5f57840f32d8ad189cf3cfc264e4f4fc7ae4b5042ce8a9a7285123d`  
		Last Modified: Fri, 22 Apr 2022 06:24:18 GMT  
		Size: 64.8 MB (64833681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ad0faeae0eafeba35f626e49131df62ce162d01874ee8c57573d66712d5c81`  
		Last Modified: Fri, 22 Apr 2022 06:24:13 GMT  
		Size: 115.9 MB (115866958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
