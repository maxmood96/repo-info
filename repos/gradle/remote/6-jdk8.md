## `gradle:6-jdk8`

```console
$ docker pull gradle@sha256:80c07f945f7f08136427cfe1505c120f829096c5e83fcf94ad1fc5d11e527f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:6-jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:0b3c554f48d77652a834453c3dcadb8e894939282f969323d3714a4531346e19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321573853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae0400ff7f7d6001b1b73164854ebd78cbebbedb8b471f0e72d15db12d7a5fe`
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
# Sun, 20 Mar 2022 15:06:16 GMT
ENV GRADLE_VERSION=6.9.2
# Sun, 20 Mar 2022 15:06:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sun, 20 Mar 2022 15:06:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:b051e710d9094309bb3dc12639391d40a4070600433d6f3e0bee001ca9808bd4`  
		Last Modified: Sun, 20 Mar 2022 15:09:32 GMT  
		Size: 107.7 MB (107690372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:fefe476f16d3d556cf615804b1847535cfcd07dffaa0ec9157abea82209c5901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306032585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cc373dca63cb97f264457a25c8b61caa53c6f2fe6e98d5c225be76db6612e9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Mar 2022 07:32:41 GMT
ADD file:2e353e40ad52bb1b5a10aafb7912657744b02d096925b5bfc6e925ebf7cddede in / 
# Fri, 18 Mar 2022 07:32:42 GMT
CMD ["bash"]
# Sun, 20 Mar 2022 06:32:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 20 Mar 2022 06:33:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 06:33:29 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sun, 20 Mar 2022 06:33:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sun, 20 Mar 2022 06:33:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 06:33:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:19:13 GMT
CMD ["gradle"]
# Sun, 20 Mar 2022 20:19:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 20 Mar 2022 20:19:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sun, 20 Mar 2022 20:19:16 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 20 Mar 2022 20:19:16 GMT
WORKDIR /home/gradle
# Sun, 20 Mar 2022 20:20:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sun, 20 Mar 2022 20:23:28 GMT
ENV GRADLE_VERSION=6.9.2
# Sun, 20 Mar 2022 20:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sun, 20 Mar 2022 20:23:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:260b2dce5be1e0d17bf9e2ec2bbde587e5023ab1b48278ddf8396dcfc8eb7e99`  
		Last Modified: Fri, 18 Mar 2022 07:36:23 GMT  
		Size: 24.1 MB (24073481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53338e80157a2d8d75acf73c7d6a401a71fb6f4b5d452c1922a2452a516efef`  
		Last Modified: Sun, 20 Mar 2022 06:40:48 GMT  
		Size: 14.9 MB (14902387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c806a21d58f306110e7b06ea5e511a3e555f24307660c718dd5fcf77ed121`  
		Last Modified: Sun, 20 Mar 2022 06:41:20 GMT  
		Size: 99.3 MB (99328788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31595617860e1aea118127a94998e05c796633ca7d15593e524b13dd4e631492`  
		Last Modified: Sun, 20 Mar 2022 06:40:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0bd1ac178903118f95e6f6478d0c04addacb8bc25f00d7ec76864fdfa42bc2`  
		Last Modified: Sun, 20 Mar 2022 20:27:17 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5468916d41ec5fff46f5a4c1f3060bb3247e665f9e110220f80a68645634a749`  
		Last Modified: Sun, 20 Mar 2022 20:28:00 GMT  
		Size: 60.0 MB (60033050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f251ac93509986761c80a89b62e6f3629d8a4f212b8ae9bdf2f77f378044a0a0`  
		Last Modified: Sun, 20 Mar 2022 20:31:32 GMT  
		Size: 107.7 MB (107690373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6033625281d3bfdbfac444e05e5a7c1a0747c016b3cc3698b626f57589a0aec5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318843434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dda25dd85d35859b96ed125e6dcf8f42a27d6fe92df60d436e79a0624692ae`
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
# Sun, 20 Mar 2022 00:30:21 GMT
ENV GRADLE_VERSION=6.9.2
# Sun, 20 Mar 2022 00:30:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sun, 20 Mar 2022 00:30:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:4184aa4e63682a1c63b7148b06c85920ab1b50695f9ad8703cbc2926cdda941d`  
		Last Modified: Sun, 20 Mar 2022 00:34:03 GMT  
		Size: 107.7 MB (107690355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:4be75bb7f101db204a8eae204910d1a089a01b6eea13d48caf6389522024c0a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333339863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778b70723ed72fe45943ce545889d8ef44a96752607a24425f874a67643a8a07`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:10:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='0666c466b8aefcc66ab25aea9c0605f5c6eda3b174b1b817a4e4e74da0de0365';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:10:57 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 23:42:25 GMT
CMD ["gradle"]
# Sun, 20 Mar 2022 23:42:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 20 Mar 2022 23:42:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sun, 20 Mar 2022 23:42:37 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 20 Mar 2022 23:42:41 GMT
WORKDIR /home/gradle
# Sun, 20 Mar 2022 23:44:14 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sun, 20 Mar 2022 23:53:43 GMT
ENV GRADLE_VERSION=6.9.2
# Sun, 20 Mar 2022 23:53:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sun, 20 Mar 2022 23:54:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf02142be739e4453e43938b7cf32c34fe354f87e24ee8e76e176a216d5243a`  
		Last Modified: Sat, 19 Mar 2022 20:18:24 GMT  
		Size: 101.1 MB (101145810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ad2446a6b6ceb15ea89ad3c5ccd8efa87389847092ee891c66549442f6077`  
		Last Modified: Sat, 19 Mar 2022 20:18:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9ab54aad1d6fd2efaa538bde7431d6edb5d40396e2d0e0aad64dc2234f6a6`  
		Last Modified: Sun, 20 Mar 2022 23:57:51 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc934a2a91f88b06f262a6b5a74f8a559a24b02910915fb834ac3f36dde36e16`  
		Last Modified: Sun, 20 Mar 2022 23:58:05 GMT  
		Size: 74.0 MB (74001462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f9b2532775462f4fba6d5789c1f0324c907122198fc8e5f7436967172c33b7`  
		Last Modified: Mon, 21 Mar 2022 00:00:18 GMT  
		Size: 107.7 MB (107690376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
