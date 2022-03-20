## `gradle:jdk8`

```console
$ docker pull gradle@sha256:5028b082d4f55c74f03911fea3608a2fa2a43df462e608d35dbf9a579ec2f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:3fda206db68d5bed3cec647e2cd106032c2679b3c0838fbeca3533d1336e559e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329748850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e7c857f5daabeb91ec32f2b1675c9fad984b1d334cbb252ec497e58229d148`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 01:15:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 01:16:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 01:16:23 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 01:16:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 01:16:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 01:16:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 15:04:34 GMT
CMD ["gradle"]
# Sun, 20 Mar 2022 15:04:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 20 Mar 2022 15:04:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sun, 20 Mar 2022 15:04:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 20 Mar 2022 15:04:35 GMT
WORKDIR /home/gradle
# Sun, 20 Mar 2022 15:05:03 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sun, 20 Mar 2022 15:05:04 GMT
ENV GRADLE_VERSION=7.4.1
# Sun, 20 Mar 2022 15:05:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
# Sun, 20 Mar 2022 15:05:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bca86330b80add24b2c91216395ff9d2a2e815b00c22f770434df27fef5335`  
		Last Modified: Sat, 19 Mar 2022 01:22:07 GMT  
		Size: 16.0 MB (16031105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf88b1d057b109c791dc01f9ee1a5d36de52352b1938797ec83c674ca7f0c`  
		Last Modified: Sat, 19 Mar 2022 01:22:15 GMT  
		Size: 103.7 MB (103656373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40efe6860cb6b0c0a462ecdfbe48ac35d21fdce9e04a18cb9f4a5c2f9e90f23e`  
		Last Modified: Sat, 19 Mar 2022 01:22:02 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5992c38e2977a64eae4c8332a3b9ca652105f55e564d788b3e7eb923d06d2bf`  
		Last Modified: Sun, 20 Mar 2022 15:07:38 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfb493856bc2a375bed2a3e0eda93011b59d3292e75aa9fdd22d1d604c4b892`  
		Last Modified: Sun, 20 Mar 2022 15:07:50 GMT  
		Size: 65.6 MB (65625574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e5e4db2a0fb5707a736ec4ef12da6b79715351cab3112266d2e5302006daf7`  
		Last Modified: Sun, 20 Mar 2022 15:07:45 GMT  
		Size: 115.9 MB (115865369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:6d280547f7b1e6e0e42483f5faae25ca1812089ab1a1abec4f463041f8c5e79a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314208291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8defe8a2bf9b7a2945abf34d52c1a7e209447b842ce4642cce46afdcca81f60`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:31 GMT
ADD file:984d3d8b31abd025bb9be52f42d60245a76b1ee991f286db819ae204da45390c in / 
# Thu, 03 Mar 2022 21:21:32 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 04:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Mar 2022 19:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:58:24 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Mon, 07 Mar 2022 19:58:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:58:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:58:49 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 07 Mar 2022 21:54:42 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 21:54:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 21:54:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 21:54:45 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 21:54:45 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 21:55:36 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 10 Mar 2022 19:42:31 GMT
ENV GRADLE_VERSION=7.4.1
# Thu, 10 Mar 2022 19:42:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
# Thu, 10 Mar 2022 19:42:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:12a77aaceb8aa1438ebb61cb4904d74fc225cfa20464a060980580674a0a31e9`  
		Last Modified: Thu, 03 Mar 2022 21:25:09 GMT  
		Size: 24.1 MB (24073718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aaac75a0138a59e98810b993ebce72dbe24ae9f2b9ef694f4b9d0f7f2a63d1`  
		Last Modified: Mon, 07 Mar 2022 20:05:47 GMT  
		Size: 14.9 MB (14902332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26da233459ab6def22dae2a016690a4ea6d3c189ffb523fe21fb04365b7ad5df`  
		Last Modified: Mon, 07 Mar 2022 20:06:19 GMT  
		Size: 99.3 MB (99329244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec7735019cc42927741d9ab56f4d70a7fd1f618de493a59bdd1434e5cccca4f`  
		Last Modified: Mon, 07 Mar 2022 20:05:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74b9680f6cdfcff9d13756b9b1679627e8fac55517e03e8de06339807760c14`  
		Last Modified: Mon, 07 Mar 2022 22:02:44 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8db927c51099e5593aa9ccab3fec7de771a03dc022e7f85a30f09a9e61dc190`  
		Last Modified: Mon, 07 Mar 2022 22:03:28 GMT  
		Size: 60.0 MB (60033134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc73e07c30fc07b48fd2b5a2a00e466f89f029b35b54a1fa3e6840c6e7b52e6`  
		Last Modified: Thu, 10 Mar 2022 19:47:33 GMT  
		Size: 115.9 MB (115865356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f469e6102c3b357cb91e06d78418ba976a4b6bd408bfc9e612d1891e300dd1db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (327018440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81eeaa0cbcb2bdcb0b91b0a5a3c8194adb5e2f1052789a4ceca413ea7c16947`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:28:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 15:28:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:28:31 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 15:28:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 15:28:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 15:28:41 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 00:28:09 GMT
CMD ["gradle"]
# Sun, 20 Mar 2022 00:28:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 20 Mar 2022 00:28:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sun, 20 Mar 2022 00:28:12 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 20 Mar 2022 00:28:13 GMT
WORKDIR /home/gradle
# Sun, 20 Mar 2022 00:28:37 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sun, 20 Mar 2022 00:28:38 GMT
ENV GRADLE_VERSION=7.4.1
# Sun, 20 Mar 2022 00:28:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
# Sun, 20 Mar 2022 00:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c236902da3463f4b33e5af2f3ff655994cbe47d5e8380294ee6d6a5957b77710`  
		Last Modified: Sat, 19 Mar 2022 15:32:57 GMT  
		Size: 15.9 MB (15897447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d96fe6e260252d5646351de5271418f1d59ae7ba31a009db409bcf331416a`  
		Last Modified: Sat, 19 Mar 2022 15:33:09 GMT  
		Size: 102.7 MB (102746633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb0b74e322b62e8d2b9db9a78da36b4d6992649b69bd01a35489375858a9572`  
		Last Modified: Sat, 19 Mar 2022 15:32:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e57f4f08cfefbb892abe5fe498730aeef83b17b018b7d4f37487b021e41fb`  
		Last Modified: Sun, 20 Mar 2022 00:32:03 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68f543b42680dceaf0f10664b6e9645296038d739811491618f386cc828521`  
		Last Modified: Sun, 20 Mar 2022 00:32:14 GMT  
		Size: 65.3 MB (65334944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776c2a85951e784edb9b83fa7675c05495c99eabe3422beaa3ffa4640377d93`  
		Last Modified: Sun, 20 Mar 2022 00:32:14 GMT  
		Size: 115.9 MB (115865361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:cb1a52abce47b58eed841b99946cdb2b48146bf897ce43af2ce38682792a804e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341515102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b177ee249176e014884e925567adf82e356e5a55235cf04f7976b21ef82c67e2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:30 GMT
ADD file:039f04ac6c5dbbe3fb0a5eee16945cf7c5fb7565751d6bdf8ec0c1102798c1de in / 
# Thu, 03 Mar 2022 20:28:38 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:04:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 23:22:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:24:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Mon, 07 Mar 2022 19:24:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:25:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:25:19 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 07 Mar 2022 19:56:12 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 19:56:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 19:56:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 19:56:25 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 19:56:28 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 19:58:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 10 Mar 2022 18:16:47 GMT
ENV GRADLE_VERSION=7.4.1
# Thu, 10 Mar 2022 18:16:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
# Thu, 10 Mar 2022 18:17:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e5444a57cda4a95f90b0c9446a9e1b47d3d7f69057765bfb54bd4f482542d548
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a16b43de69d1e799ea2cb675e7e605db0ff3a8d692fd326fbde80a370e0676d5`  
		Last Modified: Thu, 03 Mar 2022 20:33:55 GMT  
		Size: 33.3 MB (33292195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daad88923e3aab34fc02032aaddf77f4caa3bd81fe7df9b280ef3fbd2796e10`  
		Last Modified: Thu, 03 Mar 2022 23:36:10 GMT  
		Size: 17.2 MB (17205102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ad16679b810e4a3ef373d8c3be772cf312ca947fad3203750c66e1bc16b788`  
		Last Modified: Mon, 07 Mar 2022 19:36:39 GMT  
		Size: 101.1 MB (101145809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd81dd04415db6772c228ccef9d14a8deace7bf73cb9ef4ddcecf4c619cecd5`  
		Last Modified: Mon, 07 Mar 2022 19:36:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb4fd90200e77e80e7210af4a2441fe77fb09645f293e7487cea3ef3d063074`  
		Last Modified: Mon, 07 Mar 2022 20:11:16 GMT  
		Size: 4.4 KB (4372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56726572e333fccd639e24e38dc7a5b3c7e53620d54b4ef849cc052b8522209c`  
		Last Modified: Mon, 07 Mar 2022 20:11:31 GMT  
		Size: 74.0 MB (74002037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12383064d9056cc7f94ef8ed3be700e4842883367a82bc970b59d2a89800cb8e`  
		Last Modified: Thu, 10 Mar 2022 18:21:17 GMT  
		Size: 115.9 MB (115865426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
