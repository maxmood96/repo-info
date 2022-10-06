## `clojure:temurin-8-boot-focal`

```console
$ docker pull clojure@sha256:165ddd558acb4feae6e73c96c0b99c964ad85aac22a6cdfd874d5d3e6141c733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-focal` - linux; amd64

```console
$ docker pull clojure@sha256:f7cd2258e96568a405b0355986818a7daf11dac3f0733341bcc215bf8a1d6fe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207602515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8ecfee956c3303e19176bf10222cc73a38500588cf4c8fbf5e3b202555165a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:59:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 16:59:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 16:59:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 16:59:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:59:41 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 05 Oct 2022 16:59:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 05 Oct 2022 16:59:47 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 06 Oct 2022 03:47:02 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 03:47:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:47:03 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:47:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 03:47:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:47:08 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 03:48:06 GMT
RUN boot
# Thu, 06 Oct 2022 03:48:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233a70a33bef28ffc5642770b6a9c9c03ba4c926c2c5b8a45f96403495eb671`  
		Last Modified: Wed, 05 Oct 2022 17:06:50 GMT  
		Size: 16.4 MB (16352892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bfbc595c37b845e0c9e8e56f250f91ddfff6d8c3140b18f845809c09a97f88`  
		Last Modified: Wed, 05 Oct 2022 17:06:56 GMT  
		Size: 103.5 MB (103516094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe355ec14933ac4b93d181d4d5b946cd24a4b481403e4b5a0d78797ae3dc3e3`  
		Last Modified: Wed, 05 Oct 2022 17:06:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088750ae04ebf0d9e8b03624829bf753c176e1b4a7464f03362aa2c4351d171`  
		Last Modified: Thu, 06 Oct 2022 04:06:25 GMT  
		Size: 337.9 KB (337860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531cf54b76ddf6a8c9f557042590c6cbeed10cfa8ce526de87699afa252faf75`  
		Last Modified: Thu, 06 Oct 2022 04:06:28 GMT  
		Size: 58.8 MB (58821058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55ccc05b32732a99fe8c9fde96bca998db82904e4fefaa157db00cfd90d8fde7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204938435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663d6f19642201d3f27a6abf98671c5ea54b21c80e244dd3a3b128d4aa508c00`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:43:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 15:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 15:43:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 15:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:43:29 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 05 Oct 2022 15:43:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 05 Oct 2022 15:43:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 06 Oct 2022 02:28:09 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:28:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:28:11 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:28:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:28:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:28:20 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:28:35 GMT
RUN boot
# Thu, 06 Oct 2022 02:28:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da1fa3a774b470024bd9b68e8510844f128b9b5581bdf5ddb788da6ae8d71f1`  
		Last Modified: Wed, 05 Oct 2022 15:51:48 GMT  
		Size: 16.2 MB (16215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339f8ac3883c4be3eabf2ab37c56ab59e49d257766d484ff9baf73d86e27d08d`  
		Last Modified: Wed, 05 Oct 2022 15:51:55 GMT  
		Size: 102.6 MB (102615751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a40bcd89322c125c5e8c64b30a96cbc1ee657d7c5a2efa90e013dba30fd2881`  
		Last Modified: Wed, 05 Oct 2022 15:51:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd79ac0311ec73d6411edbf177f5f72da0ac66fdc08a938c13e0eeb4eb7001`  
		Last Modified: Thu, 06 Oct 2022 02:54:41 GMT  
		Size: 100.1 KB (100078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86faf00a97ab78a7646f252b63f6238224ecc9b344464e7c497a9a9321b2204`  
		Last Modified: Thu, 06 Oct 2022 02:54:45 GMT  
		Size: 58.8 MB (58815725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
