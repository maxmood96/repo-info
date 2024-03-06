## `gradle:focal`

```console
$ docker pull gradle@sha256:647799cc116246db0a802df69873c08ddcb31b793fe3877beced65143be8838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:focal` - linux; amd64

```console
$ docker pull gradle@sha256:17e0c6bec6cb2c7f4240315d7a957c6b9058a5c137c2f8b37760ac327111ce87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392443983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524cbd9607b3fa4928314c5ea51dfe393b5dbe5e5f4f45b0881144bd105d41e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:01:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:04:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:04:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 06:04:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 06:04:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 06:04:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:04:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 06:04:40 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 09:46:33 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 09:46:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 09:46:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 09:46:33 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 09:46:33 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 09:46:52 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 09:46:53 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 09:46:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 09:46:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 09:46:58 GMT
USER gradle
# Wed, 06 Mar 2024 09:46:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 09:46:59 GMT
USER root
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c95b51aedb631b034e78780f8dd39133f351ccaa5ce582020ac5c37a72331a`  
		Last Modified: Wed, 06 Mar 2024 06:09:38 GMT  
		Size: 20.7 MB (20671288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c490cd11d84335564222988de0d6115263754557d21e61e33a7b85914a3192`  
		Last Modified: Wed, 06 Mar 2024 06:09:46 GMT  
		Size: 144.9 MB (144901645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e71ce2fbd953d5acc611c082ee9a78921e1818741cd237a2a8fe10bc68bd89`  
		Last Modified: Wed, 06 Mar 2024 06:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9785679989122f060ab213f23877d1b72e38c5b3496744f29d27062ef3aa1904`  
		Last Modified: Wed, 06 Mar 2024 06:09:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1a358d0424334c3b79b9c36d672a988df9144f54beb93d98f89a1a4bb894f1`  
		Last Modified: Wed, 06 Mar 2024 09:54:04 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61881432d7ea3fdcea5f345beb8011727a94431ccf34ca8754ab7b999e2b2927`  
		Last Modified: Wed, 06 Mar 2024 09:54:15 GMT  
		Size: 65.5 MB (65465540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8578bcffbad75b1e6a76368cd067140e12246c90c65575a13b4336d12d90c479`  
		Last Modified: Wed, 06 Mar 2024 09:54:11 GMT  
		Size: 132.8 MB (132815751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d81ccab9e05a11f1d9988cd65a97e4d3640db0c962ea91c84d742de03d37be0`  
		Last Modified: Wed, 06 Mar 2024 09:54:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:4e9eb82dc8365f48f18af548c61aca1bef846db6b45e3de6db63909685ffe592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379812738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeed3d916b556dc79f551b8fb8e4472bed7435e912f4ee4705a665071721a234`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:14:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:20:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:20:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 02:20:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 02:20:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 02:20:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:20:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 02:20:23 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 03:20:28 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 03:20:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 03:20:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 03:20:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 03:20:32 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 03:21:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 03:21:07 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 03:21:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 03:21:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 03:21:17 GMT
USER gradle
# Wed, 06 Mar 2024 03:21:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 03:21:21 GMT
USER root
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d555e2c31568b7b481f2aa727b2fdcf652e9c4e4b93ca28ed5add2c3cd06645`  
		Last Modified: Wed, 06 Mar 2024 02:25:41 GMT  
		Size: 20.0 MB (19956639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ec048d9fa9ad171dd54ef0a5f117d22f1e2bed4548e473c7d566ef12a77b59`  
		Last Modified: Wed, 06 Mar 2024 02:25:55 GMT  
		Size: 142.3 MB (142339252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c469bff39279f9882015db25667bcf12782c8ecae85a24055ec351e847074e55`  
		Last Modified: Wed, 06 Mar 2024 02:25:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8541780b040ca0b71d7d5b5a27041b53d46ecee1d71515f59d27eca5b0bfa3`  
		Last Modified: Wed, 06 Mar 2024 02:25:35 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82927d9b7a0ec11a53e64c31b357b5ad779fd894e203e6b314d1e3f7a7d23654`  
		Last Modified: Wed, 06 Mar 2024 03:30:20 GMT  
		Size: 4.3 KB (4350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b628d45ad48112b4d94063fbc0ade2da85a51c8131b83d02ce18c9f6331dc9`  
		Last Modified: Wed, 06 Mar 2024 03:30:36 GMT  
		Size: 60.1 MB (60094414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d9ef6b2fb2cce88f7789b2937fee6f7fb7695a581feef8439df8c46eca05e1`  
		Last Modified: Wed, 06 Mar 2024 03:30:35 GMT  
		Size: 132.8 MB (132815662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e5b28c635dc6addd6df87174d0a62985b3b675fc0feb5dd6d7f93991d42950`  
		Last Modified: Wed, 06 Mar 2024 03:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1168ed8c29ad26ea90761c984649a388389d0951b866adaf511edff2ca67d529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 MB (390357329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb7a8d23e8df4b774bfc0aa3f7920e5dc45a331e675abde4ea8368f448b8c43`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:15 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:03:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:03:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:03:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:03:25 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 13:45:44 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 13:45:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 13:45:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 13:45:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 13:45:45 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 13:46:00 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 13:46:01 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 13:46:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 13:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 13:46:06 GMT
USER gradle
# Wed, 06 Mar 2024 13:46:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 13:46:07 GMT
USER root
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ffa0418e76e0bcdee2755d99f7dac08c24067fe1e5e552bae53e379419ec8`  
		Last Modified: Wed, 06 Mar 2024 04:07:44 GMT  
		Size: 21.4 MB (21375265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8ed3c389fd3b5d878a783cbe45ca9e8f84794ab430c386edb2d022ee1fcee7`  
		Last Modified: Wed, 06 Mar 2024 04:07:51 GMT  
		Size: 143.7 MB (143724289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d3aa451a1be4a98a7185ce13c58e08dca80b7a225ecdcee8a90957a5cc14f`  
		Last Modified: Wed, 06 Mar 2024 04:07:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2a4b2e736d2f6cc3696576bff2edc7ea7fc48979b21a342472af3cc26002f9`  
		Last Modified: Wed, 06 Mar 2024 04:07:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db9edc9748d4743b1eb63b79b76685a1ae90c9919937f1501026cee45b8c6d6`  
		Last Modified: Wed, 06 Mar 2024 13:51:58 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5a51e4fb0a697005ee8bd6ecee02ee8040e4bbe18e2b4c9496549bddc45211`  
		Last Modified: Wed, 06 Mar 2024 13:52:06 GMT  
		Size: 65.2 MB (65232305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1367ebbe89119ca5bc8824d696bb117879c047dfc18f4be3df4d43d2822a63d9`  
		Last Modified: Wed, 06 Mar 2024 13:52:03 GMT  
		Size: 132.8 MB (132815739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531fcab25e7fee132481a4bad790a93d3e4c29b8d1da3ea2082f1e13e85fcfcc`  
		Last Modified: Wed, 06 Mar 2024 13:51:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:234928b7902a406634e8d0dd1e09fa70dc53e6f905c800160972759bc4957740
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407322568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a1dfc16d9ac9de77ca1de39ed485bb1edd2ddaa40174d764fe107147ecd79b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:35:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:35:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:40:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:40:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:40:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:40:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:40:51 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:40:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 01:40:52 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 04:00:09 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 04:00:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 04:00:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 04:00:12 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 04:00:12 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 04:00:56 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 04:01:00 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 04:01:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 04:01:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 04:01:10 GMT
USER gradle
# Wed, 06 Mar 2024 04:01:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 04:01:13 GMT
USER root
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cdc517cb589adf37b100dc7920803b77c7fb948dcef214ef0f4c72da49bcd5`  
		Last Modified: Wed, 06 Mar 2024 01:47:09 GMT  
		Size: 22.7 MB (22715648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe03e34eac06c2676ae9e495f6653a55bbbec83e2e39e0a4549f5a9d2e7003a`  
		Last Modified: Wed, 06 Mar 2024 01:47:18 GMT  
		Size: 144.6 MB (144635201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a89230b8a40efa2c8f1d10596ab9fe578089a2e36a1a4dc970a426fdd649b5a`  
		Last Modified: Wed, 06 Mar 2024 01:47:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b79da40ddce0b110a94fed779ec98a2aa324bc0d12116a68097592cd1c4f6c`  
		Last Modified: Wed, 06 Mar 2024 01:47:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7861783a4d44374e5fa7ebb5cf39f04c424aefceba14a6edfebbdfdcd5378a9a`  
		Last Modified: Wed, 06 Mar 2024 04:09:09 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b196cae963c8d516adf88338a06b11eadebda837374069ebf5071092c9e3cf3`  
		Last Modified: Wed, 06 Mar 2024 04:09:22 GMT  
		Size: 73.8 MB (73834919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a516e77ff7797775f37718b9a309640482bc9301623e30098cbd6341d2efd1`  
		Last Modified: Wed, 06 Mar 2024 04:09:16 GMT  
		Size: 132.8 MB (132815746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5fb552f297703a0df2dae3d895d2bdd2c6be5f11cd34601ae02c4ae952e43a`  
		Last Modified: Wed, 06 Mar 2024 04:09:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:focal` - linux; s390x

```console
$ docker pull gradle@sha256:26682e428bab5d9935fb09e883196f2567a55ca4f531876545fe7b1155aa7ebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (378993595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f4bb4084e06d4f9435840f61b75e06a925c1d2aae00d6dba6c868ed3010b75`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:28:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:28:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:28:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:39:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:39:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:39:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:39:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:39:52 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:39:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 03:39:53 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 06:32:52 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 06:32:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 06:32:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 06:32:52 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 06:32:52 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 06:33:09 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 06:33:13 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 06:33:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 06:33:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 06:33:20 GMT
USER gradle
# Wed, 06 Mar 2024 06:33:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 06:33:21 GMT
USER root
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2555c4551e612a2a785b3f31fd17957e6c7df99bee2c607006ebe378cda27959`  
		Last Modified: Wed, 06 Mar 2024 03:57:20 GMT  
		Size: 20.1 MB (20142441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae976da396ce564d7b926e6f9f6bce1ebc4756e16c5ec52424a14fd48baaaed2`  
		Last Modified: Wed, 06 Mar 2024 03:57:28 GMT  
		Size: 134.2 MB (134212550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213fec5a03b3fa612b2ee4daa791af857221fec646f818342972e3396ff07211`  
		Last Modified: Wed, 06 Mar 2024 03:57:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87743d27f98e8009f22ff3822cf593dd5300489bb989dfa24f2ec662384010de`  
		Last Modified: Wed, 06 Mar 2024 03:57:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70072e696c5e24b9e4d851cba02fd1c4edfede89f493714b76979faf866a41`  
		Last Modified: Wed, 06 Mar 2024 06:46:50 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f995fa8b7f4d61e87a7ec94bc4f4934feb1f6422627db9567ed1c334c1899715`  
		Last Modified: Wed, 06 Mar 2024 06:47:05 GMT  
		Size: 64.8 MB (64801357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1247c1b29fcc5184c752b8a374f5725aeae1b90ff0f475a43380149506da83`  
		Last Modified: Wed, 06 Mar 2024 06:46:56 GMT  
		Size: 132.8 MB (132815733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de2b1125d206dfebbcd5c2880b64b07f8a81bb847b7121445096aa66d48f92`  
		Last Modified: Wed, 06 Mar 2024 06:46:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
