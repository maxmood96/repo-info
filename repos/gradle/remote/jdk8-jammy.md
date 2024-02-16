## `gradle:jdk8-jammy`

```console
$ docker pull gradle@sha256:c7b86464704aeb2e63e9e12097047e49410ed0100f6c1e48408662c475404154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:5e49f4f2fa4b33f3a8fea16fae3807c6a9d3212b1a661341ec0294b23e35f7c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331328456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d239af8e92b0a7da2ef64795e0e5b64afb311e82471449b13bfa0a5c45485f9`
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
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:38:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 16 Feb 2024 01:38:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Feb 2024 01:38:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 16 Feb 2024 01:38:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:38:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 01:46:44 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 01:46:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 01:46:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 01:46:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 01:46:44 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 01:47:21 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 01:47:21 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 01:47:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 01:47:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 01:47:26 GMT
USER gradle
# Fri, 16 Feb 2024 01:47:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 01:47:28 GMT
USER root
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17957504d282e5468b289a901c3e69eaaa984cc050162517fc8b5b8f873d0f3a`  
		Last Modified: Fri, 16 Feb 2024 01:42:49 GMT  
		Size: 103.6 MB (103601287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfca02b16f946cadc22fa96733c9445935400d95d0268917b4512d889dbe1b8`  
		Last Modified: Fri, 16 Feb 2024 01:42:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a45aa4c4e140beade15c463ee14bd7d915806eeaef64b1f07b379223c561d8`  
		Last Modified: Fri, 16 Feb 2024 01:42:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293a83db5474898de7fd9f6dccd1c97fd72234751a122cf0dbaaa172c5d8099b`  
		Last Modified: Fri, 16 Feb 2024 01:54:06 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d24eb846759a1801b35b99df3bf67f19ebdfadb25cb33f7cab3ead6be7279b`  
		Last Modified: Fri, 16 Feb 2024 01:54:14 GMT  
		Size: 51.5 MB (51549543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd40f7b6b489e83af192c916ee0835744addfd33ddf7d62c5d5521902ab0fbd`  
		Last Modified: Fri, 16 Feb 2024 01:54:13 GMT  
		Size: 132.8 MB (132815663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fe4c6a87c55e0900570d0727b59ddbafc459d91f71630643c3a47fc1fd0a85`  
		Last Modified: Fri, 16 Feb 2024 01:54:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:49733de1ed5fe80f6278dbb2f52d1aa0163af98351c7562256d04cb10564f227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325960275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a25ed82ba944d0978394905f640d4994707d4a3da35d9abf30cbe94e57204f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:41:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:41:24 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 01 Feb 2024 23:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Feb 2024 23:41:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 01 Feb 2024 23:41:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:41:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 00:49:02 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 00:49:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 00:49:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 00:49:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 00:49:03 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 00:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Feb 2024 23:19:19 GMT
ENV GRADLE_VERSION=8.6
# Fri, 02 Feb 2024 23:19:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 02 Feb 2024 23:19:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 02 Feb 2024 23:19:26 GMT
USER gradle
# Fri, 02 Feb 2024 23:19:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 02 Feb 2024 23:19:28 GMT
USER root
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fe67a29e28e299e1f69ba69453fcb55293e3c5137cc797c4b2099c524988f`  
		Last Modified: Thu, 01 Feb 2024 23:45:28 GMT  
		Size: 12.5 MB (12494090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e8958a60be0d867bdd6836110ce7a6921682d3feddb1a335ceb4a6b158ff2`  
		Last Modified: Thu, 01 Feb 2024 23:45:39 GMT  
		Size: 99.2 MB (99229619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7a84ed0b2e9dd2d83a10e5ee76d508e41bdf1bb4582e1ca975e9f08c3626e`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175b3a789f678dfb0171341ad9085d2714c04014935c3d5cb0549e1811b74ab`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369ec79390edb26444fd32af5bc5ee5b50e260a7ee49aefcd73de8fe1b1061a`  
		Last Modified: Fri, 02 Feb 2024 01:00:11 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90eda0b4804b0dce4676e6d2397ea131a770e6e817ace59b14370cf6c52764da`  
		Last Modified: Fri, 02 Feb 2024 01:00:43 GMT  
		Size: 53.9 MB (53889017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b1c9254f5664492945dce4e49d9e8dd6f417f6516ae7a507c7d674bf3a0858`  
		Last Modified: Fri, 02 Feb 2024 23:22:20 GMT  
		Size: 132.8 MB (132815757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d5ece52dfbeba19067e80f8948d5b7554a85976bdde7f43e8c4ea4b4a60264`  
		Last Modified: Fri, 02 Feb 2024 23:22:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2e9336847830593120954c555e34996507c4766feadf30629c08168f8e22f5bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327895028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295fade20024bb1e26d029d25e042f300cf5736708514945d36d02a240f93190`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:10:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:10:13 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 02:10:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 02:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 02:10:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 09:45:25 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 09:45:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 09:45:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 09:45:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 09:45:25 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 09:45:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Feb 2024 21:42:48 GMT
ENV GRADLE_VERSION=8.6
# Fri, 02 Feb 2024 21:42:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 02 Feb 2024 21:42:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 02 Feb 2024 21:42:53 GMT
USER gradle
# Fri, 02 Feb 2024 21:42:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 02 Feb 2024 21:42:54 GMT
USER root
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d95dd031b6947986c4e6ec03480d6cf870d0799e7c4aedb94072112e09bf46`  
		Last Modified: Fri, 02 Feb 2024 02:14:19 GMT  
		Size: 12.8 MB (12849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd5edc21c73a50bc2baddacc1de06dda6aa85b57b9c2fdb69d8e134481892c`  
		Last Modified: Fri, 02 Feb 2024 02:14:24 GMT  
		Size: 102.7 MB (102705833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f3e998208a18db1290d8c87cdb484fc992e985d5853e40592eefe384dd172`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0b92b348457895515e6390ad70809750c9a696861ac0f5fc499392d661e3ae`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472caccce5a906aab72465d4791e0ca79c58fa7a7d035e6f5f7a7c069a79b7ea`  
		Last Modified: Fri, 02 Feb 2024 09:52:26 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f4f954a177881dd8f7ee9fa4bf2fe076ad52138bf2440d89d991d3c4f8ab02`  
		Last Modified: Fri, 02 Feb 2024 09:52:33 GMT  
		Size: 51.1 MB (51118698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb0c1f34cb7a27f5a23e0904ca9aa962a2ed5499f7a400e438ee374ee275186`  
		Last Modified: Fri, 02 Feb 2024 21:45:51 GMT  
		Size: 132.8 MB (132815756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ddafaf56a21d10b2bba83526ab46a5ef9b82be0d24d71e0ade742d84ca7e67`  
		Last Modified: Fri, 02 Feb 2024 21:45:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:51420d5ed6d81dff064e6f8c0a924f6a7993b3a63178eb97476b35e46de5fbfa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338963222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6415448b099ea62cd5f39bac925ccda48e0ec1ac558c827b0b772ee1e095131e`
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
# Fri, 16 Feb 2024 03:01:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:01:58 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 16 Feb 2024 03:02:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Feb 2024 03:02:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 16 Feb 2024 03:02:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 03:02:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 05:30:08 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 05:30:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 05:30:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 05:30:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 05:30:11 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 05:31:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 05:31:13 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 05:31:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 05:31:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 05:31:26 GMT
USER gradle
# Fri, 16 Feb 2024 05:31:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 05:31:29 GMT
USER root
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edf4d63eca662220ef806035b70b3f249a9404c30da0c2caba78643928225c6`  
		Last Modified: Fri, 16 Feb 2024 03:06:48 GMT  
		Size: 13.8 MB (13769752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213eecc5af1d1261792eaf52fadd60df65d0cf1907d3609cbcaaa48ceaf9f731`  
		Last Modified: Fri, 16 Feb 2024 03:06:55 GMT  
		Size: 101.1 MB (101070349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdde1cad109c07cb977012e934ecea88aedf06587dca7d2ec67c2fc584eb22e`  
		Last Modified: Fri, 16 Feb 2024 03:06:46 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1991b9886e41547ca530fdecdf75702728aaa3505647c557c245d6da16a244d`  
		Last Modified: Fri, 16 Feb 2024 03:06:46 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acaced5d3989404cfa5a110970618b9cbf4133ca1d04327b6e29e2b998bde64`  
		Last Modified: Fri, 16 Feb 2024 05:37:08 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa81a2d026b913e9931e72df913dc8c1be1bae3f7acb85ddd5fefc56da092ca`  
		Last Modified: Fri, 16 Feb 2024 05:37:19 GMT  
		Size: 55.7 MB (55673203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf949755a171bc41a2a32a11bba3023283a37d9c9be594961f3556df6b37bdd6`  
		Last Modified: Fri, 16 Feb 2024 05:37:16 GMT  
		Size: 132.8 MB (132815656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab29d8163b6311150e33114f51809a8c930ee2b905a065c4ba27ba332a6b9bd`  
		Last Modified: Fri, 16 Feb 2024 05:37:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
