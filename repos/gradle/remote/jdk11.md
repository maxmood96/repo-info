## `gradle:jdk11`

```console
$ docker pull gradle@sha256:d8c5aa4054f79bfe91f56aa18e3fb9dd19ac39eb4ce7cd60cba4b415ca378740
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
$ docker pull gradle@sha256:b614c8475829e6e88264ed79902205c52450600be2161f3a2cbb24850b15542a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (373016534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc77f9bd35c8f92fa60e1114e40bc5f9c819dd4fa2d96f756993a4e65725b5b8`
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
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 01:39:41 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 01:47:35 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 01:47:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 01:47:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 01:47:36 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 01:47:36 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 01:47:52 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 01:47:53 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 01:47:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 01:47:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 01:47:58 GMT
USER gradle
# Fri, 16 Feb 2024 01:47:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 01:47:59 GMT
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
	-	`sha256:aaa60845047dbf87add33eb52cf3139d9cf984a26875656141982395ac9599b7`  
		Last Modified: Fri, 16 Feb 2024 01:43:34 GMT  
		Size: 145.3 MB (145288626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ad4735d3890ac3d52e41b0bcd95d751ac3ff8161d0ad4057cd1055b344d06`  
		Last Modified: Fri, 16 Feb 2024 01:43:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac015eb8852a0d112cbeb863280623a3614c5f88fded523cf145e82dd8cc7d7`  
		Last Modified: Fri, 16 Feb 2024 01:43:22 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758422f04e9730177b64aad52742784c006dd443f3b0d9682e70fb67a6d5fb37`  
		Last Modified: Fri, 16 Feb 2024 01:54:39 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d141a721bc0b160abfea4f3ed6fcc214098e96df518145d1a02657b6c5eea7a`  
		Last Modified: Fri, 16 Feb 2024 01:54:48 GMT  
		Size: 51.6 MB (51550187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc46423df8337028ce215b21b64910d4d05c141a3b8c8104529565a601fa617`  
		Last Modified: Fri, 16 Feb 2024 01:54:46 GMT  
		Size: 132.8 MB (132815745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a333a039dee4b9bf753e780af2a81e76dceb9fddd90bf5fa3194619f0f5384`  
		Last Modified: Fri, 16 Feb 2024 01:54:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d73f646cfa313540300c32fda224c73d8e49bc71995794b6c5935f23937bcab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364556550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f34c31f08cc93f7ed4c6f2ff43264330db199c51c84b30745fa26d99f1fea9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:00 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:20 GMT
ADD file:6767efafdb51cef2acde13d723fa618ffb3cd2155983115496c43ae730e762e6 in / 
# Tue, 13 Feb 2024 10:08:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:39:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:39:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:39:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 07:40:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:40:38 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 07:40:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 07:40:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 07:40:52 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 07:40:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 07:40:52 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 10:14:12 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 10:14:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 10:14:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 10:14:15 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 10:14:15 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 10:14:43 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 10:14:44 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 10:14:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 10:14:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 10:14:53 GMT
USER gradle
# Fri, 16 Feb 2024 10:14:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 10:14:57 GMT
USER root
```

-	Layers:
	-	`sha256:469ff1e358fe0665e6d5ee032bad43f71c0f28f2231f273ce387dcaaaabf733e`  
		Last Modified: Wed, 14 Feb 2024 02:35:21 GMT  
		Size: 27.5 MB (27532464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3f0021e527c265876e11e33d180e2cad20419b59bdaa42f849712c96ff17cb`  
		Last Modified: Fri, 16 Feb 2024 07:42:18 GMT  
		Size: 12.5 MB (12496385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3ed5cbf2c7762bffb7a8352f3d582b85066696455e64a36d47837103068303`  
		Last Modified: Fri, 16 Feb 2024 07:43:08 GMT  
		Size: 137.8 MB (137815100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bf0c80dcc1b757ab23ae3c2d25ecd39191a136eb8d74d61ed89176acd3cbf4`  
		Last Modified: Fri, 16 Feb 2024 07:42:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e5048a032174c9fc8b875bfac0bf3c90f183b53127ba87e2f667b95913b187`  
		Last Modified: Fri, 16 Feb 2024 07:42:53 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8a345f412a84cba54d57bb8d9321f1cb13a3506b2df55ce693d81d51e4ce29`  
		Last Modified: Fri, 16 Feb 2024 10:20:32 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc7028fbb56333f040ae8fe9ab0eac2c55ffc0c1615c329be10a25a95069876`  
		Last Modified: Fri, 16 Feb 2024 10:20:46 GMT  
		Size: 53.9 MB (53891425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57a03fb29d756684ff93aab3ec45d66911aa7caaf1cef701a39a3ccc608f013`  
		Last Modified: Fri, 16 Feb 2024 10:20:46 GMT  
		Size: 132.8 MB (132815747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf536dc39e34351d3cebf995cf3dc09cae865ea1dd4aea9f976bc4b16c6ee0b1`  
		Last Modified: Fri, 16 Feb 2024 10:20:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5828ed2b79287830669de74c6bc0ead6d094e259360b6d8adfc1e27bf151b243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367206876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea89e69cf8f14b2679236694cf6223c87328f9b6e5846097d1be33b298276f2d`
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
# Fri, 16 Feb 2024 04:51:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:52:08 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 04:52:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 04:52:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 04:52:19 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 04:52:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:52:19 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 08:33:44 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 08:33:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 08:33:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 08:33:45 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 08:33:45 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 08:33:57 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 08:33:58 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 08:33:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 08:34:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 08:34:03 GMT
USER gradle
# Fri, 16 Feb 2024 08:34:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 08:34:05 GMT
USER root
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d778895d27e2bcecf0940cf262b977497bd5ef4212e9ef2d3cf030b689dd86b`  
		Last Modified: Fri, 16 Feb 2024 04:54:33 GMT  
		Size: 12.8 MB (12849271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb281288b10eb2e5838abcea6f2980a40da9f9072ce4adcca5ac4c3c5458099d`  
		Last Modified: Fri, 16 Feb 2024 04:55:15 GMT  
		Size: 142.0 MB (142014777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4387739541bc6ae3f08119fb201610aa92380712b4cecc2ce4076f4777443a`  
		Last Modified: Fri, 16 Feb 2024 04:55:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d3c1f774422825f9851f60226693a23c1fa4ea8bfc21b54038586bce58f721`  
		Last Modified: Fri, 16 Feb 2024 04:55:07 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f228cc6c90535d4bfe400a06c37383d0c256144fad6fe4672d76c03e1aea4bcc`  
		Last Modified: Fri, 16 Feb 2024 08:37:51 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96088c2993ef6edee393e5deee6f7ac9c60120872e4eeffbc3fa70ed3e22d9f1`  
		Last Modified: Fri, 16 Feb 2024 08:37:57 GMT  
		Size: 51.1 MB (51121322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0107b5be89bdd353109b6b9aaefb00a57f11118dee08a7c4a71a85e498f56a`  
		Last Modified: Fri, 16 Feb 2024 08:37:56 GMT  
		Size: 132.8 MB (132815746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f551c114ec83c95acb481e6b24df5f30d2e294667b45e6a1c549c0b2140db4b`  
		Last Modified: Fri, 16 Feb 2024 08:37:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:30431cee9d5fa2d29cc032bea86d668e10d0563e7d6b99da39cecd6c957128f4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370307336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4ad46630fbab4fe86fb5890ec4d98193fa4931ba103cbf10e52e0f11d0cf89`
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
# Fri, 16 Feb 2024 03:02:38 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 03:02:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 03:02:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 03:02:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 03:02:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 03:02:56 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 05:31:50 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 05:31:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 05:31:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 05:31:53 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 05:31:54 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 05:32:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 05:32:37 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 05:32:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 05:32:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 05:32:47 GMT
USER gradle
# Fri, 16 Feb 2024 05:32:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 05:32:49 GMT
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
	-	`sha256:f52b752ae72c826c29d82a76e570cd68782c08dbbac4835023974a5157e85c5a`  
		Last Modified: Fri, 16 Feb 2024 03:07:41 GMT  
		Size: 132.4 MB (132413351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed630a71bb84822a8cf178aa8adc3e3d002c3d3142fddc0075fc739579cb99aa`  
		Last Modified: Fri, 16 Feb 2024 03:07:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec45f56b78995b35e4a9e97ef52c8e5fe854d6bb137445d40bf90e9aba100a3b`  
		Last Modified: Fri, 16 Feb 2024 03:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64f460afb9a70377a89ef7b4dad9e3d1a639af9c0035968a02093de4ee2c56c`  
		Last Modified: Fri, 16 Feb 2024 05:37:46 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b45f8ff049551b5d0076d59b74c94b89c291bac1d896783f082736a65a371c`  
		Last Modified: Fri, 16 Feb 2024 05:37:56 GMT  
		Size: 55.7 MB (55674227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f017144192de7ec0cc297e061d3f567e2a5bf0bcd3b0c99a72f431ff1a1678`  
		Last Modified: Fri, 16 Feb 2024 05:37:53 GMT  
		Size: 132.8 MB (132815733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4435d872d3a113304252fd425bd129f1ba163bd89e001c68cccf98d713d36164`  
		Last Modified: Fri, 16 Feb 2024 05:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:f3ebfbf9bfaa792862d13eda33167a3ab09dc76abf60588ec81c6080fdb3bfa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351140700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f9841d82eecd5e4156875640fd2bbcb29fe9f55cc07fd0d1412024dfeb8523`
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
# Fri, 16 Feb 2024 07:19:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:19:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 07:20:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 07:20:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 07:20:10 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 07:20:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 07:20:10 GMT
CMD ["jshell"]
# Fri, 16 Feb 2024 14:40:48 GMT
CMD ["gradle"]
# Fri, 16 Feb 2024 14:40:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Feb 2024 14:40:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Feb 2024 14:40:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Feb 2024 14:40:49 GMT
WORKDIR /home/gradle
# Fri, 16 Feb 2024 14:41:14 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Feb 2024 14:41:18 GMT
ENV GRADLE_VERSION=8.6
# Fri, 16 Feb 2024 14:41:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Fri, 16 Feb 2024 14:41:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 16 Feb 2024 14:41:26 GMT
USER gradle
# Fri, 16 Feb 2024 14:41:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 16 Feb 2024 14:41:27 GMT
USER root
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf42447780e67f524d569bafd0a071b82fc43f8b456857249cfcd7539b7e7577`  
		Last Modified: Fri, 16 Feb 2024 07:38:18 GMT  
		Size: 13.0 MB (12987648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231671c1f25b471900846421e39c3100e01da01fc19e2c1a77f62daed83a60e7`  
		Last Modified: Fri, 16 Feb 2024 07:38:25 GMT  
		Size: 125.4 MB (125415646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e673a7daf83b6b8b32c2c43fc585804545c02792d4390c610bfc35f5bc87f1`  
		Last Modified: Fri, 16 Feb 2024 07:38:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f81563e9f18ee7bc85a4fc9f344fba86e0fac53054df4607bf2a8315e9c9f67`  
		Last Modified: Fri, 16 Feb 2024 07:38:16 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca113bdb51ab0ad7152daaf466c81a61d85e6d23aeb9851dec660ea032634d0f`  
		Last Modified: Fri, 16 Feb 2024 14:57:42 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0364908fd8e1aa0fdc26cb5b36dfde9acf18f7fd3490f00c1abafdd3a47f`  
		Last Modified: Fri, 16 Feb 2024 14:57:50 GMT  
		Size: 51.3 MB (51277526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01bfdba3c09f6a0fdb56428202f200fd978dc32c7e92752c228db626464bbe3`  
		Last Modified: Fri, 16 Feb 2024 14:57:48 GMT  
		Size: 132.8 MB (132815719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09a3a5358f9bbe0908ecee24254af8cd4a1a23c86a5959a8a39166a3a6cad69`  
		Last Modified: Fri, 16 Feb 2024 14:57:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
