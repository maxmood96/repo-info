## `gradle:7-jammy`

```console
$ docker pull gradle@sha256:b832c8452c1424a81b770400eadca0fa463db1eef19f7c403bf9e8b6288f93b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:c64ec3034697d09752c195477d6de3b7f8d4e918ae93fafcae0d2a89c692d78e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411483223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea61a46a3ce37e9299ead23c9c6d59652fb1dc8ec26539cfa687a0bd0330605`
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
# Thu, 28 Jul 2022 16:22:20 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:30 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 17:06:26 GMT
CMD ["gradle"]
# Thu, 28 Jul 2022 17:06:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 28 Jul 2022 17:06:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 28 Jul 2022 17:06:27 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 28 Jul 2022 17:06:27 GMT
WORKDIR /home/gradle
# Thu, 28 Jul 2022 17:06:43 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 28 Jul 2022 17:06:43 GMT
ENV GRADLE_VERSION=7.5
# Thu, 28 Jul 2022 17:06:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Thu, 28 Jul 2022 17:06:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
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
	-	`sha256:f0a692022c3986777404afbe8e7a8a49f86afcdb46a83d46d466f187fac32aa5`  
		Last Modified: Thu, 28 Jul 2022 16:29:20 GMT  
		Size: 192.1 MB (192148075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd503fe1fc18b64e537625a9a840ec51bcdaa1966c46d9b8a1dfc370f4832c`  
		Last Modified: Thu, 28 Jul 2022 16:29:05 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d830c6c1c7b61340d7338f7e0abe41b4e09b6c317832582df9eaed867f876fea`  
		Last Modified: Thu, 28 Jul 2022 17:12:29 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f559049f34c94fab9f36bd4a5cb04438572d1c98026d79a3e251e725f3ac5c`  
		Last Modified: Thu, 28 Jul 2022 17:12:38 GMT  
		Size: 51.6 MB (51590471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925aa1e8a7e579ae909b297d1174c818bc64d993d1abee8cf3250a4cda77d595`  
		Last Modified: Thu, 28 Jul 2022 17:12:48 GMT  
		Size: 120.7 MB (120655739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:8c324497ab5ff6b35b2c60f328e3dd44e648441fb23cbaa172386f88158d09df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407506111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ffa9f04140341813140f6f37b1b2b7bd5c6cbfb220aae5d18c7832c98da44b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 09:35:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 09:43:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 09:43:02 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 09:43:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 09:43:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 09:43:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 09:43:33 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 11:12:34 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 11:12:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 11:12:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 11:12:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 11:12:37 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 11:13:27 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 15 Jul 2022 17:03:14 GMT
ENV GRADLE_VERSION=7.5
# Fri, 15 Jul 2022 17:03:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Fri, 15 Jul 2022 17:03:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5390c30522c8a66ee1b5710a648276f1950fd75410a08d08df5699afb754d`  
		Last Modified: Tue, 07 Jun 2022 09:59:39 GMT  
		Size: 16.8 MB (16819038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c673e0121186fd60cc06ba1146ff2acacd89cdf5a97872d146a623d2dfb65966`  
		Last Modified: Tue, 07 Jun 2022 10:00:41 GMT  
		Size: 189.4 MB (189425306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe28162d112ce47e212eb0a4cbd582cb2f1f23afe9aef28560f3145a7a3cf7d`  
		Last Modified: Tue, 07 Jun 2022 09:59:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f97fdbcc90b57c53592e2d208f79b59634152d69882bb6ce58f34591d7382`  
		Last Modified: Tue, 07 Jun 2022 11:34:14 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbb6c0f4b1eb29caef19565ba0874d95b40233b52354dfbded4a93bb63641c1`  
		Last Modified: Tue, 07 Jun 2022 11:34:52 GMT  
		Size: 53.6 MB (53584089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373b99800143cb965dcdbc3ef815123f0f5dde3620ab1e5eb36933011f201fd1`  
		Last Modified: Fri, 15 Jul 2022 17:19:45 GMT  
		Size: 120.7 MB (120655737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:87d50c5e289521aa0518880e85fe8f1507a01728f0620c46f1c471ec972d89c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409193619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2ffb17e935ef28b98e5772d1ccebdcb047f4ae1d713f9e462f93a38575b985`
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
# Thu, 28 Jul 2022 15:42:49 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 15:42:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:42:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:42:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:42:59 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 16:28:41 GMT
CMD ["gradle"]
# Thu, 28 Jul 2022 16:28:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 28 Jul 2022 16:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 28 Jul 2022 16:28:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 28 Jul 2022 16:28:45 GMT
WORKDIR /home/gradle
# Thu, 28 Jul 2022 16:29:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 28 Jul 2022 16:29:08 GMT
ENV GRADLE_VERSION=7.5
# Thu, 28 Jul 2022 16:29:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Thu, 28 Jul 2022 16:29:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
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
	-	`sha256:a6903ca3c410fa3b304466bde2d79a771754ad9b25cac5f635e35056fa224634`  
		Last Modified: Thu, 28 Jul 2022 15:50:25 GMT  
		Size: 190.9 MB (190907077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d76277049ff439542e2131f7752121f896aeabfccab8dd33a393e06b9917fb0`  
		Last Modified: Thu, 28 Jul 2022 15:50:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c549f79c20f011c39041acf3e0f6ae24722c8f341a95f33fa03b83f7c5e62c`  
		Last Modified: Thu, 28 Jul 2022 16:36:18 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce0c349150bd9fd4d94a91468277c2f8b5cfca4e8ea831c24f79032a690d607`  
		Last Modified: Thu, 28 Jul 2022 16:36:27 GMT  
		Size: 51.2 MB (51156183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610e470381e2f75d4d2b05ab2cf1298cce340ce94b09372d54a91aa2b627f008`  
		Last Modified: Thu, 28 Jul 2022 16:36:29 GMT  
		Size: 120.7 MB (120655611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:39afed27f0c1283862b49d2029426503496d7061ada4e64da6cd471469f1b1f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.6 MB (421605883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cff5cf86a0008022f93e719db77b0b10e15b752af65db161ee209091ed82a7`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:49 GMT
ADD file:62ec907c651e833838867bd541cf824f5f609ea4e2b19c4b26cec74a57b60470 in / 
# Tue, 07 Jun 2022 05:46:54 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 00:35:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:42:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:31 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 17:00:38 GMT
CMD ["gradle"]
# Thu, 28 Jul 2022 17:00:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 28 Jul 2022 17:00:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 28 Jul 2022 17:00:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 28 Jul 2022 17:00:39 GMT
WORKDIR /home/gradle
# Thu, 28 Jul 2022 17:01:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 28 Jul 2022 17:01:13 GMT
ENV GRADLE_VERSION=7.5
# Thu, 28 Jul 2022 17:01:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Thu, 28 Jul 2022 17:01:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b851cfa9fcbcb74629241502e21ebbae255fe40a2f26949573f278672b65c308`  
		Last Modified: Tue, 07 Jun 2022 05:49:53 GMT  
		Size: 35.7 MB (35717509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271d3996199a8c9ad9db4f7588a0b27613eb16f8a0ebaef74b5c3f327011070a`  
		Last Modified: Wed, 27 Jul 2022 00:56:12 GMT  
		Size: 17.9 MB (17867147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08077974618353cf925465ff3c489bf9ce38e07ecb39ef97cc8a2ce4a590a9fc`  
		Last Modified: Thu, 28 Jul 2022 16:29:16 GMT  
		Size: 191.5 MB (191454078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9828dd21a667779a9bddf4f09aed1c0157e10a31230da9b5d79ff38deeeeb8e`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2185e221352acc94af8a4edee92755a9699c79cf0cdc4c957fdcbb83f9b9cb5b`  
		Last Modified: Thu, 28 Jul 2022 17:10:03 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c419d076b387ad2ac4209ab3cc345f61712dcde0c4c57bf61d318e92a8da77`  
		Last Modified: Thu, 28 Jul 2022 17:10:19 GMT  
		Size: 55.9 MB (55906868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d700298a490e259a8ce74d8733d2818890ef0ad69ec9b83168bb9aff537adb`  
		Last Modified: Thu, 28 Jul 2022 17:10:14 GMT  
		Size: 120.7 MB (120655750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:373f01b78d8090882c8ea519f31a1bcc7551b51438afda7aa0fa8a62ef751b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397197318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16639ca9c86e5ee9dc207f58e2c7141b26a4e18f96edfa5acb3db7f3ec18a36c`
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
# Thu, 28 Jul 2022 15:42:57 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 15:43:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:43:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:43:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:43:09 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 16:05:45 GMT
CMD ["gradle"]
# Thu, 28 Jul 2022 16:05:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 28 Jul 2022 16:05:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 28 Jul 2022 16:05:46 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 28 Jul 2022 16:05:46 GMT
WORKDIR /home/gradle
# Thu, 28 Jul 2022 16:06:00 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 28 Jul 2022 16:06:03 GMT
ENV GRADLE_VERSION=7.5
# Thu, 28 Jul 2022 16:06:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
# Thu, 28 Jul 2022 16:06:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=cb87f222c5585bd46838ad4db78463a5c5f3d336e5e2b98dc7c0c586527351c2
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
	-	`sha256:38ee5983c60ab507c84cdfcddf76d43aa3405f32ac938149cff5c6eb3c0da89d`  
		Last Modified: Thu, 28 Jul 2022 15:47:11 GMT  
		Size: 180.2 MB (180161332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c5127c27f989b35dd8ce9880687e96eaac1b39ea4fe82bdc8d972fc64ac962`  
		Last Modified: Thu, 28 Jul 2022 15:46:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0f1f4d275e07676beb242560438eeccf1865ac822de917f5960ec3805f60a7`  
		Last Modified: Thu, 28 Jul 2022 16:12:07 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b530b68c8ff042fec971b8a663f90d7d20f40a129bfcb81784bbd7014a530e`  
		Last Modified: Thu, 28 Jul 2022 16:12:15 GMT  
		Size: 51.3 MB (51309294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ef06e71738bc1823e488dd56f3d98da415d75b2cc15860214e443a387f5674`  
		Last Modified: Thu, 28 Jul 2022 16:12:12 GMT  
		Size: 120.7 MB (120655737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
