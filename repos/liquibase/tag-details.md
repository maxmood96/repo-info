<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.28`](#liquibase428)
-	[`liquibase:4.28-alpine`](#liquibase428-alpine)
-	[`liquibase:4.28.0`](#liquibase4280)
-	[`liquibase:4.28.0-alpine`](#liquibase4280-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.28`

```console
$ docker pull liquibase@sha256:971bb582e6c28970a5ff439e6c4f614c2f451bbbeb9c26702487764d56d859f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.28` - linux; amd64

```console
$ docker pull liquibase@sha256:addaa73730a8659f2526462ae5077300fd0901e8db43325465c81d3e2f1baa46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205056107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f72acd9e6e63b8732d58f2781ddbebd0027f2ba691e98e9604653fcee8ff69`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 10:53:50 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 10:53:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 10:53:57 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 10:54:02 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 10:54:03 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 10:54:03 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae123141ec1dd6c084f83cac1aff9503da1362dac3530435cefcc60680b1d8`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6937fa9b000b576a2dac1d283c96b925d31978aed760610d44166dd5de8ab4a2`  
		Last Modified: Wed, 05 Jun 2024 10:54:21 GMT  
		Size: 108.2 MB (108154400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a14163b5cc65bf6019b8d53d3d9c9e68ce8b3253c6b85fb6059d4e2b329c811`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef85d62f6966ca840f1dc501628054a6121813e53324c1e798af4ebb99431bb`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb634715a4ff5d4f32f682dc496ed401991c96aed9d5ad4cf42f69ac4be273a`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.28` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5f7173826a8958b3b07848649c0845f87912b7f70187ed2d469c0b97e29f9671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202048926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f57cccef3585612fa2ceab2e0fdd111b383cd09f8271c89b35fe1802e7add4`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:37 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 09:23:43 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 09:23:57 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 09:23:57 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb61a99f36d712a1a72eedde96a4c0feefebcee865bba39553141dbb465548d`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a13c1aca7c1f34288275e6195fc8ac837a45f9209c680641610b5408848c8`  
		Last Modified: Wed, 05 Jun 2024 09:24:13 GMT  
		Size: 108.2 MB (108154403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5383ede648c1b164e79ac80d2c3c090391839c84aca2862cf113e7f03a937758`  
		Last Modified: Wed, 05 Jun 2024 09:24:09 GMT  
		Size: 5.9 MB (5924579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17116183dda4a1f2d0b155c7d9f917b84839f5e32b53bfe9b2eed280509bb83e`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17a2d0154f57d6e08c695e06fe6a474ccd373581e4dc251aa0b095ae17296da`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.28-alpine`

```console
$ docker pull liquibase@sha256:9a3edb9c51d42d77ddb0e0a4255ace2bbe6a1054b9a8f35a4d8154b2a6e169f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.28-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:88df19b7563152da0f414b828779777e217c80ff3f683ad69b9d43933ceca9f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180128000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6682295d24e63bdb39f8d475a7f0ad8c5630f90434325320ba608254da5aa7ac`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 21:53:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:53:16 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 21:53:17 GMT
WORKDIR /liquibase
# Thu, 23 May 2024 19:32:02 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 23 May 2024 19:32:03 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 23 May 2024 19:32:09 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 23 May 2024 19:32:09 GMT
ARG LPM_VERSION=0.2.4
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 23 May 2024 19:32:11 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 23 May 2024 19:32:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 23 May 2024 19:32:12 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 23 May 2024 19:32:12 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 23 May 2024 19:32:12 GMT
USER liquibase:liquibase
# Thu, 23 May 2024 19:32:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 23 May 2024 19:32:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b26e1b7d5e53dc3f871fbd5207d7b0dbed83f5652c6b593e7523f327b0995`  
		Last Modified: Fri, 12 Apr 2024 21:53:58 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16375c5e067803a594c16a34069a277129130d10c6e9f5e0dbf7a3487d94215`  
		Last Modified: Fri, 12 Apr 2024 21:54:03 GMT  
		Size: 62.6 MB (62551332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb77b6dc6f8090ac12c00c65d6ea634c83fcd075c285fba37488551f1e81de26`  
		Last Modified: Thu, 23 May 2024 19:32:45 GMT  
		Size: 108.2 MB (108176511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2199d8266f17ac40199f63462f90edf47a3afe8a2e7e89cdeb1fedc8a06f81b3`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 6.0 MB (5989466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba3fbc1bc92c2a466e2ffebad68391b3068c1333e8f3232ce58fc669be27c7`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0208ffd5550473c13ee70ef23b959d1585554899b02467f13c2a60dca99cb1`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.28-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c97af8151505981baf5efc94ce92ad7734e19c886f4b2a53f7bf985d6a61cc71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179415742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3750b359594788f1c8777f2e0ff698db08144f6f415100fe62101f73b39746aa`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:06:43 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 20 Jun 2024 19:06:46 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Thu, 20 Jun 2024 19:06:47 GMT
WORKDIR /liquibase
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 20 Jun 2024 19:06:53 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 20 Jun 2024 19:06:53 GMT
ARG LPM_VERSION=0.2.4
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 20 Jun 2024 19:06:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 20 Jun 2024 19:06:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
USER liquibase:liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:06:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4406234da3a5998e3d1445fd0eb47ad428a631f09e763a640dbe17d75c6c6`  
		Last Modified: Thu, 20 Jun 2024 19:07:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7432ddf70a827b50f9b31076dc5cca2188f6a0569ff3f6b6df5f0eb112bbee`  
		Last Modified: Thu, 20 Jun 2024 19:07:16 GMT  
		Size: 62.3 MB (62268169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0a72bb2023e4e7ed1c0d0c0d5e048f233644e1176f1c73b1b33e8b74e0913`  
		Last Modified: Thu, 20 Jun 2024 19:07:14 GMT  
		Size: 108.2 MB (108176266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353217f147332a4dfe3310e5fadaa6860a6048bba2966209dc539b978072ff`  
		Last Modified: Thu, 20 Jun 2024 19:07:10 GMT  
		Size: 5.6 MB (5612191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3840df3881678ce840651140c48862b735633ba7fb3664529d12309100ddaa`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a198cdd68962571f07d9627fb0bb1cf1c399f8810eb052f201c340878f026bb`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.28.0`

```console
$ docker pull liquibase@sha256:971bb582e6c28970a5ff439e6c4f614c2f451bbbeb9c26702487764d56d859f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.28.0` - linux; amd64

```console
$ docker pull liquibase@sha256:addaa73730a8659f2526462ae5077300fd0901e8db43325465c81d3e2f1baa46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205056107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f72acd9e6e63b8732d58f2781ddbebd0027f2ba691e98e9604653fcee8ff69`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 10:53:50 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 10:53:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 10:53:57 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 10:54:02 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 10:54:03 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 10:54:03 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae123141ec1dd6c084f83cac1aff9503da1362dac3530435cefcc60680b1d8`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6937fa9b000b576a2dac1d283c96b925d31978aed760610d44166dd5de8ab4a2`  
		Last Modified: Wed, 05 Jun 2024 10:54:21 GMT  
		Size: 108.2 MB (108154400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a14163b5cc65bf6019b8d53d3d9c9e68ce8b3253c6b85fb6059d4e2b329c811`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef85d62f6966ca840f1dc501628054a6121813e53324c1e798af4ebb99431bb`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb634715a4ff5d4f32f682dc496ed401991c96aed9d5ad4cf42f69ac4be273a`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.28.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5f7173826a8958b3b07848649c0845f87912b7f70187ed2d469c0b97e29f9671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202048926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f57cccef3585612fa2ceab2e0fdd111b383cd09f8271c89b35fe1802e7add4`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:37 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 09:23:43 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 09:23:57 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 09:23:57 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb61a99f36d712a1a72eedde96a4c0feefebcee865bba39553141dbb465548d`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a13c1aca7c1f34288275e6195fc8ac837a45f9209c680641610b5408848c8`  
		Last Modified: Wed, 05 Jun 2024 09:24:13 GMT  
		Size: 108.2 MB (108154403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5383ede648c1b164e79ac80d2c3c090391839c84aca2862cf113e7f03a937758`  
		Last Modified: Wed, 05 Jun 2024 09:24:09 GMT  
		Size: 5.9 MB (5924579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17116183dda4a1f2d0b155c7d9f917b84839f5e32b53bfe9b2eed280509bb83e`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17a2d0154f57d6e08c695e06fe6a474ccd373581e4dc251aa0b095ae17296da`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.28.0-alpine`

```console
$ docker pull liquibase@sha256:9a3edb9c51d42d77ddb0e0a4255ace2bbe6a1054b9a8f35a4d8154b2a6e169f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.28.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:88df19b7563152da0f414b828779777e217c80ff3f683ad69b9d43933ceca9f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180128000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6682295d24e63bdb39f8d475a7f0ad8c5630f90434325320ba608254da5aa7ac`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 21:53:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:53:16 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 21:53:17 GMT
WORKDIR /liquibase
# Thu, 23 May 2024 19:32:02 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 23 May 2024 19:32:03 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 23 May 2024 19:32:09 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 23 May 2024 19:32:09 GMT
ARG LPM_VERSION=0.2.4
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 23 May 2024 19:32:11 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 23 May 2024 19:32:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 23 May 2024 19:32:12 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 23 May 2024 19:32:12 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 23 May 2024 19:32:12 GMT
USER liquibase:liquibase
# Thu, 23 May 2024 19:32:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 23 May 2024 19:32:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b26e1b7d5e53dc3f871fbd5207d7b0dbed83f5652c6b593e7523f327b0995`  
		Last Modified: Fri, 12 Apr 2024 21:53:58 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16375c5e067803a594c16a34069a277129130d10c6e9f5e0dbf7a3487d94215`  
		Last Modified: Fri, 12 Apr 2024 21:54:03 GMT  
		Size: 62.6 MB (62551332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb77b6dc6f8090ac12c00c65d6ea634c83fcd075c285fba37488551f1e81de26`  
		Last Modified: Thu, 23 May 2024 19:32:45 GMT  
		Size: 108.2 MB (108176511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2199d8266f17ac40199f63462f90edf47a3afe8a2e7e89cdeb1fedc8a06f81b3`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 6.0 MB (5989466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba3fbc1bc92c2a466e2ffebad68391b3068c1333e8f3232ce58fc669be27c7`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0208ffd5550473c13ee70ef23b959d1585554899b02467f13c2a60dca99cb1`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.28.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c97af8151505981baf5efc94ce92ad7734e19c886f4b2a53f7bf985d6a61cc71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179415742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3750b359594788f1c8777f2e0ff698db08144f6f415100fe62101f73b39746aa`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:06:43 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 20 Jun 2024 19:06:46 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Thu, 20 Jun 2024 19:06:47 GMT
WORKDIR /liquibase
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 20 Jun 2024 19:06:53 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 20 Jun 2024 19:06:53 GMT
ARG LPM_VERSION=0.2.4
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 20 Jun 2024 19:06:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 20 Jun 2024 19:06:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
USER liquibase:liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:06:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4406234da3a5998e3d1445fd0eb47ad428a631f09e763a640dbe17d75c6c6`  
		Last Modified: Thu, 20 Jun 2024 19:07:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7432ddf70a827b50f9b31076dc5cca2188f6a0569ff3f6b6df5f0eb112bbee`  
		Last Modified: Thu, 20 Jun 2024 19:07:16 GMT  
		Size: 62.3 MB (62268169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0a72bb2023e4e7ed1c0d0c0d5e048f233644e1176f1c73b1b33e8b74e0913`  
		Last Modified: Thu, 20 Jun 2024 19:07:14 GMT  
		Size: 108.2 MB (108176266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353217f147332a4dfe3310e5fadaa6860a6048bba2966209dc539b978072ff`  
		Last Modified: Thu, 20 Jun 2024 19:07:10 GMT  
		Size: 5.6 MB (5612191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3840df3881678ce840651140c48862b735633ba7fb3664529d12309100ddaa`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a198cdd68962571f07d9627fb0bb1cf1c399f8810eb052f201c340878f026bb`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:9a3edb9c51d42d77ddb0e0a4255ace2bbe6a1054b9a8f35a4d8154b2a6e169f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:88df19b7563152da0f414b828779777e217c80ff3f683ad69b9d43933ceca9f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180128000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6682295d24e63bdb39f8d475a7f0ad8c5630f90434325320ba608254da5aa7ac`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 21:53:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:53:16 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 21:53:17 GMT
WORKDIR /liquibase
# Thu, 23 May 2024 19:32:02 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 23 May 2024 19:32:03 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 23 May 2024 19:32:09 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 23 May 2024 19:32:09 GMT
ARG LPM_VERSION=0.2.4
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 23 May 2024 19:32:11 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 23 May 2024 19:32:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 23 May 2024 19:32:12 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 23 May 2024 19:32:12 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 23 May 2024 19:32:12 GMT
USER liquibase:liquibase
# Thu, 23 May 2024 19:32:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 23 May 2024 19:32:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b26e1b7d5e53dc3f871fbd5207d7b0dbed83f5652c6b593e7523f327b0995`  
		Last Modified: Fri, 12 Apr 2024 21:53:58 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16375c5e067803a594c16a34069a277129130d10c6e9f5e0dbf7a3487d94215`  
		Last Modified: Fri, 12 Apr 2024 21:54:03 GMT  
		Size: 62.6 MB (62551332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb77b6dc6f8090ac12c00c65d6ea634c83fcd075c285fba37488551f1e81de26`  
		Last Modified: Thu, 23 May 2024 19:32:45 GMT  
		Size: 108.2 MB (108176511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2199d8266f17ac40199f63462f90edf47a3afe8a2e7e89cdeb1fedc8a06f81b3`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 6.0 MB (5989466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba3fbc1bc92c2a466e2ffebad68391b3068c1333e8f3232ce58fc669be27c7`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0208ffd5550473c13ee70ef23b959d1585554899b02467f13c2a60dca99cb1`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c97af8151505981baf5efc94ce92ad7734e19c886f4b2a53f7bf985d6a61cc71
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179415742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3750b359594788f1c8777f2e0ff698db08144f6f415100fe62101f73b39746aa`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:06:43 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 20 Jun 2024 19:06:46 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Thu, 20 Jun 2024 19:06:47 GMT
WORKDIR /liquibase
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 20 Jun 2024 19:06:53 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 20 Jun 2024 19:06:53 GMT
ARG LPM_VERSION=0.2.4
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 20 Jun 2024 19:06:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 20 Jun 2024 19:06:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 20 Jun 2024 19:06:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 20 Jun 2024 19:06:56 GMT
USER liquibase:liquibase
# Thu, 20 Jun 2024 19:06:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:06:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4406234da3a5998e3d1445fd0eb47ad428a631f09e763a640dbe17d75c6c6`  
		Last Modified: Thu, 20 Jun 2024 19:07:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7432ddf70a827b50f9b31076dc5cca2188f6a0569ff3f6b6df5f0eb112bbee`  
		Last Modified: Thu, 20 Jun 2024 19:07:16 GMT  
		Size: 62.3 MB (62268169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0a72bb2023e4e7ed1c0d0c0d5e048f233644e1176f1c73b1b33e8b74e0913`  
		Last Modified: Thu, 20 Jun 2024 19:07:14 GMT  
		Size: 108.2 MB (108176266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353217f147332a4dfe3310e5fadaa6860a6048bba2966209dc539b978072ff`  
		Last Modified: Thu, 20 Jun 2024 19:07:10 GMT  
		Size: 5.6 MB (5612191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3840df3881678ce840651140c48862b735633ba7fb3664529d12309100ddaa`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a198cdd68962571f07d9627fb0bb1cf1c399f8810eb052f201c340878f026bb`  
		Last Modified: Thu, 20 Jun 2024 19:07:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:971bb582e6c28970a5ff439e6c4f614c2f451bbbeb9c26702487764d56d859f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:addaa73730a8659f2526462ae5077300fd0901e8db43325465c81d3e2f1baa46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205056107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f72acd9e6e63b8732d58f2781ddbebd0027f2ba691e98e9604653fcee8ff69`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 10:53:50 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 10:53:50 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 10:53:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 10:53:56 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 10:53:57 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 10:54:02 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 10:54:03 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 10:54:03 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 10:54:03 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 10:54:03 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae123141ec1dd6c084f83cac1aff9503da1362dac3530435cefcc60680b1d8`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6937fa9b000b576a2dac1d283c96b925d31978aed760610d44166dd5de8ab4a2`  
		Last Modified: Wed, 05 Jun 2024 10:54:21 GMT  
		Size: 108.2 MB (108154400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a14163b5cc65bf6019b8d53d3d9c9e68ce8b3253c6b85fb6059d4e2b329c811`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef85d62f6966ca840f1dc501628054a6121813e53324c1e798af4ebb99431bb`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb634715a4ff5d4f32f682dc496ed401991c96aed9d5ad4cf42f69ac4be273a`  
		Last Modified: Wed, 05 Jun 2024 10:54:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5f7173826a8958b3b07848649c0845f87912b7f70187ed2d469c0b97e29f9671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202048926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f57cccef3585612fa2ceab2e0fdd111b383cd09f8271c89b35fe1802e7add4`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:37 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
WORKDIR /liquibase
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Wed, 05 Jun 2024 09:23:37 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Wed, 05 Jun 2024 09:23:43 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_VERSION=0.2.4
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 05 Jun 2024 09:23:44 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 05 Jun 2024 09:23:57 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 05 Jun 2024 09:23:57 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 05 Jun 2024 09:23:58 GMT
USER liquibase:liquibase
# Wed, 05 Jun 2024 09:23:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 09:23:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb61a99f36d712a1a72eedde96a4c0feefebcee865bba39553141dbb465548d`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a13c1aca7c1f34288275e6195fc8ac837a45f9209c680641610b5408848c8`  
		Last Modified: Wed, 05 Jun 2024 09:24:13 GMT  
		Size: 108.2 MB (108154403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5383ede648c1b164e79ac80d2c3c090391839c84aca2862cf113e7f03a937758`  
		Last Modified: Wed, 05 Jun 2024 09:24:09 GMT  
		Size: 5.9 MB (5924579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17116183dda4a1f2d0b155c7d9f917b84839f5e32b53bfe9b2eed280509bb83e`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17a2d0154f57d6e08c695e06fe6a474ccd373581e4dc251aa0b095ae17296da`  
		Last Modified: Wed, 05 Jun 2024 09:24:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
