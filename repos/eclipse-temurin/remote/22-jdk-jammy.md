## `eclipse-temurin:22-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:fb5176af3268211b954d03ff05b1782b9b3354475aa77288a96d3fb3c4512780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:22-jdk-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9035430037330bf9a38d54d63e9fd0b412ed875dc6ba4853151bd8b6af09fb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204671268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800bfc78299a9e794d7ee30c1692815b59d221170dc7b66afa99eb238de86a9c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e531083e1b0a15cdfac26d85cd8a10953cf6e70ef3798ed13a8457344f2c87f`  
		Last Modified: Thu, 28 Mar 2024 02:13:42 GMT  
		Size: 16.3 MB (16337175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34e2093c50752190bab37a96ab0af869b84a8714e622349658adf61bddee95a`  
		Last Modified: Thu, 28 Mar 2024 02:13:52 GMT  
		Size: 157.9 MB (157881913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b36755bec6f1cea87895a91d5c638c7e0f2aa7b78f0f866b30ff5c50886159`  
		Last Modified: Thu, 28 Mar 2024 02:13:40 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7b39df2027f8c1ade8a458cf1f2d5926a841b79715789ce75737f160b950a`  
		Last Modified: Thu, 28 Mar 2024 02:13:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:67e082c90cda3a359a1f0a94d8058a53bb653b2e4d87495a953cc6668ea0f0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202022635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b921b431d7974db1f90e314ae43fc0d360c192b4ce64fd2388152fdd91004c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eed17e143fcb68d292cc5b280d9ad56bc66b06bfc8c003154c1da1478fd40d4`  
		Last Modified: Thu, 28 Mar 2024 00:56:41 GMT  
		Size: 17.8 MB (17752824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07458f9dc618c8115689f491c4da9a057b898d7b8c4f0d0494cc0ad2af6e30b`  
		Last Modified: Thu, 28 Mar 2024 00:56:48 GMT  
		Size: 155.9 MB (155868295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a8e70dd0980556fa3a25c5be10cb7726ee99a2ad278208d6632bdaafd4ff6b`  
		Last Modified: Thu, 28 Mar 2024 00:56:38 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8702b3f91ac788a7fbb6c3174c929b5ba85940b4a952993d831244e666a3de`  
		Last Modified: Thu, 28 Mar 2024 00:56:38 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8fc6b9c8f2035beccd985ea580b79a20717c874a9ccb4a39d22bebf138ea8ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210218800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e0d2887a1055637a5fceeb357c3447fea25290f5376e7834ebc79eae8df078`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09e1d97679c5f933a3f3bab77d6c984fce5804ba5dc47186747281c376aab91`  
		Last Modified: Thu, 28 Mar 2024 01:49:46 GMT  
		Size: 17.3 MB (17330993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300d46b19aa85778b243c671560f119ad77554073f5867a61237dc406b17d31`  
		Last Modified: Thu, 28 Mar 2024 01:49:57 GMT  
		Size: 157.3 MB (157264190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b643f225320353083507a9752143ef55b7fb3ff26db6778330e220f6c58bb19`  
		Last Modified: Thu, 28 Mar 2024 01:49:41 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df29413d91328fae90422165a7ec893303d0d517d2de3c5caff397b6b16df6fe`  
		Last Modified: Thu, 28 Mar 2024 01:49:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
