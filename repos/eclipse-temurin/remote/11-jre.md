## `eclipse-temurin:11-jre`

```console
$ docker pull eclipse-temurin@sha256:93e59ab9a843cd2b43dcd15b809eb5a1ffbcd7261eae7dc20f2549a6acc7972a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9542ef9f5cfb37141dacbfb36f5c7c5d6f1a112b23542bbe4cad83e162f2c16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91585804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbba9f163c9866f617b4f59ff29f5dd71329a299f17b801ff81950b49c8117d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:41:37 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:41:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:41:40 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 10 Oct 2024 07:41:40 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:b627c66b52e2eefb1e7bf48a0fd27633dd3cc98fdeff155513c13f3bdea54ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86192826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab1283b6fa72c7f5960b15dba2a9d625d9e89b51fd3d4a4a30a896651c28ba5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:40 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:41 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:43 GMT
ADD file:a30667697f58d730cc31ae308b1ba41bf25987733d14114fca71a90447988801 in / 
# Thu, 10 Oct 2024 07:43:44 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3d31f15da95226160d2c4d971d0721ec4463223129e41bcf869d34fcb64e5a`  
		Last Modified: Sat, 12 Oct 2024 00:33:02 GMT  
		Size: 13.1 MB (13135136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4f43687d51fee953ef8d45b8cd53e6d9eb6ebce2aa57c98579ca232eb9d185`  
		Last Modified: Sat, 12 Oct 2024 00:34:01 GMT  
		Size: 45.3 MB (45320943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71074f5d0711028fdecc7ff7111d96ee01cb2947f86516893285d2c649256d72`  
		Last Modified: Sat, 12 Oct 2024 00:33:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1044ec4cb8cf787b28bc4e5e76b16f2860ebe65b14eee3addadb27b3148150`  
		Last Modified: Sat, 12 Oct 2024 00:33:54 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:62c1320ddaa766c33f99607ded73da1522b3dff06167f290ac4ca627e063ea71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89311575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fb97aca39f823ecb11f5d836dc349aaa272401cb673471198b3f9a5028744d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:44:36 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:44:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 10 Oct 2024 07:44:40 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3860a0e0eb09022a77ced58131844a4f2d46e7c01d7c0f7a7ba1fa0fc3d132b5`  
		Last Modified: Sat, 12 Oct 2024 00:14:20 GMT  
		Size: 45.6 MB (45557180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf82f1bcce38d91a99de4dadfddc1084f20272d9b6db8b6a2f0fc4d7bb3dbb`  
		Last Modified: Sat, 12 Oct 2024 00:14:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fca13db07011dae250054b123b8203f6f22425760cdc3c04e02888b4e064f30`  
		Last Modified: Sat, 12 Oct 2024 00:14:15 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e9aafaaeaaa45ddd1034e82640dead0c4b9a0609b62dbd66d524769aca0ff584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93081961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ece3a532e1f4e5e29d093701942558862a71528513831afda8eb640d51dd85e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:56 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:00 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 10 Oct 2024 07:44:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15086c23dcc309fa9386aa3f0907d6689b8bc489e8f1311ca8248bffcaf162db`  
		Last Modified: Fri, 11 Oct 2024 23:55:29 GMT  
		Size: 14.9 MB (14914320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2373cf9b2627fb4edb71d9e405f6d160fa93be539f961b28b7fa5fe0688d1b65`  
		Last Modified: Fri, 11 Oct 2024 23:56:29 GMT  
		Size: 42.7 MB (42652104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d047bc9221ecdb10b22fc99b492c6170f4dc8ec2f56c118086ba0a9c7dd3d6db`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5df3c39fe820131c64cd3c3f6f5d9bb3d2413b2bcff6e10753285e00beb16`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:db4957f7feb65f7ff6b2a48f6fafa4dfb96ea07b1246f19a3a6048716e4bb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85677825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668d8847765cbbd799c4873164ae471625fd5a185dae48b15a597e6856d7c975`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:54 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:56 GMT
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
# Thu, 10 Oct 2024 07:43:56 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f4b3060da0149631cc385d58c57350144169b82f0600be0bfca3031687fa1`  
		Last Modified: Sat, 12 Oct 2024 00:25:46 GMT  
		Size: 14.2 MB (14195098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486869d9c1abdd6b1c24f35034f0dd8739f977eae223bf9f465aaeddbed0dd75`  
		Last Modified: Sat, 12 Oct 2024 00:26:07 GMT  
		Size: 40.8 MB (40817330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b5b18f76f974e74439280589c12c19f270f47596f75451ecd6d61f6ad910f4`  
		Last Modified: Sat, 12 Oct 2024 00:26:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e8260d2638105631b8f199221c4d4700c8a7a07c7390528536e08228caadb`  
		Last Modified: Sat, 12 Oct 2024 00:26:01 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:25562bbdc492a63b5a62d503b65d6739fa6ea13adafe5c81ec6a896318751fdf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873980704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9f20b00c77390c54864117c236e4c228423ea9f9deab45014d519166f7772e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:41:35 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 09 Oct 2024 23:46:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.24_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.24_8.msi ;     Write-Host ('Verifying sha256 (da8e0016ee777b9eb4536991ba5e1ca38be049db13239c2f3924f759730fe329) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'da8e0016ee777b9eb4536991ba5e1ca38be049db13239c2f3924f759730fe329') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:46:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf32b74b2294f38fc45be14c479b7b1b1c14ee67f15e4fb589ca3f820814af7`  
		Last Modified: Thu, 10 Oct 2024 00:22:00 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13046206a2c98caf0e85a3e1030e081119ac555db97490a254a8aafa0dfec9e9`  
		Last Modified: Thu, 10 Oct 2024 00:23:53 GMT  
		Size: 74.4 MB (74358170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35d07dee271443e32959f47489639f4710551f5804331102565f059fe5e84e7`  
		Last Modified: Thu, 10 Oct 2024 00:23:44 GMT  
		Size: 278.2 KB (278157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:a10c52816f7748ef27e5290490e400622de15cfb1b4aea3ef596bfd1de29ae1d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1976449361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458fb54bc3857035fc1a889873b63ea23dae51975fc3db056c30a02dd505c993`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:43:03 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 09 Oct 2024 23:47:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.24_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_windows_hotspot_11.0.24_8.msi ;     Write-Host ('Verifying sha256 (da8e0016ee777b9eb4536991ba5e1ca38be049db13239c2f3924f759730fe329) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'da8e0016ee777b9eb4536991ba5e1ca38be049db13239c2f3924f759730fe329') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:48:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce5154c3aa8e57e8c86b6769be6f6e58ee929c2b8723c895e858ecdb52c6f5b`  
		Last Modified: Thu, 10 Oct 2024 00:22:38 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e473f3b1456d1a440502653e38587b798d538ba4b6a8ed3713a9346e3c2b66`  
		Last Modified: Thu, 10 Oct 2024 00:24:10 GMT  
		Size: 74.4 MB (74364163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fc0a0d6c1956d6926cf3ebeb414b083e9dd6c6e2e68d3a9f3d9aea993bc870`  
		Last Modified: Thu, 10 Oct 2024 00:24:01 GMT  
		Size: 257.1 KB (257084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
