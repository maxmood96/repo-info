## `eclipse-temurin:22-noble`

```console
$ docker pull eclipse-temurin@sha256:c9de9009148fecfe7134583f48449e5c6d1f7eb842486e57f5c8e7491cf22704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:22-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:51281e94a96f0e77ddb5d8985a13bd98922b71fb8943b17c30f7f002ffb0d6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207341591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119bbb92172e1643f21312cfb0e063a2821afb678346b9be7f8ff66731182c26`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d10ed217d47bf9ca7ed4ff10640027072814de6488661774d73baf109c03a0`  
		Last Modified: Tue, 17 Sep 2024 01:12:29 GMT  
		Size: 20.2 MB (20240501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5815365a0e83d98b24555f83b654f913632be9fcb37c2daf2b2259318f14da1e`  
		Last Modified: Tue, 17 Sep 2024 01:12:39 GMT  
		Size: 156.5 MB (156487290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2748124e047febb64f4eac3fd6f75a79d50b217e9b56f0be73a4f5609dde065b`  
		Last Modified: Tue, 17 Sep 2024 01:12:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791194ce36d6a70425a4b9e243e052e776a60fe432fcf43d399daf11aca270c8`  
		Last Modified: Tue, 17 Sep 2024 01:12:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2082d0d17859a9ff0202a16d91d20241eaf59dadab0804be87009c3e840e0823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203417972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431c04584797985de370f03306a41f4cd7a3d8c569492c00c45257b5c7458239`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b141587f26721272defe7a8441c82c6c025cf68abf11c95e7a03e721dc40110`  
		Last Modified: Sat, 17 Aug 2024 01:38:00 GMT  
		Size: 19.0 MB (19004619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a374b5775895dc65797da72facef41db14d5f3979612dfbd5da693a0d479c9`  
		Last Modified: Fri, 23 Aug 2024 19:47:22 GMT  
		Size: 154.5 MB (154501072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db2a5830202fd55fd0da6d5cfe5c2d16d0835d17cccd1ab5c4f431ee094fed4`  
		Last Modified: Fri, 23 Aug 2024 19:47:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f9deb08c05f614fdb41320b00241cefb7299bb2d29d9f5b1f3015c3d253d5`  
		Last Modified: Fri, 23 Aug 2024 19:47:12 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bce193a70f50fa5ef5119a67612428747a35c06f9dbb5b3fb3cea36a9f74ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212381831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537be1360744145a113d03d6bede2871bc148c80b60bebd2cc0478e52051a924`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e3c5169d6293fd9f3f82b9deaee88fa754271e536ada337866cf56d5926d7b`  
		Last Modified: Tue, 17 Sep 2024 01:11:33 GMT  
		Size: 20.4 MB (20391476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704573ca6df8d470c3ab95ca77762e7fbc82101178a7c2a52380d3309d95fec3`  
		Last Modified: Tue, 17 Sep 2024 01:11:44 GMT  
		Size: 156.5 MB (156469921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4e48a26238566ea036db271832856c7531e7244260abdd4e0af9506d0eb396`  
		Last Modified: Tue, 17 Sep 2024 01:11:28 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7ac17574cabcfff717eb8e07267e8b06689fcfb4e6bd834551d206ec262ef8`  
		Last Modified: Tue, 17 Sep 2024 01:11:28 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b99d3c077364122819e3893b0aa35e36247709d7effebfa4b4a45e7fbe0601ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192953786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bdcf7e8e77228bf3f92b2bc544cde45cd09df57b93db6e97143e90b2ecb900`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701c545282c2a7358d2fa866a8ab7a8b55a9b824d3584c69be2a4ad062edf3c`  
		Last Modified: Sat, 17 Aug 2024 01:35:45 GMT  
		Size: 16.7 MB (16708922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962ee4ac6eb4fedbba0da61aa304586daa94728ec923db1ccbea4c8283cac091`  
		Last Modified: Fri, 23 Aug 2024 19:49:18 GMT  
		Size: 145.6 MB (145550289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222219fc4086b0c8f5e9494c346b99cbe08e25e8cc42b5037fff0101c563f99c`  
		Last Modified: Fri, 23 Aug 2024 19:49:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f131a27ca78c83bd711fac4756a82367a0295599295498f2ebdf7559ca34a8d4`  
		Last Modified: Fri, 23 Aug 2024 19:49:07 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
