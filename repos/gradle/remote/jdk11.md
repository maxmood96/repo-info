## `gradle:jdk11`

```console
$ docker pull gradle@sha256:1d472df71d43fd1243ba036d47a4b9aaefb8655d818d5b54785fc26526469f41
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
$ docker pull gradle@sha256:9c97ff1209d505206850548237a1adf9312243500930d7180a85941ee3e7d338
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418419229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fcdf5de32bd5c4fad702736f252e770d5e824ff1068a1f74e3d581ac631681`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Wed, 06 Oct 2021 21:50:08 GMT
CMD ["gradle"]
# Wed, 06 Oct 2021 21:50:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Oct 2021 21:50:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 06 Oct 2021 21:50:09 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Oct 2021 21:50:09 GMT
WORKDIR /home/gradle
# Wed, 06 Oct 2021 21:50:28 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Oct 2021 21:50:29 GMT
ENV GRADLE_VERSION=7.2
# Wed, 06 Oct 2021 21:50:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Wed, 06 Oct 2021 21:50:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fedd6a0c137a1b2a88dac30fa92d7ce40807d35f10350305e6ba0bdd4cbeea1`  
		Last Modified: Wed, 06 Oct 2021 21:52:36 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480bcdf97e9c8b61c54b3640169a20d35b85269daab4bab5cc95219d2388c0c2`  
		Last Modified: Wed, 06 Oct 2021 21:52:52 GMT  
		Size: 65.6 MB (65626456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9c22b27f4d453de45bcb0fbd3ff2f7a228e029454152fb0bad0750113faf2`  
		Last Modified: Wed, 06 Oct 2021 21:52:45 GMT  
		Size: 114.4 MB (114373764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:b75c0614cdd66ee160121102998af1f002a38151530761d6e981f221a8ea733e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395081020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e629a0bbe29fd9dcf9c8b2354c4f71864dea5fd7b9a58939d8deec37df9081`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 02 Oct 2021 05:58:58 GMT
ADD file:17b7faea72ce285877ae2e83ecc15fc88de184361899edfcb561531ea121090b in / 
# Sat, 02 Oct 2021 05:58:59 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 23:26:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Oct 2021 23:26:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 23:28:04 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Sat, 02 Oct 2021 23:28:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Oct 2021 23:28:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Oct 2021 23:28:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 02 Oct 2021 23:28:29 GMT
CMD ["jshell"]
# Wed, 06 Oct 2021 20:50:53 GMT
CMD ["gradle"]
# Wed, 06 Oct 2021 20:50:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Oct 2021 20:50:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 06 Oct 2021 20:50:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Oct 2021 20:50:56 GMT
WORKDIR /home/gradle
# Wed, 06 Oct 2021 20:51:45 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Oct 2021 20:51:46 GMT
ENV GRADLE_VERSION=7.2
# Wed, 06 Oct 2021 20:51:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Wed, 06 Oct 2021 20:51:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:29a0bfee4452af9c258710b3049350eec1ed6ee85e33634a638e982934e59d83`  
		Last Modified: Sat, 02 Oct 2021 06:03:00 GMT  
		Size: 24.1 MB (24067218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64e2199de8cbbc437199cb30a504a0e04104b5a48bab3447d69fdb35ef7e9fd`  
		Last Modified: Sat, 02 Oct 2021 23:33:01 GMT  
		Size: 14.9 MB (14897772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febd8bba8434a8851302730054590f0e9819ea501b148ea05b81c1543a72ea87`  
		Last Modified: Sat, 02 Oct 2021 23:34:00 GMT  
		Size: 181.7 MB (181705374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b45b93bec49fb5b7c1c9b128a03bad4f3b99b81dd6a4c6f4a5debc07cc3f6`  
		Last Modified: Sat, 02 Oct 2021 23:32:52 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fa9ccc48790084cd11f4ad8ad33483958af936be6bdd7996d685cc4b171891`  
		Last Modified: Wed, 06 Oct 2021 20:56:37 GMT  
		Size: 4.3 KB (4340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce317af5d143071e565eed455f3a8d73e09d7d747a443dbc6356c959514d870`  
		Last Modified: Wed, 06 Oct 2021 20:57:20 GMT  
		Size: 60.0 MB (60032412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589189c2ea4ea4cadd900c0f38e7dc72b31b76c5b689be40169a2d02cfed2f0f`  
		Last Modified: Wed, 06 Oct 2021 20:57:10 GMT  
		Size: 114.4 MB (114373741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:94d8a666cfeb97b6c0bc85014545f1cf6da7c3ea3194a58fa9d302eefbd2675a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.3 MB (413280374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f95b8fe161023f8c5645c78469ad17aed50451380d9edbe5b28a6a33be2553`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 06 Oct 2021 22:35:05 GMT
CMD ["gradle"]
# Wed, 06 Oct 2021 22:35:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Oct 2021 22:35:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 06 Oct 2021 22:35:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Oct 2021 22:35:07 GMT
WORKDIR /home/gradle
# Wed, 06 Oct 2021 22:35:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Oct 2021 22:35:27 GMT
ENV GRADLE_VERSION=7.2
# Wed, 06 Oct 2021 22:35:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Wed, 06 Oct 2021 22:35:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253e14a81f8b6eff3d76b4a5d20e47b341f934fed8f178b17327aa9a3a25d7a9`  
		Last Modified: Wed, 06 Oct 2021 22:38:30 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84df08a5fc68ef0cb1c491fb6e9946a7652d3614f64921a2cbebf20e94df3668`  
		Last Modified: Wed, 06 Oct 2021 22:38:42 GMT  
		Size: 65.3 MB (65332682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba86ed5f3e8815a2038195085a3d71c3de2cf6add4e6256e088aa716e13cbda6`  
		Last Modified: Wed, 06 Oct 2021 22:38:38 GMT  
		Size: 114.4 MB (114373742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:cc66547d1402c8563316107bd3254d0814f8de34c1d8c33e0d33526e08947a51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414561348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ffa0eba94c3978ba9538d8105755ccfb4dfe5eaba50ebb4911d8f2f1d9798c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Oct 2021 12:59:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 13:01:40 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Tue, 05 Oct 2021 13:02:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Oct 2021 13:02:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 13:02:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Oct 2021 13:02:21 GMT
CMD ["jshell"]
# Thu, 07 Oct 2021 10:05:37 GMT
CMD ["gradle"]
# Thu, 07 Oct 2021 10:05:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 07 Oct 2021 10:05:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 07 Oct 2021 10:05:48 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 07 Oct 2021 10:05:52 GMT
WORKDIR /home/gradle
# Thu, 07 Oct 2021 10:08:23 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 07 Oct 2021 10:08:30 GMT
ENV GRADLE_VERSION=7.2
# Thu, 07 Oct 2021 10:08:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Thu, 07 Oct 2021 10:08:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d0f93d81b8713c3abad0c3080f3bf43c08c0392ff1e24e640afa4e8a5ab59a`  
		Last Modified: Tue, 05 Oct 2021 13:08:20 GMT  
		Size: 17.2 MB (17207545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca99b87bc0dfa669b9673c6c74d224baee18cb4f1911e057caa296636589b1b`  
		Last Modified: Tue, 05 Oct 2021 13:09:27 GMT  
		Size: 175.7 MB (175686441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfb7d0a5a5dd1b81608953725a708cf3fe80f8fde405c622bd46718056c6e3`  
		Last Modified: Tue, 05 Oct 2021 13:09:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5203a2da426ac6b93a0fdd3700b445ccd46183648791ae0d698c0cfd15c6d96`  
		Last Modified: Thu, 07 Oct 2021 10:16:38 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5c95cdc39bd66aa29373aab14b276a9a28561743cfff626a079dfb54af25c8`  
		Last Modified: Thu, 07 Oct 2021 10:16:53 GMT  
		Size: 74.0 MB (73998372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d15a3d735c95d3f8c0aa604709dbdf25a056ff6c91d4fad899e7417f1c777c0`  
		Last Modified: Thu, 07 Oct 2021 10:16:48 GMT  
		Size: 114.4 MB (114373759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:21b232d9f43335582eb694dbd2aa14c8f28c73689e2ff2739d127c1325fe21af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.8 MB (390798933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46e64c126ed4e2204efa0ddc048b712e7cb1d36ca13d2173ce71411e9ae5618`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Sat, 16 Oct 2021 00:59:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 00:59:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 00:59:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 00:59:05 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 01:23:29 GMT
CMD ["gradle"]
# Sat, 16 Oct 2021 01:23:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 16 Oct 2021 01:23:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 16 Oct 2021 01:23:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 16 Oct 2021 01:23:30 GMT
WORKDIR /home/gradle
# Sat, 16 Oct 2021 01:23:46 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 16 Oct 2021 01:23:49 GMT
ENV GRADLE_VERSION=7.2
# Sat, 16 Oct 2021 01:23:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Sat, 16 Oct 2021 01:23:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9aae3329e8c839bcceb87144b9f18dbe85b59f108d21ca33422ddd42c32344`  
		Last Modified: Sat, 16 Oct 2021 01:01:12 GMT  
		Size: 168.7 MB (168726763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e2babc36c34e9a1804509361ffbefaf3e47cd2aed7c1d7ec038fd85b7f82c1`  
		Last Modified: Sat, 16 Oct 2021 01:01:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5ef3bbe3e349e36a9ab4f31ba18a774648c732908e5caa95210be2c4dbcb35`  
		Last Modified: Sat, 16 Oct 2021 01:26:05 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130455fb3afbfef892393ae1e180b97b407ad4062de3b9ffd9563f4593e43dba`  
		Last Modified: Sat, 16 Oct 2021 01:26:15 GMT  
		Size: 64.8 MB (64830952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022eafe6bb1c4be8326fadb38a3b1e0aa431b02d6431c5cd619be10bff7337c0`  
		Last Modified: Sat, 16 Oct 2021 01:26:10 GMT  
		Size: 114.4 MB (114373759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
