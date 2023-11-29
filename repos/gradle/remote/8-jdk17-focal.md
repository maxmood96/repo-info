## `gradle:8-jdk17-focal`

```console
$ docker pull gradle@sha256:711ac839b94e63adf7959bfab50bd0647489fa7c9e34c8deb4ca8c42e2b496cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:8-jdk17-focal` - linux; amd64

```console
$ docker pull gradle@sha256:cfd9bd15d6585fe291861789dd2a7a489358b6f679a5af617d4eef4ab9ddb59c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390627281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01de9b3fefd42774ae7214861d4347e9906e9ab9fdb2c96880eef8a770c1831`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:50:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:50:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:27:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:10 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:27:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e2c5e26f8572544b201bc22a9b28f2b1a3147ab69be111cea07c7f52af252e75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7b175dbe0d6e3c9c23b6ed96449b018308d8fc94a5ecd9c0df8b8bc376c3c18a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='626b2375b08554ad4cbad440a7ff490277bc196852589dd48cab514a7428fa8b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3ae4b254d5b720f94f986481e787fbd67f0667571140ba2e2ae5020ceddbc826';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='45562179b9b623331f741a3a12b298a4d4b901555862148963c86ae7b10d320a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:27:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:27:21 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:27:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:27:21 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 05:22:38 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 05:22:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 05:22:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 05:22:39 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 05:22:39 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 05:22:57 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 31 Oct 2023 05:22:58 GMT
ENV GRADLE_VERSION=8.4
# Tue, 31 Oct 2023 05:22:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
# Tue, 31 Oct 2023 05:23:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 31 Oct 2023 05:23:02 GMT
USER gradle
# Tue, 31 Oct 2023 05:23:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 31 Oct 2023 05:23:03 GMT
USER root
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b30e249cd979e411fd310dc9efb9af0136fcdaa859b1de2d891b1dbb21e72`  
		Last Modified: Mon, 30 Oct 2023 23:35:43 GMT  
		Size: 20.7 MB (20661219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681f2834b6aebb8e22755af16c2fbe996a00f5ab8aa83aa0328964aceeb0f324`  
		Last Modified: Mon, 30 Oct 2023 23:35:51 GMT  
		Size: 144.9 MB (144880392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b200e0ed932cb22894c13d8d280c52730bef46bb10cb43891fbac04c5926db16`  
		Last Modified: Mon, 30 Oct 2023 23:35:39 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8fee9502d1f30de11b84ef3b10d6754c83fea9aeb59bc8e694fdaefdf819e7`  
		Last Modified: Mon, 30 Oct 2023 23:35:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7699ade57402ab8e6326e3f3bfab41ab113bd4d5cd4edb45acc1c190fd659248`  
		Last Modified: Tue, 31 Oct 2023 05:30:17 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22868ce030bab8d2af37881331ac880e8ca86b58ee76bc7fe1b65aae3819f52f`  
		Last Modified: Tue, 31 Oct 2023 05:30:27 GMT  
		Size: 65.5 MB (65489820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10aedf3c10f5a78db3690a41184e52f544268fc99c67c58b1dac2527e3f8223c`  
		Last Modified: Tue, 31 Oct 2023 05:30:24 GMT  
		Size: 131.0 MB (131009729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db720213339cbacfbe0f5468d404e64f5e6ecd8aff1698e74bb81a9183cd825f`  
		Last Modified: Tue, 31 Oct 2023 05:30:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk17-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:7bd914d3ccd3f650847c1e844e5d4526d809c2cef56a874478f0028cee77b2c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379494620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b9e52a26aed02c5ca4918e67ffd09ca5b268fc70b78aacd3b7d3c34efe6a06`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:15:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:00:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:00:33 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:00:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e2c5e26f8572544b201bc22a9b28f2b1a3147ab69be111cea07c7f52af252e75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7b175dbe0d6e3c9c23b6ed96449b018308d8fc94a5ecd9c0df8b8bc376c3c18a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='626b2375b08554ad4cbad440a7ff490277bc196852589dd48cab514a7428fa8b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3ae4b254d5b720f94f986481e787fbd67f0667571140ba2e2ae5020ceddbc826';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='45562179b9b623331f741a3a12b298a4d4b901555862148963c86ae7b10d320a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:00:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:00:48 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:00:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:00:48 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 00:10:36 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 00:10:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 00:10:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 00:10:37 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 00:10:37 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 00:10:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 29 Nov 2023 22:58:11 GMT
ENV GRADLE_VERSION=8.5
# Wed, 29 Nov 2023 22:58:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 29 Nov 2023 22:58:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 29 Nov 2023 22:58:17 GMT
USER gradle
# Wed, 29 Nov 2023 22:58:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 29 Nov 2023 22:58:18 GMT
USER root
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f144f9b13fee3559a44fd346855066eebb23017eb6f35baf0f236ffa76b51`  
		Last Modified: Mon, 30 Oct 2023 23:04:01 GMT  
		Size: 20.0 MB (19961913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dafba4940fcb8f553eb5c6c0a12465fa33d0e1a5fb339f4ce11e457d6d5adf`  
		Last Modified: Mon, 30 Oct 2023 23:04:09 GMT  
		Size: 142.3 MB (142292662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5d973988e09900b87d5b81e58948fe10bfc67b2d1d5a2cd5dccdbddce228f1`  
		Last Modified: Mon, 30 Oct 2023 23:03:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f513fbbc72e92bcb8dd20d0714cc6a3086a852f5e5f3ae29baffe406488bc1`  
		Last Modified: Mon, 30 Oct 2023 23:03:55 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5887ad57bd4f1e19d8edf858ecdbc85829b9ffb8a6f1e912ab5c9ae0337b9733`  
		Last Modified: Tue, 31 Oct 2023 00:15:56 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c8830c4c58cbb33a511f3492872c957b06a8b72488b3a196bb5615a7a333c`  
		Last Modified: Tue, 31 Oct 2023 00:16:10 GMT  
		Size: 60.1 MB (60097724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18231d53ed0ef4e43993119e9268b18438bb0501a0e92063228e3b29d753e7b`  
		Last Modified: Wed, 29 Nov 2023 23:02:46 GMT  
		Size: 132.5 MB (132544721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7715a30c526dc3ec3c1dd383d6446e2570ba5bb3e93bb04c19ab6b60cdb1792f`  
		Last Modified: Wed, 29 Nov 2023 23:02:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk17-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:495637b4243268c62fc249721a72115022bed5502baf82b874b365b39510ff73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 MB (388520425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f821df50212a95f130a4e8cfcd1610fd3c87e07aafc1cb88f1e83dd7f3cd708`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:43:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:43:33 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:43:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e2c5e26f8572544b201bc22a9b28f2b1a3147ab69be111cea07c7f52af252e75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7b175dbe0d6e3c9c23b6ed96449b018308d8fc94a5ecd9c0df8b8bc376c3c18a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='626b2375b08554ad4cbad440a7ff490277bc196852589dd48cab514a7428fa8b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3ae4b254d5b720f94f986481e787fbd67f0667571140ba2e2ae5020ceddbc826';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='45562179b9b623331f741a3a12b298a4d4b901555862148963c86ae7b10d320a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:43:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:43:45 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:43:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:43:46 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 01:41:53 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 01:41:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 01:41:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 01:41:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 01:41:54 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 01:42:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 31 Oct 2023 01:42:09 GMT
ENV GRADLE_VERSION=8.4
# Tue, 31 Oct 2023 01:42:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
# Tue, 31 Oct 2023 01:42:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 31 Oct 2023 01:42:14 GMT
USER gradle
# Tue, 31 Oct 2023 01:42:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 31 Oct 2023 01:42:15 GMT
USER root
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3982c3bf03cb594352f69f3f546c659470c3051ff39a2f19d27f0ef95db66ca`  
		Last Modified: Mon, 30 Oct 2023 23:50:22 GMT  
		Size: 21.4 MB (21378540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96483b1a43145a7af0fdc3be3c947b3728cbf3dc8fe24ebbd4f3130d89298b6d`  
		Last Modified: Mon, 30 Oct 2023 23:50:30 GMT  
		Size: 143.7 MB (143691557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819c3060ffc080bf8dd29efdee66ada09c5a1acb8b0e71f382cf63f5e8a2754b`  
		Last Modified: Mon, 30 Oct 2023 23:50:18 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bd917118368b7a5b4cf5a84521e0fbf7a95755a495330edd4cd040b2065397`  
		Last Modified: Mon, 30 Oct 2023 23:50:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f844d868e9e82e65748cbdb91690320ebfa449ed7defbfa059e79b4da43a1c`  
		Last Modified: Tue, 31 Oct 2023 01:48:24 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b57c471e48adb9575a73a46b7315c6fc52773d4a75ecdacbeed1a1c5425b5b9`  
		Last Modified: Tue, 31 Oct 2023 01:48:33 GMT  
		Size: 65.2 MB (65235657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d611b1dbd0e0f6876f9b79c77111f9660c2d725709662a6b1c12a41ff39d86`  
		Last Modified: Tue, 31 Oct 2023 01:48:32 GMT  
		Size: 131.0 MB (131009726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76eb52e338c8801b55d364a8d4d0d8cd9b5af606f6cf23a7806832d9efd29e2`  
		Last Modified: Tue, 31 Oct 2023 01:48:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk17-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:63148bce598fe9f74a1dda3e97964387a985b2e25f5283a5b88bc1c47c6d7132
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 MB (407010346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21703a4d1802f0a885178df63b39e6dadec759edff2e8bd15bee1e376e99e789`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:52 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:56 GMT
ADD file:ba2394102af0c0584d39af9ec5dd4fa13286293b4607ac7cb9e16d7a2781eef2 in / 
# Tue, 03 Oct 2023 11:03:56 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:59:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 07:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 07:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:23:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:23:26 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:23:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e2c5e26f8572544b201bc22a9b28f2b1a3147ab69be111cea07c7f52af252e75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7b175dbe0d6e3c9c23b6ed96449b018308d8fc94a5ecd9c0df8b8bc376c3c18a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='626b2375b08554ad4cbad440a7ff490277bc196852589dd48cab514a7428fa8b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3ae4b254d5b720f94f986481e787fbd67f0667571140ba2e2ae5020ceddbc826';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='45562179b9b623331f741a3a12b298a4d4b901555862148963c86ae7b10d320a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:23:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:23:46 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:23:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:23:46 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 00:46:52 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 00:46:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 00:46:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 00:46:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 00:46:54 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 00:47:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 29 Nov 2023 23:25:52 GMT
ENV GRADLE_VERSION=8.5
# Wed, 29 Nov 2023 23:25:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 29 Nov 2023 23:25:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 29 Nov 2023 23:26:01 GMT
USER gradle
# Wed, 29 Nov 2023 23:26:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 29 Nov 2023 23:26:03 GMT
USER root
```

-	Layers:
	-	`sha256:f3046919588b0e4a9b202dcd311befda8e46083ce41f424888dcbea91ce8e6e2`  
		Last Modified: Fri, 13 Oct 2023 06:16:08 GMT  
		Size: 33.3 MB (33306424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f221d72c9bf27c7034655ef6e56fad843ff16fdbde81de07ac6186c80efb13`  
		Last Modified: Mon, 30 Oct 2023 23:32:18 GMT  
		Size: 22.7 MB (22707653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914c7fde4ad0188015c6f798c5d3ce7d4836c9a9e52d76c92770b0c58e4b82d2`  
		Last Modified: Mon, 30 Oct 2023 23:32:26 GMT  
		Size: 144.6 MB (144606512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48612460d4008ba52c3b06734e47e535e9e187519e93c40742853b817d24acff`  
		Last Modified: Mon, 30 Oct 2023 23:32:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77cbc4f210e4ea12c0400c68c86c53407c51659eb5b9393b8c6917473b8f0bd`  
		Last Modified: Mon, 30 Oct 2023 23:32:13 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eedac2bc7119d3b1e9029cba86f641eaecd74e5465d1183df71f0fb47a21f13`  
		Last Modified: Tue, 31 Oct 2023 00:52:55 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f263f18af074adf02e32e2e237408468bb88512b48ea615c66fdbaf64c24ae1`  
		Last Modified: Tue, 31 Oct 2023 00:53:11 GMT  
		Size: 73.8 MB (73839642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a677030ad137814abca0e861f7663edca08dd353b5979fa3d8ff8dae0ef5172b`  
		Last Modified: Wed, 29 Nov 2023 23:30:40 GMT  
		Size: 132.5 MB (132544683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c172bcb32cf72959a8cf1be67fb79d69132286047e16286625c455b211d68c6`  
		Last Modified: Wed, 29 Nov 2023 23:30:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk17-focal` - linux; s390x

```console
$ docker pull gradle@sha256:426b146aedb9d390ce17cb32aac08da45024f1b51a59d3bedd73239002ca9b62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377155421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4de6bd81ee6fbeed30f942dd9baf43d2b71ec4ac67b942d24b970432c43b0c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:23 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:23 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:25 GMT
ADD file:1d9be1bf43c126d53bda18c06d12757c021da97c0c9d3a9c9f56df17312095b8 in / 
# Tue, 03 Oct 2023 11:03:25 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 10:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:08:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:26:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:26:10 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:26:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e2c5e26f8572544b201bc22a9b28f2b1a3147ab69be111cea07c7f52af252e75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7b175dbe0d6e3c9c23b6ed96449b018308d8fc94a5ecd9c0df8b8bc376c3c18a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='626b2375b08554ad4cbad440a7ff490277bc196852589dd48cab514a7428fa8b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3ae4b254d5b720f94f986481e787fbd67f0667571140ba2e2ae5020ceddbc826';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='45562179b9b623331f741a3a12b298a4d4b901555862148963c86ae7b10d320a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:26:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:26:25 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:26:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:26:25 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 01:09:21 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 01:09:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 01:09:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 01:09:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 01:09:21 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 01:09:37 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 31 Oct 2023 01:09:42 GMT
ENV GRADLE_VERSION=8.4
# Tue, 31 Oct 2023 01:09:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
# Tue, 31 Oct 2023 01:09:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 31 Oct 2023 01:09:50 GMT
USER gradle
# Tue, 31 Oct 2023 01:09:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e1af3ae886920c3ac87f7a91f816c0c7c436f276a6eefdb3da152100fef72ae
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 31 Oct 2023 01:09:51 GMT
USER root
```

-	Layers:
	-	`sha256:2f51ce1532d2fc433720a55b8851134d5051381dedc2ef6109fb7ebb7a0edb92`  
		Last Modified: Fri, 13 Oct 2023 10:16:26 GMT  
		Size: 27.0 MB (27014102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494e2290595369aef767062fddabdef9e6de2a0df560c06c453d94e7c5355a2a`  
		Last Modified: Mon, 30 Oct 2023 23:30:25 GMT  
		Size: 20.1 MB (20140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fb5771c022579d70525b5a6837136e025d5943281a229f3b71730b405aa2d8`  
		Last Modified: Mon, 30 Oct 2023 23:30:32 GMT  
		Size: 134.2 MB (134187552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25578ef7ccc2e6b4076ec96564d76cf33128cd5b037b7780f78e2916a49b85a1`  
		Last Modified: Mon, 30 Oct 2023 23:30:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3dd53e2414f1077d022b2b8799ee1aa3cf1d7711eb896d4ef724ec83c2d963`  
		Last Modified: Mon, 30 Oct 2023 23:30:22 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02a1abc8af3d6450ad36106a5587beb67c1d2ef362cefc0cfc1f023cbd29736`  
		Last Modified: Tue, 31 Oct 2023 01:14:43 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21e0a2ff77992edbb40e06812dd7cd01699648dd1c3e92881d09813adb4c223`  
		Last Modified: Tue, 31 Oct 2023 01:15:02 GMT  
		Size: 64.8 MB (64797785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c792d793674017427ff12732bda975b93df4eb984e23dbdf14716121c30343b2`  
		Last Modified: Tue, 31 Oct 2023 01:14:51 GMT  
		Size: 131.0 MB (131009717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c92c033f13b34b9a44809992f47d45715783c2e14f5dd363fc713ea7e7e65b5`  
		Last Modified: Tue, 31 Oct 2023 01:14:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
