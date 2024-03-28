## `eclipse-temurin:8u402-b06-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:74198c254e59ad06c6d2666f38f4faac0e02c05bd8f80655f6c2c95760b5fc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u402-b06-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e3b2f14e8674d66cf2eeced0ead85df6762c24776c847b84fb5bc9d4e3fb6985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87353346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b016b80bcffb188975966f071b4f9245929fc8b8323e4accc3f849133a346953`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4482b1922021fb7a7193283132c9143a46f8c6e3f22582ccaaeb3023ef8f0ae3`  
		Last Modified: Thu, 28 Mar 2024 02:03:10 GMT  
		Size: 16.9 MB (16920563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04aef2548841b4f52721a782022e4247c0d6869cf73012c83d1a1df37f959d5f`  
		Last Modified: Thu, 28 Mar 2024 02:04:41 GMT  
		Size: 41.8 MB (41847575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c98237e7e8a8545f9fd2f627146f1faa31c33aa6e96d5e22f52504ee6d38de7`  
		Last Modified: Thu, 28 Mar 2024 02:04:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf7a1de717b2e40515b0ab3f4265b2006b66af9f937d9617406b860ae6a102`  
		Last Modified: Thu, 28 Mar 2024 02:04:36 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u402-b06-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:0175fa18a7100d2b8f133ac724ef3d9d61e04f418e652a03308b5a6c1adc3b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79836908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2317de6330bb46dbcb35609ccb0f517b39f62fa766355c0ffe1cc833adbbb5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2956656d6dbbab8b27d20bd8760fc1ca4314e3f3b646580a1a4e5554fedb82`  
		Last Modified: Thu, 28 Mar 2024 01:04:41 GMT  
		Size: 15.7 MB (15664313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636aaa8b27a3c2aa6d5c719509db4d1d7b6d17ec7b3ef30dff5f3dd43f8ea0c3`  
		Last Modified: Thu, 28 Mar 2024 01:05:31 GMT  
		Size: 39.6 MB (39570362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41d416d40c03032f5df16752640e6034461e0627d01e27de9860425092c4f8d`  
		Last Modified: Thu, 28 Mar 2024 01:05:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e2ca8ccbe79f9785eadd85a6894162c3d924a63ac2c114a0f9a29522887e26`  
		Last Modified: Thu, 28 Mar 2024 01:05:25 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u402-b06-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5faed9dce915036c1261874ae6a52d2b76f2949fc9cf6205e8f0f8c6a33db54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84835520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf594f631d04af707e3766ae469ca193baabb0ea70f6a412e1820653291d126c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba6206cf5e5c72dd9d04c2269ff85b1ce7015a33a12585df751669013b790c`  
		Last Modified: Thu, 28 Mar 2024 00:48:26 GMT  
		Size: 16.8 MB (16776713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf17e4a7fffb9172e13271a9acd8ba54b67a9123a17c04e708ad6d8fdbf5fbe`  
		Last Modified: Thu, 28 Mar 2024 00:49:32 GMT  
		Size: 40.9 MB (40853627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0260e52921bc21fc7f2e520c7a0bd7122c6c91f20ab48cb238f621207845779a`  
		Last Modified: Thu, 28 Mar 2024 00:49:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e607a86045304a992ae438c19e85e7989f4da85695e30d1513613f334248632`  
		Last Modified: Thu, 28 Mar 2024 00:49:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u402-b06-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8c75143478bf1f4651bbaedd2d42965606bc3d673ac8f335c1138c4f46dcc488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92780659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df32d4a33c798431c04de78f7a5780f5022548810a0528e238f39afe15d28e9f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cb7b12d05c6f7088aa73f03686c5693c7f8c0e33895a3df3b70702bc8d2037`  
		Last Modified: Thu, 28 Mar 2024 01:40:10 GMT  
		Size: 18.2 MB (18222011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2cb37ea818e0c13f15fdf4007ad3457770ae60907fb82fab39d0558ba42dbd`  
		Last Modified: Thu, 28 Mar 2024 01:41:36 GMT  
		Size: 41.2 MB (41242144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36891cc7ab63d422eb96dfaabaf8727562745f414658033df19e5c69aaae3ae1`  
		Last Modified: Thu, 28 Mar 2024 01:41:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4055201bb1c0ca50de7c77691b1ea241f6d0ca88cc743efc23e111beb559ba4d`  
		Last Modified: Thu, 28 Mar 2024 01:41:30 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
