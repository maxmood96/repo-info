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
$ docker pull liquibase@sha256:5de87daf55f9a41b7a54020abfef36db8aff6f04fe98014ccbe2f25bce4d9072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27` - linux; amd64

```console
$ docker pull liquibase@sha256:6846921dcbef3d664da28333771493ab8f747e9262d23aa33d44427afe220e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203965332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399775180752e821b43e80e5d389a3698e44a71d063e52d6cdaa82a422c0a6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 21:52:48 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:07 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:07 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:07 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b345ba1396e8406df1a417529c91dac4e4802e6b18921719b9022f3dfb3734cf`  
		Last Modified: Thu, 28 Mar 2024 02:10:46 GMT  
		Size: 47.2 MB (47163261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0a682e40f83e4da859eee85bc3b44b9444d2949261d3f2a475b030d190ecb`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5752204b57ae4cecf034a16e07738b48b46bfdb2f5aa6981b074fb11f5626`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99aadb837fde40ca6a2dae9a40d04bd1bf50553785b2a7f694dc6307c8fba068`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142bcf0470e7af61487651177e0900dcec93ab4f9a8afaa85deb86c06b45b16d`  
		Last Modified: Fri, 12 Apr 2024 21:53:44 GMT  
		Size: 107.1 MB (107144846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef24c62932c3bc8e48919087bb1c0d5569b260c4d0efbfa4493126aae14494f`  
		Last Modified: Fri, 12 Apr 2024 21:53:39 GMT  
		Size: 6.3 MB (6297806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc0598ef38143545973f089ec27358cd12b59abd95727a4c74036eeaed885e8`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c313aef20cca69ade8dc14a5851ac20a74ab4c48b4a1b049cb90cb8f69842`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:ca6f4de2b6b720f9ca497b237799ba176cd3e36a949c4d5c1239cf060b3de005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200957095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c12a20d72802bd065f1cf577314c07b2fb4fe5d95ab19e3909226b0a8858b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:17 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:36 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17bdfa9148d9619181c35e4af7d8316b4c654657aba355ba11c5bf0c24a3b89`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6aec77f30cba1cf4ed2b4199af718afe7275a40fff8b4cc74e0ae952a3f09d`  
		Last Modified: Fri, 12 Apr 2024 22:10:12 GMT  
		Size: 107.1 MB (107144849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e588b3f4e0c7bcf8339ff2f631d85608a67940e0dd1a6f63031d185c72e4fe2c`  
		Last Modified: Fri, 12 Apr 2024 22:10:08 GMT  
		Size: 5.9 MB (5922778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cc118d4593e39eb8131904ffbe801063d378872727ff186456ac6a48855595`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff52041511678c55870cd6c4fb757f1ced6cca10300c516f4a290b0205e96e5f`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 174.0 B  
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
$ docker pull liquibase@sha256:5de87daf55f9a41b7a54020abfef36db8aff6f04fe98014ccbe2f25bce4d9072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.27.0` - linux; amd64

```console
$ docker pull liquibase@sha256:6846921dcbef3d664da28333771493ab8f747e9262d23aa33d44427afe220e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203965332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399775180752e821b43e80e5d389a3698e44a71d063e52d6cdaa82a422c0a6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 21:52:48 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:07 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:07 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:07 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b345ba1396e8406df1a417529c91dac4e4802e6b18921719b9022f3dfb3734cf`  
		Last Modified: Thu, 28 Mar 2024 02:10:46 GMT  
		Size: 47.2 MB (47163261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0a682e40f83e4da859eee85bc3b44b9444d2949261d3f2a475b030d190ecb`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5752204b57ae4cecf034a16e07738b48b46bfdb2f5aa6981b074fb11f5626`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99aadb837fde40ca6a2dae9a40d04bd1bf50553785b2a7f694dc6307c8fba068`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142bcf0470e7af61487651177e0900dcec93ab4f9a8afaa85deb86c06b45b16d`  
		Last Modified: Fri, 12 Apr 2024 21:53:44 GMT  
		Size: 107.1 MB (107144846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef24c62932c3bc8e48919087bb1c0d5569b260c4d0efbfa4493126aae14494f`  
		Last Modified: Fri, 12 Apr 2024 21:53:39 GMT  
		Size: 6.3 MB (6297806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc0598ef38143545973f089ec27358cd12b59abd95727a4c74036eeaed885e8`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c313aef20cca69ade8dc14a5851ac20a74ab4c48b4a1b049cb90cb8f69842`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.27.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:ca6f4de2b6b720f9ca497b237799ba176cd3e36a949c4d5c1239cf060b3de005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200957095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c12a20d72802bd065f1cf577314c07b2fb4fe5d95ab19e3909226b0a8858b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:17 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:36 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17bdfa9148d9619181c35e4af7d8316b4c654657aba355ba11c5bf0c24a3b89`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6aec77f30cba1cf4ed2b4199af718afe7275a40fff8b4cc74e0ae952a3f09d`  
		Last Modified: Fri, 12 Apr 2024 22:10:12 GMT  
		Size: 107.1 MB (107144849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e588b3f4e0c7bcf8339ff2f631d85608a67940e0dd1a6f63031d185c72e4fe2c`  
		Last Modified: Fri, 12 Apr 2024 22:10:08 GMT  
		Size: 5.9 MB (5922778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cc118d4593e39eb8131904ffbe801063d378872727ff186456ac6a48855595`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff52041511678c55870cd6c4fb757f1ced6cca10300c516f4a290b0205e96e5f`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 174.0 B  
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
$ docker pull liquibase@sha256:5de87daf55f9a41b7a54020abfef36db8aff6f04fe98014ccbe2f25bce4d9072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:6846921dcbef3d664da28333771493ab8f747e9262d23aa33d44427afe220e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203965332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399775180752e821b43e80e5d389a3698e44a71d063e52d6cdaa82a422c0a6f9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 21:52:48 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:52:48 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:52:54 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:52:54 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:07 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:07 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:07 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:07 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:07 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b345ba1396e8406df1a417529c91dac4e4802e6b18921719b9022f3dfb3734cf`  
		Last Modified: Thu, 28 Mar 2024 02:10:46 GMT  
		Size: 47.2 MB (47163261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0a682e40f83e4da859eee85bc3b44b9444d2949261d3f2a475b030d190ecb`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5752204b57ae4cecf034a16e07738b48b46bfdb2f5aa6981b074fb11f5626`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99aadb837fde40ca6a2dae9a40d04bd1bf50553785b2a7f694dc6307c8fba068`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142bcf0470e7af61487651177e0900dcec93ab4f9a8afaa85deb86c06b45b16d`  
		Last Modified: Fri, 12 Apr 2024 21:53:44 GMT  
		Size: 107.1 MB (107144846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef24c62932c3bc8e48919087bb1c0d5569b260c4d0efbfa4493126aae14494f`  
		Last Modified: Fri, 12 Apr 2024 21:53:39 GMT  
		Size: 6.3 MB (6297806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc0598ef38143545973f089ec27358cd12b59abd95727a4c74036eeaed885e8`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c313aef20cca69ade8dc14a5851ac20a74ab4c48b4a1b049cb90cb8f69842`  
		Last Modified: Fri, 12 Apr 2024 21:53:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:ca6f4de2b6b720f9ca497b237799ba176cd3e36a949c4d5c1239cf060b3de005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200957095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c12a20d72802bd065f1cf577314c07b2fb4fe5d95ab19e3909226b0a8858b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:17 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:36 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:36 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17bdfa9148d9619181c35e4af7d8316b4c654657aba355ba11c5bf0c24a3b89`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6aec77f30cba1cf4ed2b4199af718afe7275a40fff8b4cc74e0ae952a3f09d`  
		Last Modified: Fri, 12 Apr 2024 22:10:12 GMT  
		Size: 107.1 MB (107144849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e588b3f4e0c7bcf8339ff2f631d85608a67940e0dd1a6f63031d185c72e4fe2c`  
		Last Modified: Fri, 12 Apr 2024 22:10:08 GMT  
		Size: 5.9 MB (5922778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cc118d4593e39eb8131904ffbe801063d378872727ff186456ac6a48855595`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff52041511678c55870cd6c4fb757f1ced6cca10300c516f4a290b0205e96e5f`  
		Last Modified: Fri, 12 Apr 2024 22:10:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
