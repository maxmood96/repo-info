## `gradle:latest`

```console
$ docker pull gradle@sha256:c4c855480c291d29b11fc0cc0b45ad73cf8b941a9c26b9c0717fa79de72db6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:latest` - linux; amd64

```console
$ docker pull gradle@sha256:54c61588506708f210c71be31a7976c07279c32fba2db10c339fdc324e644381
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377182518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5facac16c350df086e661b5cf0a0939ab6290c44bcffab2f2cb2b15d891b2223`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:40:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:40:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:40:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 01:40:39 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 01:48:09 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 01:48:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 01:48:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 01:48:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 01:48:10 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 01:48:26 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 01:48:26 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 01:48:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 01:48:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 01:48:31 GMT
USER gradle
# Fri, 16 Feb 2024 01:48:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 01:48:33 GMT
USER root
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7828aa16a0c8e2b8a6af9914e88c0c936e93653acddab38c30c518d85f16c29a`  
		Last Modified: Fri, 16 Feb 2024 01:44:19 GMT  
		Size: 144.9 MB (144899392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1d87a91565e3280f7058c72effe794711da5ca9c4cb45cd6ecdb6ce1e8ff09`  
		Last Modified: Fri, 16 Feb 2024 01:44:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7873651f0068cf646c7141160fb2e2f886d9964ee0d89c3ab58425e5f11789ad`  
		Last Modified: Fri, 16 Feb 2024 01:44:07 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468b1c76f6c1c48015e6ec73f6fa3a9c39be38e2eeb192f25b69601c6f397685`  
		Last Modified: Fri, 16 Feb 2024 01:55:13 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12719e443a6effd7905847c2830f86e01aa0d79b13fe3ef69defcc9f2defb9c`  
		Last Modified: Fri, 16 Feb 2024 01:55:22 GMT  
		Size: 51.6 MB (51553392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cab79985ee49492e39d34fec83a57b6cc45dec2059bf2e0caf0b72d22a8a72`  
		Last Modified: Fri, 16 Feb 2024 01:55:20 GMT  
		Size: 132.8 MB (132815736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b06351e7e9b2bd45bf0d897665687b9155f12a7cbd523804df0253fbd55b543`  
		Last Modified: Fri, 16 Feb 2024 01:55:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; arm variant v7

```console
$ docker pull gradle@sha256:c1f04c32eaf3f1c7415277feed03fa8aeadb71d91da7e019e4b06ee5103f636b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374174440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc3984ee9fe7833176f57b56227417ae8e6d7c38990a84cd634dd9ce94bf87b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:20:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:20:58 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 02:21:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 02:21:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 02:21:17 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:21:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 02:21:17 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 03:19:29 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 03:19:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 03:19:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 03:19:33 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 03:19:33 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 03:20:03 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 03:20:04 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 03:20:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 03:20:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 03:20:13 GMT
USER gradle
# Wed, 06 Mar 2024 03:20:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 03:20:18 GMT
USER root
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50a96c90f08484f2e138b73f4209ee84d01efe73944204993cbc23843f5075`  
		Last Modified: Wed, 06 Mar 2024 02:26:14 GMT  
		Size: 17.6 MB (17588569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dd2e23591b56f0c9a378c10cf4fa2b6c4ad06c3e39ef43b677706b3d095eaf`  
		Last Modified: Wed, 06 Mar 2024 02:26:28 GMT  
		Size: 142.3 MB (142338737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a15277a8469cbcf05a5613fb67f89beb3a778abd38a34d6d528ee7024ec536`  
		Last Modified: Wed, 06 Mar 2024 02:26:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978c56cc301e9ff7bc6e98fedb0041cf5efea2be9df27976427c38fc49b1ed5`  
		Last Modified: Wed, 06 Mar 2024 02:26:09 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b62eb1302362ad9f79517d5d766867054ab5a326c8da5a27a002fb17dc7f7b0`  
		Last Modified: Wed, 06 Mar 2024 03:29:06 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fca5fdebe3c1c3882e17588c8f845ce76c32260cf77f02dc7c5ed43a676a04`  
		Last Modified: Wed, 06 Mar 2024 03:29:19 GMT  
		Size: 53.9 MB (53892033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf10de5b6ea0d7f7fa576095efa43f50362939f57b53ecaf406a8eb95b383221`  
		Last Modified: Wed, 06 Mar 2024 03:29:19 GMT  
		Size: 132.8 MB (132815738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3385c77f4607959f2ad3a69fe6842d33d9da69716e873e96bff9b5f436fb1c86`  
		Last Modified: Wed, 06 Mar 2024 03:29:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c0f72f8ddc857b9af82b73777b1939d8ae743752a1ea3545e2c3dfbe472d59f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374931263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b00513fa941de814bc4aa357d2fea12b35035ea9fc672f4f8ffddf87d11f24`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:51:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 04:51:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 04:52:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:52:49 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 04:52:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 04:52:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 04:52:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 04:52:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:52:59 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 08:34:09 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 08:34:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 08:34:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 08:34:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 08:34:10 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 08:34:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 08:34:23 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 08:34:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 08:34:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 08:34:28 GMT
USER gradle
# Fri, 16 Feb 2024 08:34:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 08:34:29 GMT
USER root
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76266141a695afde995a7cd7ce10e77a76fb2784d5b193501a0770abb0dc7e5`  
		Last Modified: Fri, 16 Feb 2024 04:55:54 GMT  
		Size: 143.7 MB (143724169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce09e5ecb75335308eac898e130df5be02483e0fa736865f00e72d6bc01f18c2`  
		Last Modified: Fri, 16 Feb 2024 04:55:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689deaab56a786d5415c3530e6a9bd3c9bb7ef89b349942435384e2181a7577`  
		Last Modified: Fri, 16 Feb 2024 04:55:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28684d9aea1ddef4d4e1803dc04ee30837b31d5350446270c4493819dcf9fe3`  
		Last Modified: Fri, 16 Feb 2024 08:38:20 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0a3b024a0f6ee061c4838e8683b5cba6eb7ab79702eb4ae0eabaf5b29e7d49`  
		Last Modified: Fri, 16 Feb 2024 08:38:26 GMT  
		Size: 51.1 MB (51125026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da06816a642620064eed0b77d8fc3444008cee558cc2d72927990b32928c1f`  
		Last Modified: Fri, 16 Feb 2024 08:38:25 GMT  
		Size: 132.8 MB (132815714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1031b21870cc0321b861b8c205dd7602eacf27024a01a3f24a7187adb276fbb9`  
		Last Modified: Fri, 16 Feb 2024 08:38:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; ppc64le

```console
$ docker pull gradle@sha256:2bd9473bcce8250b9df9bed1c82997c0773e1ce5b761186bf2b35d4d8923feac
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387486953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2730507da7fb07aa7e859feea4d41e01d60ca40cb8a8ce7bd362bc9778621396`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 03:01:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 03:01:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 03:03:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:03:54 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 03:04:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 03:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 03:04:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 03:04:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 03:04:13 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 05:33:04 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 05:33:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 05:33:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 05:33:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 05:33:09 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 05:33:49 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 05:33:53 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 05:33:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 05:34:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 05:34:03 GMT
USER gradle
# Fri, 16 Feb 2024 05:34:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 05:34:07 GMT
USER root
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f58720ac09e0a0749b7f33b7e071a91c06df2aa3390db23d6f7460a7a72e687`  
		Last Modified: Fri, 16 Feb 2024 03:08:31 GMT  
		Size: 144.6 MB (144634054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260ed70c2d85dc8fae118fc6419d155f6df24539547562701272893711d226ac`  
		Last Modified: Fri, 16 Feb 2024 03:08:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a585a9fb909ab5c26594e86581e49a8aa6419b0e9912852c8ff9c6bc892403b`  
		Last Modified: Fri, 16 Feb 2024 03:08:17 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929398da5f70b10f98536e257a9e32a923ab07f5765402bf882349018f6f8234`  
		Last Modified: Fri, 16 Feb 2024 05:38:22 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c9cb208c717c63cca9afaa9b1e8e0088d20362643119247587085239a2133`  
		Last Modified: Fri, 16 Feb 2024 05:38:32 GMT  
		Size: 55.7 MB (55676682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cb27a5f283027dabd14ea85786f9d2bae85b562b68d9cd90cf4ae2e36d43b5`  
		Last Modified: Fri, 16 Feb 2024 05:38:29 GMT  
		Size: 132.8 MB (132815745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c210b6b8f0680c75343720ee69b71d2579f2f3ecc6d974adbfe4fc8c55ff9b96`  
		Last Modified: Fri, 16 Feb 2024 05:38:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; s390x

```console
$ docker pull gradle@sha256:598de81fe6195cdd63b1d53390efa62ab3b34e9f40bd8d24d8126509ab83c554
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364214426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcee60c2a1174d0296b97acf09609a94d66235b7f62b45a3e8c9b863dd25dc03`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 07:27:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:27:10 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 07:27:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 07:27:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 07:27:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 07:27:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 07:27:24 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 14:43:53 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 14:43:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 14:43:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 14:43:54 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 14:43:54 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 14:44:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 14:44:10 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 14:44:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 14:44:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 14:44:19 GMT
USER gradle
# Fri, 16 Feb 2024 14:44:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 14:44:20 GMT
USER root
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06439c312d07b9a9a2b1abe400a875c694ea9d34abcd938043094f9fa832631d`  
		Last Modified: Fri, 16 Feb 2024 07:38:53 GMT  
		Size: 17.3 MB (17261530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc621bb8b1d5be869a6e2f4ab151bf49e26d56d679e844fa3ab62956e584a23`  
		Last Modified: Fri, 16 Feb 2024 07:39:00 GMT  
		Size: 134.2 MB (134212457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd915a4acb922febde2aac9fb1669ffa60ad19d035377268b3cba05c0f739065`  
		Last Modified: Fri, 16 Feb 2024 07:38:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac0d091e7bf2a5b4099c2da6b0c3c6f96e7c09acb5e83daaa5576d9f83fecb3`  
		Last Modified: Fri, 16 Feb 2024 07:38:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046fc0116e43bd4188a8a5d13f384d6bcb5fd6c5f8bb870aabde900550199dad`  
		Last Modified: Fri, 16 Feb 2024 14:58:04 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd4383b694e210b43d9a4702f2cf6a1168d5a7c134e36c99c04ec1987fc2c2`  
		Last Modified: Fri, 16 Feb 2024 14:58:12 GMT  
		Size: 51.3 MB (51280531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1863eac804a213e25e09c38203b290568c9d6b394eb489d94f8bd01042c239`  
		Last Modified: Fri, 16 Feb 2024 14:58:09 GMT  
		Size: 132.8 MB (132815739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b856c103573837492b0432b2abfc2a49e7e2a0b8427175592a85049269c6bf4`  
		Last Modified: Fri, 16 Feb 2024 14:58:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
