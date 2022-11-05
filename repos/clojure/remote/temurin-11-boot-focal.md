## `clojure:temurin-11-boot-focal`

```console
$ docker pull clojure@sha256:7f594b8dab20cd54f134cb25000f9b2ddc33368128921cb896e473edf2d3a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-focal` - linux; amd64

```console
$ docker pull clojure@sha256:6143e57c140bbc18060a839946fbab9cf7b152bccda1f87bfd5cf082ff6e0495
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302554707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c09a0c125a9d203e2b8d89db3d32c2860bd7d46d1bde8af169f367daf1073`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:27:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 17:27:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 17:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 17:27:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:21:27 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:21:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='9ff3b4bd2bac18fb39f3356148efa2dc710ac029e12dc8f18ea1fe6be23bf299';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 23:21:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 23:21:38 GMT
CMD ["jshell"]
# Sat, 05 Nov 2022 01:12:43 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:12:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:12:43 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:13:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:13:46 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:14:05 GMT
RUN boot
# Sat, 05 Nov 2022 01:14:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1869246ce33b7e9d4cfc0f2be772ef684e2425767400664f548b81c2a69eb`  
		Last Modified: Tue, 25 Oct 2022 17:33:48 GMT  
		Size: 16.4 MB (16353656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92987a6c66b9d34f09f6ef0fad549352afbe72ee489c23324c1dd11f432c0243`  
		Last Modified: Fri, 04 Nov 2022 23:27:46 GMT  
		Size: 198.5 MB (198464645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0db103a91cc0800441b2d41aeab58673674235234416ed22e955b92d025c3ab`  
		Last Modified: Fri, 04 Nov 2022 23:27:32 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df15968a6ffc1d6132d1c714efe678c61aee018d512c3a6430c1eafa13bfad4`  
		Last Modified: Sat, 05 Nov 2022 01:26:23 GMT  
		Size: 337.9 KB (337948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc301b9c30e88802aa0b7cb0fe6d86501ba1117c3f16d15bf757a2665ff2172`  
		Last Modified: Sat, 05 Nov 2022 01:26:26 GMT  
		Size: 58.8 MB (58820450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:632d8640b01add8b0c214dac1cf6692c626a380469555061705ccb560e428fc3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297786960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f160d23c1694bd147040676bca65a9bdd924a40fe7f5db8d14cfd3844413e272`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:07:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 01:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:07:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:08:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:40:30 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 22:40:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='9ff3b4bd2bac18fb39f3356148efa2dc710ac029e12dc8f18ea1fe6be23bf299';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 04 Nov 2022 22:40:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 22:40:51 GMT
CMD ["jshell"]
# Fri, 04 Nov 2022 23:13:21 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Nov 2022 23:13:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Nov 2022 23:13:21 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:13:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Nov 2022 23:13:26 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Nov 2022 23:13:43 GMT
RUN boot
# Fri, 04 Nov 2022 23:13:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b9bffe95bbbebdbdfba5c69142aeb65478735d04064fd29982a5b9c980559e`  
		Last Modified: Wed, 26 Oct 2022 01:16:15 GMT  
		Size: 16.2 MB (16216007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c67043335a7043f697bda117df614e35c201fa3cb63419f2b48ef06f40919ba`  
		Last Modified: Fri, 04 Nov 2022 22:45:25 GMT  
		Size: 195.2 MB (195215377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433eedea1da6277a5795ecee1af3019b8504b9bab7666ad9b163815b3d9fac1b`  
		Last Modified: Fri, 04 Nov 2022 22:45:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07916a4815b52e9f56ce297a7425f72e712a8521dd2bc8b69b271745a99a7696`  
		Last Modified: Fri, 04 Nov 2022 23:23:45 GMT  
		Size: 339.1 KB (339050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e53c74955d1b830f38d80168cfd75d1b091bedecbaa3dbe1149834f9d1a76`  
		Last Modified: Fri, 04 Nov 2022 23:23:48 GMT  
		Size: 58.8 MB (58820357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
