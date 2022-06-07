## `gradle:7-jdk-jammy`

```console
$ docker pull gradle@sha256:125f0d3379c5def4cb4e91edf57e7c775d9156a385581fac70b06b4b2c04b83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `gradle:7-jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:58f56046624ac0b6173c2ccd954f18ca4a3aab6033efd606abef10e1f5b98ac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 MB (407025031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f353b28631ebda262f46c6af6f33f2a22620c5ed1a2dfdd98df9b01cd350cd5`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:15:58 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:16:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:16:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:16:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:16:08 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 04:20:02 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 04:20:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 04:20:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 04:20:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 04:20:03 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 04:20:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 04:20:18 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 04:20:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 04:20:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160c99d3182b28de91f5c2c165e40fe309db075058fa23129c7dc2b4e2852b0e`  
		Last Modified: Tue, 07 Jun 2022 00:22:32 GMT  
		Size: 16.7 MB (16660695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07a736be37f1d15b9e60b62cb6080265876f34f4e59124da4ce8fc14c478517`  
		Last Modified: Tue, 07 Jun 2022 00:22:43 GMT  
		Size: 192.5 MB (192474640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb991d49ce62266dbe97f5cacb927c3bf16683663f867c4067dbf4ed2865adf3`  
		Last Modified: Tue, 07 Jun 2022 00:22:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c51e5ac488864342dbd6c7a8f31935070965078d4359baf4421bebb9f141af8`  
		Last Modified: Tue, 07 Jun 2022 04:27:13 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaadd5423c3651ac85d8bfb8e1c8de88ca1956ef12087f062395dacfc37b303`  
		Last Modified: Tue, 07 Jun 2022 04:27:22 GMT  
		Size: 51.6 MB (51594452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358733492b020750d0a22a2b8a8a3ed0b0dfad1655488313129477a5c05dfd33`  
		Last Modified: Tue, 07 Jun 2022 04:27:19 GMT  
		Size: 115.9 MB (115867004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:66ae82e9714f159e916f4bb359b4c7781f5949b998329735809cec6b9846b3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404497360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6733e941b6ed73ebe9094b366672d0885562a2e1cbb28b9a18195c46696120`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 22:59:30 GMT
ADD file:78ae02cb00d8cc788584388eeb9fdc5ca6b45f502d33acd7f6efe7fc2a325683 in / 
# Fri, 29 Apr 2022 22:59:31 GMT
CMD ["bash"]
# Thu, 26 May 2022 21:58:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 26 May 2022 22:03:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 26 May 2022 22:03:05 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Thu, 26 May 2022 22:03:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 26 May 2022 22:03:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 May 2022 22:03:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 26 May 2022 22:03:36 GMT
CMD ["jshell"]
# Thu, 26 May 2022 22:38:29 GMT
CMD ["gradle"]
# Thu, 26 May 2022 22:38:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 26 May 2022 22:38:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 26 May 2022 22:38:31 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 26 May 2022 22:38:32 GMT
WORKDIR /home/gradle
# Thu, 26 May 2022 22:39:21 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 26 May 2022 22:39:22 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 26 May 2022 22:39:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 26 May 2022 22:39:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:5a3411c136d8a6da4e9d7d3abcbfc94f59ecb2935fd02cad49be6a79c899fcaa`  
		Last Modified: Fri, 29 Apr 2022 23:03:59 GMT  
		Size: 27.0 MB (27015834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1e324620b2d6e069ce59fade629688b54563b78a4b4350c24a8d523f2e638f`  
		Last Modified: Thu, 26 May 2022 22:13:52 GMT  
		Size: 18.6 MB (18601195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf780d747c3febfb0be8ab372baecd9f69d703a80cf6d6a07c39a2da8b09ca2`  
		Last Modified: Thu, 26 May 2022 22:14:53 GMT  
		Size: 189.4 MB (189425265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bb2a789887b9aebbb2d955a09f3d62bc83c1ed9fdf1a91595b3b3a73d76b3b`  
		Last Modified: Thu, 26 May 2022 22:13:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd9f87c7a2235ead2a4e5a559c75a419f55a0b669dfcca5b737acb7029e930d`  
		Last Modified: Thu, 26 May 2022 22:47:24 GMT  
		Size: 4.4 KB (4354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881d2d1aea29c9026775b7123e02c0dd57bdae313b86bb03893f580bac92c8cd`  
		Last Modified: Thu, 26 May 2022 22:48:03 GMT  
		Size: 53.6 MB (53583550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0f83e54bddfb05be969da6f30da0fc1583887f25c2af8fd5ca005e478350c1`  
		Last Modified: Thu, 26 May 2022 22:47:57 GMT  
		Size: 115.9 MB (115867002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a563b20ea9f96bef9dd805e8026c8805d8b2800847dbab4c718d5238cb86b41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404741244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c7838e4906fe265e0a7ebe62085d6236554b915ed25e2a27a82aa0cf9e6aa6`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:34:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:37:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:37:24 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 06:37:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:37:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:37:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:37:33 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 07:04:48 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 07:04:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 07:04:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 07:04:51 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 07:04:52 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 07:05:13 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 07:05:14 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 07:05:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 07:05:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05b1ade9954ed8f53cec97e324b11b1651b87e1cc39bcaa916ed2a7aacc6c4`  
		Last Modified: Tue, 07 Jun 2022 06:45:20 GMT  
		Size: 18.1 MB (18092093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b9116ed1268ba49cab644bbe5f713c73f9c49b3883c8554fd7459fb6f9e11a`  
		Last Modified: Tue, 07 Jun 2022 06:45:35 GMT  
		Size: 191.2 MB (191243896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64039e07e333a2d40c8f7049ce715b4b8c8011ced47f5ead589d68e2b599564`  
		Last Modified: Tue, 07 Jun 2022 06:45:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bff0ac8bbe56c4eecf486b52abca1295e42cdf4402fc1fad71ca46f034956fb`  
		Last Modified: Tue, 07 Jun 2022 07:14:48 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9e2a346b2c34453a5cb66d723fe3a6b7b51871c31c7dcfaffd8cc58d8bb2e2`  
		Last Modified: Tue, 07 Jun 2022 07:14:57 GMT  
		Size: 51.2 MB (51155763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3ebe9b7756e4e67198e9083dd6138ef2d4494375b1d2e646f00d09f6ef753`  
		Last Modified: Tue, 07 Jun 2022 07:15:02 GMT  
		Size: 115.9 MB (115866841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:2cd49df0d8d87f3a41d1912e24ce9c4919db82f320251754ae240bfdd4e5eb44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392636964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185fa8865923c44438247398afeaa5e422c7eb1fb401988f93ed14543654807b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 04:05:41 GMT
ADD file:5412b0d16961079a78b96411ca23f1838ac09c2fae839829476380b5389e49f8 in / 
# Tue, 07 Jun 2022 04:05:45 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:33:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:37:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:37:40 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 06:38:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:38:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:38:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:38:29 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 07:08:38 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 07:08:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 07:08:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 07:08:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 07:08:41 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 07:09:14 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 07:09:19 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 07:09:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 07:09:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6fa1296f44090f6150dfb96d6ae217a58b9d66c56d7a986c35657df6bd1a89f0`  
		Last Modified: Tue, 07 Jun 2022 04:08:13 GMT  
		Size: 28.6 MB (28638482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd8c93abff5baf988449855146fa80db180ea7004a449308cc565413cfd99c9`  
		Last Modified: Tue, 07 Jun 2022 06:44:14 GMT  
		Size: 16.4 MB (16427939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b8f831f238627d9fdf72d4a0e18828b1c4ba6b01d6107d918923eb6625bc5`  
		Last Modified: Tue, 07 Jun 2022 06:44:24 GMT  
		Size: 180.4 MB (180405008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42a3693b024df7b86b24e45fafad747c71cebbbc9ede76054ecb66db434600`  
		Last Modified: Tue, 07 Jun 2022 06:44:12 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a922dc284074e76c16cbd154fcae23b768e43b7fd3e4fa38f480f1d1b718a61`  
		Last Modified: Tue, 07 Jun 2022 07:18:40 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563f97e20b72d1ec79c28f8dcf19a8610101d19fe193aab115ed9a3a05189e5b`  
		Last Modified: Tue, 07 Jun 2022 07:18:48 GMT  
		Size: 51.3 MB (51294008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9efe0491477f7d278b2c52926668d758e9bf1bb1011e58906ebf2e6a1eb7825`  
		Last Modified: Tue, 07 Jun 2022 07:18:46 GMT  
		Size: 115.9 MB (115866997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
