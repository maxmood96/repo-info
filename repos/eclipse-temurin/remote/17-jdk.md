## `eclipse-temurin:17-jdk`

```console
$ docker pull eclipse-temurin@sha256:98ca4f83a82e98fe0c5b7f527e37e53349f469475657111789f18f75ab5d94ee
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

### `eclipse-temurin:17-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0f26c13f14768406f60c1c07d6fefdc062458a366d1e4e26d41edacbf90c80de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195559100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3069c3b3cbb3ff1297cd7dac6bcb02413a946cd21a9e545bd71ed62abb33122`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce83d25f400c40aa6cf73004c3c25759517829cd2d12dbd9aefb0f621922ae6`  
		Last Modified: Fri, 11 Oct 2024 23:57:34 GMT  
		Size: 19.8 MB (19766057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead06433d5595020118f9efb30b25219c6604946b5a2288632b882128fed06a`  
		Last Modified: Fri, 11 Oct 2024 23:57:42 GMT  
		Size: 145.2 MB (145177484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a6ea05c286d588dbea7e3d2b7773d44bc5a0c305b687abec3bd2f803023f38`  
		Last Modified: Fri, 11 Oct 2024 23:57:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef6db917bc411a0277c91774e801fd42dc0423ad13f0cdb6f560546578e2e0`  
		Last Modified: Fri, 11 Oct 2024 23:57:31 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:a3709672692b40a84478da68d26a9c49fe5e2d7cd759e3a515fdd77721f77a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188590160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f935e120ae9eca89b9bfb671e8adc515f8f1ff3b0de72eeb49a96f24b36308fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9941494d0affa1584ffd166e1ddf1d3a3eb5d229dfa517be864733b13934f42`  
		Last Modified: Sat, 12 Oct 2024 00:34:12 GMT  
		Size: 18.2 MB (18209140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48bcc7afbc21981d04c2ebff600cf18653b68f8a3cc086b1e0b08dcff2b9975`  
		Last Modified: Sat, 12 Oct 2024 00:34:22 GMT  
		Size: 142.6 MB (142644256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07de939ed9d353a07c7c092182fe037dce7b733e20a54f904b31b8a2527b76`  
		Last Modified: Sat, 12 Oct 2024 00:34:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507c07d7a1e3cd7cdec960dc8d919c490cfe112c0cfbc873660ab6d912daf147`  
		Last Modified: Sat, 12 Oct 2024 00:34:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:62e76ef8e6c51129283ca05ffd8a3b863fd4176c4a8c9d37cb66ed2b58572f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194888217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45049af6911b71cfe558ec1b2c967bb1ca0b560274fadede8701a228970783f6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babae9d38eccb00a7f7fb35b3fda5a1c782265c776159596da9546817843c8a5`  
		Last Modified: Sat, 12 Oct 2024 00:14:32 GMT  
		Size: 21.0 MB (20964953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1624cd11606aaad6356af9b2be34e9bd33785c079fe832002716b98f043119d5`  
		Last Modified: Sat, 12 Oct 2024 00:14:38 GMT  
		Size: 144.0 MB (143967398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23e244e51bdfac285ae96b341865f164046230ac04ff13139937c6542f58c14`  
		Last Modified: Sat, 12 Oct 2024 00:14:29 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e01c57bd3ede45c282a3927f616fc8ee36ba4cd5fd95faa7c63f11c207b25e0`  
		Last Modified: Sat, 12 Oct 2024 00:14:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6fc4ded22f9181c761072e0189d5546d8914b9eba0aa38e849bfbbe9f16bccee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200579497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95a6b56c9b70fd1bceb6223fcae5b46335ccba9407db7d6238ccf04b53e3c3c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3cfd9d478fed07d4b0bdecff494aa712709199789929275d7a03426cd4dd89`  
		Last Modified: Fri, 11 Oct 2024 23:56:43 GMT  
		Size: 20.2 MB (20199883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e205472fdc45dc6cf59d6ed005edf825163ecbc49df1fe00dabbc4439c6a01`  
		Last Modified: Fri, 11 Oct 2024 23:56:52 GMT  
		Size: 144.9 MB (144864065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1953db51e4776cb49ed4e9eb00cacfe347b453c14f45b5fbea801f41f01c5db5`  
		Last Modified: Fri, 11 Oct 2024 23:56:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2d9f1d626e4ffbbb9a97da1029f1acf7dbead3c7b8a7c9df1b992bb222e85`  
		Last Modified: Fri, 11 Oct 2024 23:56:38 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:bae15f7404072f6fc4c1e5885efb7f3310f8fe27201df3d7ce0a7cf161242687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183804787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0ce1f1cf728c6185afa092e1f7cfc32b33b7f393a8c71c280212419273c5b2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cfaec2f2d1c1ba8692d6ef5557e02cdfbbeefa0fe8d06cf5673dd2b42ba90a`  
		Last Modified: Sat, 12 Oct 2024 00:26:16 GMT  
		Size: 18.7 MB (18730996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c285d6f45583b7b1707a48d68753ddefd81df71c54bd0671d9085fd73e3d35`  
		Last Modified: Sat, 12 Oct 2024 00:26:24 GMT  
		Size: 134.4 MB (134408378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c4210cc7c1b2797d9b8c55ef1d4755c392456bacf2139279793c4ad3f7d5d`  
		Last Modified: Sat, 12 Oct 2024 00:26:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb8b4a066f114a2acd7cbfcb60b980d898b635b3f0e1fe5e839b0263f25a238`  
		Last Modified: Sat, 12 Oct 2024 00:26:14 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:81b24e167aa71eb2a145b387ef631117514972f3cd8357d460ba9f85526b86d4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2153339517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a5fea3408c7de48407235a89d5e976bfdca9aa2f20f0ce44e6c801c885b6a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:48:55 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:49:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:50:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:50:11 GMT
CMD ["jshell"]
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
	-	`sha256:6222f88e95e2ade54fc72bc5b001168d2b8f9d4dfe8790c7a9d98d096500b66e`  
		Last Modified: Thu, 10 Oct 2024 00:24:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eccb9b5e86391a0a04c82b47619edbcc4687c1372227bb48fe57ee4dd3de3e`  
		Last Modified: Thu, 10 Oct 2024 00:24:58 GMT  
		Size: 353.7 MB (353707190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1da334b3adc2f33d5647a83a8594749830b6c66d437147f6e16eab38dd00bc`  
		Last Modified: Thu, 10 Oct 2024 00:24:33 GMT  
		Size: 286.5 KB (286524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b38a90d6f6cb4c145e87ed056412e0fa2316439ad6d70c196af1e721ce61d9`  
		Last Modified: Thu, 10 Oct 2024 00:24:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:1ea3feb995f90ad6f3f510c0bad12362dd6d1260e10efc9c32392ad9a099d3b7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2259311554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137c1a970b5dad56ecd321c1807b37c434b5347c9d19a060b55cfcf50cbb06d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:50:24 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:51:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:52:19 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:52:20 GMT
CMD ["jshell"]
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
	-	`sha256:ec183f8c91ef88858125b806eb4896cdc12f748961d5134ebf50daf472609879`  
		Last Modified: Thu, 10 Oct 2024 00:25:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c5b2deff9794cadb8c8a8b3f6e68860370b7f7a4b3529d1256fecd84837cfd`  
		Last Modified: Thu, 10 Oct 2024 00:25:34 GMT  
		Size: 353.7 MB (353701533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc89060e7b600e68b7e00712ed832f1375dcdc6300c113afa3c2a066e089e78d`  
		Last Modified: Thu, 10 Oct 2024 00:25:10 GMT  
		Size: 3.8 MB (3780439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04d9abd115c6dfe022e455a15cbea3b19908c892e37a4e15ce5230898fac2ed`  
		Last Modified: Thu, 10 Oct 2024 00:25:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
