## `gradle:jdk11-focal`

```console
$ docker pull gradle@sha256:bb1ca8106ee9b18f8f8cc0b82a16157eb326e2ba5c505a45c4160002e2871d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk11-focal` - linux; amd64

```console
$ docker pull gradle@sha256:c427e0b5767bc756e9d6d6753c3dcf3503e38b82d2c9fab6b1ad1de515960062
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384049377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1525b32bf8eaf315f85f2920eb645663f7c6b92c1eb034ed545280e1648a99`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 02:01:38 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 02:01:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 02:01:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 02:01:39 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 02:01:39 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 02:02:04 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 02:02:05 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 02:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 02:02:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640ff3b94a44795751b00ee0a1332db83daf302c47f6894a3e154b3fd19b40ff`  
		Last Modified: Wed, 26 Jul 2023 02:05:37 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5ed36b1e26e3408e286cb4297c5cf104dc5017e83d7c9778be88683f87ebfe`  
		Last Modified: Wed, 26 Jul 2023 02:05:47 GMT  
		Size: 65.5 MB (65486416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34db22c840a13cfb1e030b4730b44e034ad0118d0e7e3e4574e3eb0562949b7d`  
		Last Modified: Wed, 26 Jul 2023 02:05:43 GMT  
		Size: 128.7 MB (128727028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:2615b5bc127820b2e2db0e4bd9d263d2073cf71125d0b5253165f18958c8a2c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366055276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e85607bb6fc68f84df07eeefdbf4fb23ece54f3183068b2e5dc9974b893ea0c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:08:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:08:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:08:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:09:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 25 Jul 2023 23:59:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 23:59:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 23:59:06 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:31:58 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 00:31:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 00:31:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 00:31:58 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 00:31:58 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 00:32:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 00:32:24 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 00:32:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 00:32:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0186b47b0f035fc3bcf39b19dfd039f6fa8694a7e17ba90a3fc477b5753c106`  
		Last Modified: Tue, 04 Jul 2023 20:13:22 GMT  
		Size: 15.2 MB (15239799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29568b15f3a2955a7ef9c3b85c523c380946ca6afc73e12914687413ce0a04d3`  
		Last Modified: Wed, 26 Jul 2023 00:00:44 GMT  
		Size: 137.4 MB (137406228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a02f03a54960fda566439ca393661b94e410d54f800a4ccf38198891daca1a1`  
		Last Modified: Wed, 26 Jul 2023 00:00:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d113e8482917dd55771242f32dfabb94748e110c9be44af999fffc70c4cb5501`  
		Last Modified: Wed, 26 Jul 2023 00:34:54 GMT  
		Size: 4.4 KB (4351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd9a3006b26d7982e602602f640c0a35326988fed2068cf44b2258ea1cffa95`  
		Last Modified: Wed, 26 Jul 2023 00:35:05 GMT  
		Size: 60.1 MB (60089524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6448a76bbb7ff78be616cd6dbfceea3353d6c2f8e876e710ff478a23c146839`  
		Last Modified: Wed, 26 Jul 2023 00:35:01 GMT  
		Size: 128.7 MB (128727065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:333880edeca2bc54096bdca3e902c4dbee3f9e4433be334901c6c6444c957281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (379002783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51785c62d06d48ccf8b3fb58eabe4f898bba064777e38167c88265c7ca2073b`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:50:05 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 01:50:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 01:50:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 01:50:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 01:50:06 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 01:50:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 01:50:30 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 01:50:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 01:50:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c5f9f5e0a691cdb2d201a5bb5900b51b387d966883d1890525253d7970dc5d`  
		Last Modified: Wed, 26 Jul 2023 01:52:51 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11415d6abacfc570402573d9d612fea930ad64d887915b32079c5e640de5e489`  
		Last Modified: Wed, 26 Jul 2023 01:52:59 GMT  
		Size: 65.2 MB (65233093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c360589a5be068169de98a672d6c78e7c704b5e3cddec15f724faf562f21d5`  
		Last Modified: Wed, 26 Jul 2023 01:52:57 GMT  
		Size: 128.7 MB (128726998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:efa613ce3f238ab2c22473b2457f5cfa081ac29c9125e0be9400b68129b3708c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385527441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4957c71d090e8cee8efc054dcc89dbb82e77aa09693c7143b9d9cad2c92437`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 00:16:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 00:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 00:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jul 2023 00:17:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:16:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:17:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:17:21 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:14:54 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 01:14:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 01:14:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 01:14:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 01:14:58 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 01:16:15 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 01:16:19 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 01:16:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 01:16:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:4e95615eadb7a0d90a47ca15a5c0693371494902f54d8d78a50d53e89e7a20de`  
		Last Modified: Tue, 04 Jul 2023 04:40:49 GMT  
		Size: 33.3 MB (33308759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900a3bee385ed74b6117be4963259e4ef65f261ee58fc971b7206f32acb0572b`  
		Last Modified: Wed, 05 Jul 2023 00:27:54 GMT  
		Size: 17.6 MB (17648843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24a08ed55e0de1cc68c00fba548e250ce6fd0301e9f4913fed502a4d78107ea`  
		Last Modified: Wed, 26 Jul 2023 00:22:20 GMT  
		Size: 132.0 MB (132000964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a531d35c5668e40ca19b1a43d77e8d5a036bf699adaa895fd6d5b552308f37b`  
		Last Modified: Wed, 26 Jul 2023 00:22:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa12025f8fce8d536080e4ddabd29901a224c4122c2e0f5cf51be74cd89bd6a`  
		Last Modified: Wed, 26 Jul 2023 01:21:25 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db5545ea757472f4bbba0762bbee0dd9e8149bbc57617c1616973412acee75c`  
		Last Modified: Wed, 26 Jul 2023 01:21:47 GMT  
		Size: 73.8 MB (73837261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686b9f6eee900c37debca787c373d416770b9d362d7288e57850092cca35e1a3`  
		Last Modified: Wed, 26 Jul 2023 01:21:36 GMT  
		Size: 128.7 MB (128727077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11-focal` - linux; s390x

```console
$ docker pull gradle@sha256:667278e3f0543f29b3087ed67fb9fdc8d3599efaadcd70a8cc215b533e217dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361778366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7359361ad66704a430da36309c9baccfb09484c6b95b16bca574cc7e4f73eadb`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 16:23:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:23:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 16:23:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:41:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:42:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:42:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:42:11 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:03:43 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 01:03:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 01:03:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 01:03:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 01:03:44 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 01:04:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 01:04:14 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 01:04:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 01:04:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f5ebe8481b30a6d3b710b0efdec29843cca805811e3be1a4e375761725c40e5a`  
		Last Modified: Tue, 04 Jul 2023 13:07:41 GMT  
		Size: 27.0 MB (27013645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3533c99e551f88519f4e20865cc3f7f85d6c5a6083a720282116b19596c7043`  
		Last Modified: Tue, 04 Jul 2023 16:28:03 GMT  
		Size: 16.1 MB (16103623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a9a1e09a6335ef44d69230102f319888ecfb012e1e66c235081455a884475`  
		Last Modified: Wed, 26 Jul 2023 00:44:55 GMT  
		Size: 125.1 MB (125135745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974813bfca7f53474985d80469c00684c07772ea5b09b830b7f6e0b60aa4c231`  
		Last Modified: Wed, 26 Jul 2023 00:44:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31024f09b7b5bdec0f042742ff505d78de5e9ee2d7a6d8b85af79127a3807de2`  
		Last Modified: Wed, 26 Jul 2023 01:07:33 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced519c1d5969cef411396641762de51fc2c600afd82437312ecec2c2c5dcc39`  
		Last Modified: Wed, 26 Jul 2023 01:07:43 GMT  
		Size: 64.8 MB (64793764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365039c1c5ad48742956e37e54bb0e72feb686d6866737052d2b47f6e9c7c0df`  
		Last Modified: Wed, 26 Jul 2023 01:07:39 GMT  
		Size: 128.7 MB (128727050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
