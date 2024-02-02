## `clojure:temurin-8-boot-2.8.3-focal`

```console
$ docker pull clojure@sha256:ce2456f4e490857674ec672b8cae77e8a9a2cd4bee023b401f1e5c84b789b235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-focal` - linux; amd64

```console
$ docker pull clojure@sha256:0822891285f247e3288d3d42e5ea10d9f869c370e48dcfc6081ad53929ff7187
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208271607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cb1426887347fdfbfdd826234aadbd52bf7cce74c2c36da121a5ce4525e7b6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:41:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:41:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:14 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:20 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 17:06:40 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:06:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:06:40 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:06:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:06:46 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:07:10 GMT
RUN boot
# Fri, 02 Feb 2024 17:07:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482e8906db891635177f51c396548100ceb210499ac8ae3e9f43b9b647dc8dc4`  
		Last Modified: Fri, 02 Feb 2024 07:47:19 GMT  
		Size: 16.9 MB (16923425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b19d56aedad13df7de9ebf68dacd6837cba0135113af1ec0197a237a6ef8fb`  
		Last Modified: Fri, 02 Feb 2024 07:47:24 GMT  
		Size: 103.6 MB (103603216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe326c5902552644e5ab7a5afc549f40a11a63ce81abf21985d2fa31d322338`  
		Last Modified: Fri, 02 Feb 2024 07:47:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0900aebd30ff889c811a3fb56eac36b49a667deb9f78c19e53fb2547bd16be69`  
		Last Modified: Fri, 02 Feb 2024 07:47:16 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b5e823f08c99a008675b6cf678194bb6c1c4784966574bca355494411916ab`  
		Last Modified: Fri, 02 Feb 2024 17:29:10 GMT  
		Size: 339.0 KB (339035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8d071981ee6cf09d5671aff7e8177a730ac6d1eba2d5ed32fc8b1e0376e4f8`  
		Last Modified: Fri, 02 Feb 2024 17:29:13 GMT  
		Size: 58.8 MB (58820578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26c9a6669efe7e6028f1da80f7ab099386736e1078a85da5107cc53360a1e8b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205847078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882f40f000765ab595b54ffd2cdd91df06a438f4cff1e74f9a2ae61409941d5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:09:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:09:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:09:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:09:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:09:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 02:09:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 02:09:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 02:09:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:09:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 08:15:33 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:15:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:15:34 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:15:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:15:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:15:45 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:16:43 GMT
RUN boot
# Fri, 02 Feb 2024 08:16:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa774d25e71a9aa0fabab9093684ee75133fee0e119afe23e6f5c3318d0ce083`  
		Last Modified: Fri, 02 Feb 2024 02:14:02 GMT  
		Size: 16.8 MB (16773969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443c78122b3378cf9ddf9feae8f427e4cfe288f9a9a9655ec5357f17f8ea2e0d`  
		Last Modified: Fri, 02 Feb 2024 02:14:06 GMT  
		Size: 102.7 MB (102707151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c9b8e236a0f32142f20239be05a62f5ff3150749935e1c8f9fed0038e305d3`  
		Last Modified: Fri, 02 Feb 2024 02:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4d1d2cfc135626423cca6557c130f11b2a2598bb617e2a487e265791a63c2`  
		Last Modified: Fri, 02 Feb 2024 02:14:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35fe8c0cd1985dfa47c67c8abbbef07e10e92e828f91d801eabfa212fc5d69a`  
		Last Modified: Fri, 02 Feb 2024 08:36:16 GMT  
		Size: 339.0 KB (338969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d4d3ac946ad0b6940b54e7a4f711fcb19f582bf99bf3ce5134333f2a9c95da`  
		Last Modified: Fri, 02 Feb 2024 08:36:25 GMT  
		Size: 58.8 MB (58821035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
