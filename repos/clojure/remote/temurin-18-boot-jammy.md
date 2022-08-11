## `clojure:temurin-18-boot-jammy`

```console
$ docker pull clojure@sha256:45a02ad355c0528845a986b7d5e24e6abf8f37ccf4b9f1ba44a812e8a2eee0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-boot-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:78c67d67b395b0dd8987348da1d215eaa08e39eef736123ea07419bf369e032e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (299046319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70dae89fdf920e068fbc45eaeb2b22a712b85e0c2d447fe92086ec35915e1db5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:20:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:25:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 19:27:14 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:27:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 19:27:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:27:26 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:13:23 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:13:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:13:24 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:13:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 20:13:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:13:28 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:13:46 GMT
RUN boot
# Thu, 11 Aug 2022 20:13:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:13:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:13:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b6eaba4d2174e3bed591e0faa47bb5cce268d4172344b196f3fe9feb0bf05e`  
		Last Modified: Thu, 11 Aug 2022 19:36:05 GMT  
		Size: 15.9 MB (15884335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100f50896a87a3d076ca4667ed17688ca6a830d5320726e4dd590c1b1ae66cc1`  
		Last Modified: Thu, 11 Aug 2022 19:39:12 GMT  
		Size: 193.6 MB (193578342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c49138a982865654d2ce232732081ccdb8d6224b7f697e648e45abd49a32bd`  
		Last Modified: Thu, 11 Aug 2022 19:38:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202b556b9998588e9d4cb3597fd53c3452ebad5736529c733598d3ae46834743`  
		Last Modified: Thu, 11 Aug 2022 20:23:30 GMT  
		Size: 336.6 KB (336571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9346fb0d4d49ba32adb2a5b9970fadf112de11b8e8de1856274e1b48964b3f`  
		Last Modified: Thu, 11 Aug 2022 20:23:33 GMT  
		Size: 58.8 MB (58820360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4519eb09034e9cc0c2c134347cc08d2f266ce4d23024a3b4d155607a9f63989`  
		Last Modified: Thu, 11 Aug 2022 20:23:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-boot-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:733370e965308a63558f974f2d3e22747e068da30a646cc3abfad9a3ef98522a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297050607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe25d8b3273887866e4bb8fe16d41d47e2e402e72a59737735660714834a6de1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:40:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 18:47:35 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 18:47:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 18:47:47 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 18:47:47 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:00:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:00:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:00:28 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:00:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 20:00:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:00:37 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:00:50 GMT
RUN boot
# Thu, 11 Aug 2022 20:00:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:00:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:00:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04632ef1df025fa34842e72b255aed8926a8a48dffec56bfbc4b1ccdf186156e`  
		Last Modified: Thu, 11 Aug 2022 18:57:25 GMT  
		Size: 17.3 MB (17322776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76537264322d6ba91c700ba516285ff6728884981676056c3e5969b1e0fe98c`  
		Last Modified: Thu, 11 Aug 2022 19:00:18 GMT  
		Size: 192.4 MB (192431582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96dd48bb87958098877668c15f27231d47229d2bfef6f10b24865e607243d8d`  
		Last Modified: Thu, 11 Aug 2022 19:00:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c878dcbe6485cefe73aaf9660d4201026a54fdc0aa16a0ad5d4c0fd736b532`  
		Last Modified: Thu, 11 Aug 2022 20:10:16 GMT  
		Size: 98.8 KB (98843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf2f830a43776306ef907a8ad24acc74aabf3ce02032ca8362128524d4a5a8b`  
		Last Modified: Thu, 11 Aug 2022 20:10:20 GMT  
		Size: 58.8 MB (58815691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8257b25c6fdfe687dde446a981f7bc9d8f9f8fc9f3ba38ec8bc524cc28a657`  
		Last Modified: Thu, 11 Aug 2022 20:10:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
