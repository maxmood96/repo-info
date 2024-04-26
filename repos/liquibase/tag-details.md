<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.27`](#liquibase427)
-	[`liquibase:4.27-alpine`](#liquibase427-alpine)
-	[`liquibase:4.27.0`](#liquibase4270)
-	[`liquibase:4.27.0-alpine`](#liquibase4270-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.27`

```console
$ docker pull liquibase@sha256:b90904cf535624441484fc726c639103f68a23696526bb5b9a88beae03932527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27` - linux; amd64

```console
$ docker pull liquibase@sha256:5f3f44506dce1a5cefa8ea7eca3e7aab26ab8b2e210c9d2cc3e383c58cfb9a5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204047549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0037750e876061c0c0e4e145887554a0c4051a6ecc008d76a5212d6bb0e39a1`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
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
# Fri, 26 Apr 2024 03:25:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
WORKDIR /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 26 Apr 2024 03:25:06 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_VERSION=0.2.4
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 26 Apr 2024 03:25:14 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Apr 2024 03:25:14 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
USER liquibase:liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Apr 2024 03:25:14 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc23b5f4191f6dddf2d742599b80f634a2e6de0d3615aefa013e720da19a7a16`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ebb511f54230b8129fdab0df67585225c45d16ccfecab686d4c6feb2f0c6f`  
		Last Modified: Fri, 26 Apr 2024 03:25:32 GMT  
		Size: 107.1 MB (107144814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7672f43bc1a181ed02d8fd2f581cf4938c7e49fc342d8d5978c2e3d9ea2e05`  
		Last Modified: Fri, 26 Apr 2024 03:25:28 GMT  
		Size: 6.3 MB (6298244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cad8562b8e6387d7010fa4df5f37abcd8a0d5bea08ccce2805b1b2cf774508e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1287669d7b086d9b52c72bdedae52f0edd92c0cd1d40cb020bce3cc4f711a7e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9916b1dfe6eddcd268c3b9847d49bc1a506d3a15dddca01416db3add0424622f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201035384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c1a19edfcb3fd5f4db7b53a53ffe181f1c1a124450007cb8683d8099d6100`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
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
# Wed, 24 Apr 2024 21:52:49 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
WORKDIR /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Wed, 24 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_VERSION=0.2.4
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 24 Apr 2024 21:53:01 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 24 Apr 2024 21:53:01 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
USER liquibase:liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 21:53:01 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44036d89ece0c6a2ca157ffe0736acae61b4672b50928eb4e8ca06e43081e393`  
		Last Modified: Wed, 24 Apr 2024 17:59:39 GMT  
		Size: 46.7 MB (46716214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7d8aa92f4e9fea32592955f11013f4411d4d90a4da37b0811a1b0c8d153273`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfebd60a844cafed95523be64c05c71a242f2402c5f0dbab9d16a3f8bff29b3`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f2e67b0cf917db51977497f57fb7047edc0a379d8650905d0a98a6a0152a23`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db17c30f8725ec6942cf830e867b6ebb3c75363467a6030d270862a63a2d64`  
		Last Modified: Wed, 24 Apr 2024 21:53:17 GMT  
		Size: 107.1 MB (107144810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2335f13047f4052a34ce41e9a560a6d6a4d36fdfe30d4446a8ac0194644090c`  
		Last Modified: Wed, 24 Apr 2024 21:53:14 GMT  
		Size: 5.9 MB (5923530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61184e51f59eef64723ea8e0a491241cfa22893c7a5d523d43d7e49a0128978`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15adda11992a19399d3958fde385924a74a4faa73f339d2aae0bb459f52ebd5`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.27-alpine`

```console
$ docker pull liquibase@sha256:3569a5194a22fcd31d95ffd183f3c86b036ea893a79dc79aab394cea9eb3903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:8e83243d494f413e5d1dd537beb2ee8a5c3f3236a6fc860caa6d95ce7f87bd4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179118630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60f98847f0d02b37c0091d18ae1546c59490ef6e609604eac0640ae9c9b3a70`
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
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:53:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:25 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:25 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:26 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:26 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:26 GMT
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
	-	`sha256:80890c3d38ea6a223d979b84509075148311447fc8ac6600c294ddfae065f4d1`  
		Last Modified: Fri, 12 Apr 2024 21:54:01 GMT  
		Size: 107.2 MB (107167151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8feb059297540b79a709e55c1606d0df0b30c4353b35114585c6614198663e`  
		Last Modified: Fri, 12 Apr 2024 21:53:56 GMT  
		Size: 6.0 MB (5989458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74eff2b7e0ed7e98c8fe6ca67e84b2c306d9846c1805984d30224a9c36c3360`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e5e492ea3d14e8820abf9031e78088571b07f8a8e98d80c2b21e994283ef36`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5d040853b474bcc42db35dfe65297d1cc95cc475ada0d5afbfd6323fc49f8dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178376991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee5e4a96c378d24640a5b7623ab2ac82bba61db9c3e9c486ae942cb10ede6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 22:09:41 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:43 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 22:09:45 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:50 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:50 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:52 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:53 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:53 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5cf91af4c3b9ba459a6c2e1e4720bb24d515e7e1590061221774c5afc05741`  
		Last Modified: Fri, 12 Apr 2024 22:10:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25670433c04b1b51be1d83e9471b255315d5855735fdb5c478de779fc4d36c1a`  
		Last Modified: Fri, 12 Apr 2024 22:10:32 GMT  
		Size: 62.2 MB (62247991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a0662a2f48ebe9e1417bf734bd23a1364ed6ff98e24ba92df730f7103e4a87`  
		Last Modified: Fri, 12 Apr 2024 22:10:30 GMT  
		Size: 107.2 MB (107167120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e8d1878262c3f6371355d3e70fda8d44e1160933043bf3410ad3e8c81747f`  
		Last Modified: Fri, 12 Apr 2024 22:10:26 GMT  
		Size: 5.6 MB (5612200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a4512c1e0f3ab24f8063edc55981331b296f8616aa8946db6b741c6234c38a`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f90ac47caca49d33b4fd4a4dc651d9a11570ab8a4d7f930332efbf7cdaaf670`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.27.0`

```console
$ docker pull liquibase@sha256:b90904cf535624441484fc726c639103f68a23696526bb5b9a88beae03932527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27.0` - linux; amd64

```console
$ docker pull liquibase@sha256:5f3f44506dce1a5cefa8ea7eca3e7aab26ab8b2e210c9d2cc3e383c58cfb9a5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204047549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0037750e876061c0c0e4e145887554a0c4051a6ecc008d76a5212d6bb0e39a1`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
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
# Fri, 26 Apr 2024 03:25:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
WORKDIR /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 26 Apr 2024 03:25:06 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_VERSION=0.2.4
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 26 Apr 2024 03:25:14 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Apr 2024 03:25:14 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
USER liquibase:liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Apr 2024 03:25:14 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc23b5f4191f6dddf2d742599b80f634a2e6de0d3615aefa013e720da19a7a16`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ebb511f54230b8129fdab0df67585225c45d16ccfecab686d4c6feb2f0c6f`  
		Last Modified: Fri, 26 Apr 2024 03:25:32 GMT  
		Size: 107.1 MB (107144814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7672f43bc1a181ed02d8fd2f581cf4938c7e49fc342d8d5978c2e3d9ea2e05`  
		Last Modified: Fri, 26 Apr 2024 03:25:28 GMT  
		Size: 6.3 MB (6298244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cad8562b8e6387d7010fa4df5f37abcd8a0d5bea08ccce2805b1b2cf774508e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1287669d7b086d9b52c72bdedae52f0edd92c0cd1d40cb020bce3cc4f711a7e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9916b1dfe6eddcd268c3b9847d49bc1a506d3a15dddca01416db3add0424622f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201035384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c1a19edfcb3fd5f4db7b53a53ffe181f1c1a124450007cb8683d8099d6100`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
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
# Wed, 24 Apr 2024 21:52:49 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
WORKDIR /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Wed, 24 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_VERSION=0.2.4
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 24 Apr 2024 21:53:01 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 24 Apr 2024 21:53:01 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
USER liquibase:liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 21:53:01 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44036d89ece0c6a2ca157ffe0736acae61b4672b50928eb4e8ca06e43081e393`  
		Last Modified: Wed, 24 Apr 2024 17:59:39 GMT  
		Size: 46.7 MB (46716214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7d8aa92f4e9fea32592955f11013f4411d4d90a4da37b0811a1b0c8d153273`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfebd60a844cafed95523be64c05c71a242f2402c5f0dbab9d16a3f8bff29b3`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f2e67b0cf917db51977497f57fb7047edc0a379d8650905d0a98a6a0152a23`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db17c30f8725ec6942cf830e867b6ebb3c75363467a6030d270862a63a2d64`  
		Last Modified: Wed, 24 Apr 2024 21:53:17 GMT  
		Size: 107.1 MB (107144810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2335f13047f4052a34ce41e9a560a6d6a4d36fdfe30d4446a8ac0194644090c`  
		Last Modified: Wed, 24 Apr 2024 21:53:14 GMT  
		Size: 5.9 MB (5923530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61184e51f59eef64723ea8e0a491241cfa22893c7a5d523d43d7e49a0128978`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15adda11992a19399d3958fde385924a74a4faa73f339d2aae0bb459f52ebd5`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.27.0-alpine`

```console
$ docker pull liquibase@sha256:3569a5194a22fcd31d95ffd183f3c86b036ea893a79dc79aab394cea9eb3903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:8e83243d494f413e5d1dd537beb2ee8a5c3f3236a6fc860caa6d95ce7f87bd4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179118630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60f98847f0d02b37c0091d18ae1546c59490ef6e609604eac0640ae9c9b3a70`
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
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:53:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:25 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:25 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:26 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:26 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:26 GMT
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
	-	`sha256:80890c3d38ea6a223d979b84509075148311447fc8ac6600c294ddfae065f4d1`  
		Last Modified: Fri, 12 Apr 2024 21:54:01 GMT  
		Size: 107.2 MB (107167151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8feb059297540b79a709e55c1606d0df0b30c4353b35114585c6614198663e`  
		Last Modified: Fri, 12 Apr 2024 21:53:56 GMT  
		Size: 6.0 MB (5989458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74eff2b7e0ed7e98c8fe6ca67e84b2c306d9846c1805984d30224a9c36c3360`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e5e492ea3d14e8820abf9031e78088571b07f8a8e98d80c2b21e994283ef36`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5d040853b474bcc42db35dfe65297d1cc95cc475ada0d5afbfd6323fc49f8dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178376991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee5e4a96c378d24640a5b7623ab2ac82bba61db9c3e9c486ae942cb10ede6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 22:09:41 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:43 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 22:09:45 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:50 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:50 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:52 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:53 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:53 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5cf91af4c3b9ba459a6c2e1e4720bb24d515e7e1590061221774c5afc05741`  
		Last Modified: Fri, 12 Apr 2024 22:10:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25670433c04b1b51be1d83e9471b255315d5855735fdb5c478de779fc4d36c1a`  
		Last Modified: Fri, 12 Apr 2024 22:10:32 GMT  
		Size: 62.2 MB (62247991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a0662a2f48ebe9e1417bf734bd23a1364ed6ff98e24ba92df730f7103e4a87`  
		Last Modified: Fri, 12 Apr 2024 22:10:30 GMT  
		Size: 107.2 MB (107167120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e8d1878262c3f6371355d3e70fda8d44e1160933043bf3410ad3e8c81747f`  
		Last Modified: Fri, 12 Apr 2024 22:10:26 GMT  
		Size: 5.6 MB (5612200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a4512c1e0f3ab24f8063edc55981331b296f8616aa8946db6b741c6234c38a`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f90ac47caca49d33b4fd4a4dc651d9a11570ab8a4d7f930332efbf7cdaaf670`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:3569a5194a22fcd31d95ffd183f3c86b036ea893a79dc79aab394cea9eb3903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:8e83243d494f413e5d1dd537beb2ee8a5c3f3236a6fc860caa6d95ce7f87bd4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179118630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60f98847f0d02b37c0091d18ae1546c59490ef6e609604eac0640ae9c9b3a70`
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
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:53:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:25 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:25 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:26 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:26 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:26 GMT
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
	-	`sha256:80890c3d38ea6a223d979b84509075148311447fc8ac6600c294ddfae065f4d1`  
		Last Modified: Fri, 12 Apr 2024 21:54:01 GMT  
		Size: 107.2 MB (107167151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8feb059297540b79a709e55c1606d0df0b30c4353b35114585c6614198663e`  
		Last Modified: Fri, 12 Apr 2024 21:53:56 GMT  
		Size: 6.0 MB (5989458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74eff2b7e0ed7e98c8fe6ca67e84b2c306d9846c1805984d30224a9c36c3360`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e5e492ea3d14e8820abf9031e78088571b07f8a8e98d80c2b21e994283ef36`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5d040853b474bcc42db35dfe65297d1cc95cc475ada0d5afbfd6323fc49f8dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178376991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee5e4a96c378d24640a5b7623ab2ac82bba61db9c3e9c486ae942cb10ede6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 22:09:41 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:43 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 22:09:45 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:50 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:50 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:52 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:53 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:53 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5cf91af4c3b9ba459a6c2e1e4720bb24d515e7e1590061221774c5afc05741`  
		Last Modified: Fri, 12 Apr 2024 22:10:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25670433c04b1b51be1d83e9471b255315d5855735fdb5c478de779fc4d36c1a`  
		Last Modified: Fri, 12 Apr 2024 22:10:32 GMT  
		Size: 62.2 MB (62247991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a0662a2f48ebe9e1417bf734bd23a1364ed6ff98e24ba92df730f7103e4a87`  
		Last Modified: Fri, 12 Apr 2024 22:10:30 GMT  
		Size: 107.2 MB (107167120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e8d1878262c3f6371355d3e70fda8d44e1160933043bf3410ad3e8c81747f`  
		Last Modified: Fri, 12 Apr 2024 22:10:26 GMT  
		Size: 5.6 MB (5612200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a4512c1e0f3ab24f8063edc55981331b296f8616aa8946db6b741c6234c38a`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f90ac47caca49d33b4fd4a4dc651d9a11570ab8a4d7f930332efbf7cdaaf670`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:b90904cf535624441484fc726c639103f68a23696526bb5b9a88beae03932527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:5f3f44506dce1a5cefa8ea7eca3e7aab26ab8b2e210c9d2cc3e383c58cfb9a5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204047549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0037750e876061c0c0e4e145887554a0c4051a6ecc008d76a5212d6bb0e39a1`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
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
# Fri, 26 Apr 2024 03:25:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
WORKDIR /liquibase
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 26 Apr 2024 03:25:01 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 26 Apr 2024 03:25:06 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_VERSION=0.2.4
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 26 Apr 2024 03:25:07 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 26 Apr 2024 03:25:14 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Apr 2024 03:25:14 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Apr 2024 03:25:14 GMT
USER liquibase:liquibase
# Fri, 26 Apr 2024 03:25:14 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Apr 2024 03:25:14 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc23b5f4191f6dddf2d742599b80f634a2e6de0d3615aefa013e720da19a7a16`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ebb511f54230b8129fdab0df67585225c45d16ccfecab686d4c6feb2f0c6f`  
		Last Modified: Fri, 26 Apr 2024 03:25:32 GMT  
		Size: 107.1 MB (107144814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7672f43bc1a181ed02d8fd2f581cf4938c7e49fc342d8d5978c2e3d9ea2e05`  
		Last Modified: Fri, 26 Apr 2024 03:25:28 GMT  
		Size: 6.3 MB (6298244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cad8562b8e6387d7010fa4df5f37abcd8a0d5bea08ccce2805b1b2cf774508e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1287669d7b086d9b52c72bdedae52f0edd92c0cd1d40cb020bce3cc4f711a7e`  
		Last Modified: Fri, 26 Apr 2024 03:25:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9916b1dfe6eddcd268c3b9847d49bc1a506d3a15dddca01416db3add0424622f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201035384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c1a19edfcb3fd5f4db7b53a53ffe181f1c1a124450007cb8683d8099d6100`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
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
# Wed, 24 Apr 2024 21:52:49 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
WORKDIR /liquibase
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Wed, 24 Apr 2024 21:52:49 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Wed, 24 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_VERSION=0.2.4
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Wed, 24 Apr 2024 21:52:55 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Wed, 24 Apr 2024 21:53:01 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Wed, 24 Apr 2024 21:53:01 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Wed, 24 Apr 2024 21:53:01 GMT
USER liquibase:liquibase
# Wed, 24 Apr 2024 21:53:01 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 21:53:01 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44036d89ece0c6a2ca157ffe0736acae61b4672b50928eb4e8ca06e43081e393`  
		Last Modified: Wed, 24 Apr 2024 17:59:39 GMT  
		Size: 46.7 MB (46716214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7d8aa92f4e9fea32592955f11013f4411d4d90a4da37b0811a1b0c8d153273`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfebd60a844cafed95523be64c05c71a242f2402c5f0dbab9d16a3f8bff29b3`  
		Last Modified: Wed, 24 Apr 2024 17:59:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f2e67b0cf917db51977497f57fb7047edc0a379d8650905d0a98a6a0152a23`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db17c30f8725ec6942cf830e867b6ebb3c75363467a6030d270862a63a2d64`  
		Last Modified: Wed, 24 Apr 2024 21:53:17 GMT  
		Size: 107.1 MB (107144810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2335f13047f4052a34ce41e9a560a6d6a4d36fdfe30d4446a8ac0194644090c`  
		Last Modified: Wed, 24 Apr 2024 21:53:14 GMT  
		Size: 5.9 MB (5923530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61184e51f59eef64723ea8e0a491241cfa22893c7a5d523d43d7e49a0128978`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15adda11992a19399d3958fde385924a74a4faa73f339d2aae0bb459f52ebd5`  
		Last Modified: Wed, 24 Apr 2024 21:53:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
