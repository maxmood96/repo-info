## `gradle:jdk11`

```console
$ docker pull gradle@sha256:329d1aabe6dce7fd6e757d5b8e722654e24770c0a9922a9d0fe1f9e716313753
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
$ docker pull gradle@sha256:49e008c1509d9d2aee4cce548f026ea5beb2f31289bc444dfb6ccea3481dffc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (420040974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7dd5ef8a9e5ec60d6f93059c81c6e5dc66ab0fc70e7d670c890476928d7c49`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:23:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 23:58:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:27:02 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 19:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:27:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:27:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 19:27:11 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 19:54:15 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 19:54:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 19:54:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 19:54:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 19:54:16 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 19:54:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 07 Mar 2022 19:54:35 GMT
ENV GRADLE_VERSION=7.4
# Mon, 07 Mar 2022 19:54:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
# Mon, 07 Mar 2022 19:54:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d66994d054da0091fad11fb497b2a23c0cfd350d897d78d57f78b3200b90fd6`  
		Last Modified: Fri, 04 Mar 2022 00:06:51 GMT  
		Size: 16.0 MB (16030868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbea39b540a5a007ac6cc93018df2dc6e64c95f362c01b8e6178e62862536f8c`  
		Last Modified: Mon, 07 Mar 2022 19:31:16 GMT  
		Size: 193.9 MB (193949676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14ed2aa322a3be19eb1c8a2f1ad22d8f70051f4845706e41dc880031654700`  
		Last Modified: Mon, 07 Mar 2022 19:31:02 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9206e24aa8d1a696ce02fa825fed9e453987944f0b7866dcd039bedcf4451c3`  
		Last Modified: Mon, 07 Mar 2022 19:57:24 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa8dcac4c4b231bf3ed07cfd843e61a9e01005a4853c038391b5ee188b57cee`  
		Last Modified: Mon, 07 Mar 2022 19:57:35 GMT  
		Size: 65.6 MB (65625417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a59973126977632ced9658b8e25121290846cc3a96146257d69599309e398a3`  
		Last Modified: Mon, 07 Mar 2022 19:57:30 GMT  
		Size: 115.9 MB (115864742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:e47bfadc00ae2a203bc5564c4857013abbd0a072a1fd03552cbe1ebbbb0c291e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396709248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fc89c46120fd8fc96df65fce03dedb30db1e0f96340cd44480c3328f58c9e7`
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
# Mon, 07 Mar 2022 19:59:36 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 20:00:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 20:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 20:00:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 20:00:05 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 21:56:03 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 21:56:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 21:56:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 21:56:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 21:56:06 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 21:56:57 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 07 Mar 2022 21:56:58 GMT
ENV GRADLE_VERSION=7.4
# Mon, 07 Mar 2022 21:56:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
# Mon, 07 Mar 2022 21:57:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
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
	-	`sha256:d341667848a8d99b3ca2b3ef6aa5bfddf564646d06d5958fa7122d7ccf3308a0`  
		Last Modified: Mon, 07 Mar 2022 20:08:19 GMT  
		Size: 181.8 MB (181831101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f28b281b7e145bf45fa5674d10e07d22180a3ff3e2427b1a7b94fd349653`  
		Last Modified: Mon, 07 Mar 2022 20:07:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c222cac8f2d313698d1e536affd82b5264656353efe07461f16764b6d7141`  
		Last Modified: Mon, 07 Mar 2022 22:03:48 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d003c05204624f494a22aecda6d8411766b27c3379e0264c839579f7547e9fe5`  
		Last Modified: Mon, 07 Mar 2022 22:04:31 GMT  
		Size: 60.0 MB (60032810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d8b2890cc9d9a94ebc8b917d6ac70b5d800a368d6e205e37e186f011bb8944`  
		Last Modified: Mon, 07 Mar 2022 22:04:20 GMT  
		Size: 115.9 MB (115864781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0f613528a30ebce5950127402e7860a5804b00ec1bc22e6e60e2511834989940
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (414956360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead6d499360d058b3489eb2cb17a89eb8ea8c56eb48c75f5ae86fe1e4bb01c81`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:21:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 21:48:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:43:22 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 19:43:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:43:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:43:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 19:43:37 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 20:07:20 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 20:07:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 20:07:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 20:07:23 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 20:07:24 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 20:07:48 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 07 Mar 2022 20:07:49 GMT
ENV GRADLE_VERSION=7.4
# Mon, 07 Mar 2022 20:07:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
# Mon, 07 Mar 2022 20:07:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef837f2895f973a326f5521a157b464e2c984b807cae56ef148568938f8bbc0`  
		Last Modified: Thu, 03 Mar 2022 21:55:26 GMT  
		Size: 15.9 MB (15897880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e91d252a1525ab45839b4f6c4d3f03423539b0d39c8fc710e30a728c1927d5`  
		Last Modified: Mon, 07 Mar 2022 19:48:52 GMT  
		Size: 190.7 MB (190684870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effcccf97b209bf1f81d7cfa22a72a7279cd572fac1711ea22787013bb6f598`  
		Last Modified: Mon, 07 Mar 2022 19:48:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0559af48736ee8b31344ae8a694a1bdb297234322c76e58957e88917e30a0938`  
		Last Modified: Mon, 07 Mar 2022 20:11:07 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b243c086c40f5ab08dcbc94eacac7fc375c539e902ce6c97e4bbcb6c342b6`  
		Last Modified: Mon, 07 Mar 2022 20:11:18 GMT  
		Size: 65.3 MB (65334907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5332149884e3dae9ddd10241a530e4c4196ae0f31fa5a7a45df35e159a41288`  
		Last Modified: Mon, 07 Mar 2022 20:11:15 GMT  
		Size: 115.9 MB (115864632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:828ac92a492a6e07447978bfc98521a7b4f936cd6abbf4e562d58606e90a58b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416210655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d5a3bdcb3e8ad499904e1af080c6d2422c1e765da66496689339ffe445ca04`
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
# Mon, 07 Mar 2022 19:26:25 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 19:26:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:27:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:27:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 19:27:20 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 19:59:23 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 19:59:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 19:59:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 19:59:42 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 19:59:47 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 20:02:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 07 Mar 2022 20:02:32 GMT
ENV GRADLE_VERSION=7.4
# Mon, 07 Mar 2022 20:02:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
# Mon, 07 Mar 2022 20:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
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
	-	`sha256:ae5ded363df7c4fd7a1a11184a14876e8ba4e8d8abb61242fd9ed2ac52586d89`  
		Last Modified: Mon, 07 Mar 2022 19:37:38 GMT  
		Size: 175.8 MB (175842565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1c652d22763265b0aa08b6ba55891c17bd3b1f0548ac388e4fd8235c40aa8`  
		Last Modified: Mon, 07 Mar 2022 19:37:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6635761963a9a13fc1549982d0de0adc564188c53c9fc5cdd5d3a82ae6d3a8cf`  
		Last Modified: Mon, 07 Mar 2022 20:11:53 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc0db76e62603f2ed571843bbfa791f095961766cf6346d0061020b52b419a0`  
		Last Modified: Mon, 07 Mar 2022 20:12:08 GMT  
		Size: 74.0 MB (74001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00d65231fb466ab1a4af5c1f84c893b9961d85d5e50d1f109c5a93eff4d7aac`  
		Last Modified: Mon, 07 Mar 2022 20:12:03 GMT  
		Size: 115.9 MB (115864718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:23b53cb308c53a45296d43bc582e7ffb087693591d7f0c201b6b0c7b3c368e19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391890307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48accaec33dc096752120f36ce6aa6aece0b220ce25513b8ff896af281b32b3c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:52 GMT
ADD file:3162233da685a36a9f274a7fa1d99452cab76f37e3640d38851c782ca506f75b in / 
# Thu, 03 Mar 2022 19:41:53 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 20:04:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:43:36 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Mon, 07 Mar 2022 19:43:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:43:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:43:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 19:43:48 GMT
CMD ["jshell"]
# Mon, 07 Mar 2022 20:03:14 GMT
CMD ["gradle"]
# Mon, 07 Mar 2022 20:03:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 07 Mar 2022 20:03:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Mon, 07 Mar 2022 20:03:14 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 07 Mar 2022 20:03:15 GMT
WORKDIR /home/gradle
# Mon, 07 Mar 2022 20:03:33 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 07 Mar 2022 20:03:36 GMT
ENV GRADLE_VERSION=7.4
# Mon, 07 Mar 2022 20:03:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
# Mon, 07 Mar 2022 20:03:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8cc27038d5dbd815759851ba53e70cf62e481b87494cc97cfd97982ada5ba634
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ade7e68f4e34f438527a34c9761a285c3c3864e3daab0544b2c4f4163c7c3f56`  
		Last Modified: Thu, 03 Mar 2022 19:43:22 GMT  
		Size: 27.1 MB (27084671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6625b9cdb7a6f1a1f7715f9b1e2a04e2e285aa79c11778a4edeca0017ab83b5`  
		Last Modified: Thu, 03 Mar 2022 20:12:44 GMT  
		Size: 15.7 MB (15739982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276f4118632bb872282e6211d18c7eeb131eb95882af3d4584a2bae1b8c05c99`  
		Last Modified: Mon, 07 Mar 2022 19:46:24 GMT  
		Size: 168.4 MB (168352401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f95bfc326ca44db1d632392fe9af071e165b3045b5b8a25bfc9b3153a06377`  
		Last Modified: Mon, 07 Mar 2022 19:46:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573065c8c08d9ea550ba4acf7d2c0db8f7baac2d6863c7aaf015a96a8955286d`  
		Last Modified: Mon, 07 Mar 2022 20:05:56 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91a7559153cad584ad5540710b6e12f2ca6fc3291eda42cd7f5b8ca8fdc62d9`  
		Last Modified: Mon, 07 Mar 2022 20:06:06 GMT  
		Size: 64.8 MB (64843951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27b9f057cf99aedc5bd5172c7729ccea327b9fe0d69ebd94e616833b080207c`  
		Last Modified: Mon, 07 Mar 2022 20:06:01 GMT  
		Size: 115.9 MB (115864779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
