## `clojure:temurin-19-boot-2.8.3`

```console
$ docker pull clojure@sha256:15d03a259002a850945209dba0964d26a1502d60f70b6e0c181489474ab21d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:790e5fce9c00fc3619df6611055ea81f6ccb8b35dbff2323a9e4585a69d29e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307427460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10c19660f1c6c62d20fed08ef0bfb946edc26d9e60fbe4c6fac2514964b2c12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:20 GMT
ADD file:6cd2e13356aa5339c1f2abd3c210a52f6ed74fae05cd61aa09f37b6a4764f65c in / 
# Tue, 04 Oct 2022 23:35:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 16:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 16:59:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 17:03:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:04:25 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 05 Oct 2022 17:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 17:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 05 Oct 2022 17:04:38 GMT
CMD ["jshell"]
# Thu, 06 Oct 2022 04:01:14 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 04:01:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 04:01:14 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 04:01:19 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 04:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 04:01:19 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 04:01:40 GMT
RUN boot
# Thu, 06 Oct 2022 04:01:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 04:01:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 04:01:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92e523b49ea3d1fae59f5f082437a5f96c244fda6697995920142ff31d59cf`  
		Last Modified: Tue, 04 Oct 2022 03:04:01 GMT  
		Size: 30.4 MB (30428928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b295fc69f17be5773c7d5e868ebc3c55b8e7789141f3aa47363fa69a7a446c7a`  
		Last Modified: Wed, 05 Oct 2022 17:10:08 GMT  
		Size: 17.0 MB (16985789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb16a7f89c003acecb2d099844a9722843884ea5758e2c77259663069f4599a`  
		Last Modified: Wed, 05 Oct 2022 17:11:53 GMT  
		Size: 200.9 MB (200853025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59ab7026df10162a7e5044a7863ffe6bbf44a12fdf74105700d99d4ea9bf3b`  
		Last Modified: Wed, 05 Oct 2022 17:11:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75bba44a2ca63c4ac4b5295b518e31055908bc9ab273b7cddb86f415f326586`  
		Last Modified: Thu, 06 Oct 2022 04:16:23 GMT  
		Size: 338.5 KB (338538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62effa0ef4120fe6099bef9d2bc3c05b6a7f0358f56400a1c0e645ac059c00b1`  
		Last Modified: Thu, 06 Oct 2022 04:16:27 GMT  
		Size: 58.8 MB (58820604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb0dbd4a485632683278cc6c1db6b70089cd8968f110b5b0760dea7db3c322f`  
		Last Modified: Thu, 06 Oct 2022 04:16:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63e75fbecdbd1b7aef3acbe54d0f083b0d50801c9a5a5dc30d338bf1e174d51e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305307743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a6d4dd16bbb1d787f921f5ae360eaf01a09b47e39d03401ed6578a7d5385a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 15:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 15:44:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 15:47:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:48:39 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 05 Oct 2022 15:48:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 15:48:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 05 Oct 2022 15:48:52 GMT
CMD ["jshell"]
# Thu, 06 Oct 2022 02:46:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:46:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:46:29 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:46:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:46:38 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:46:53 GMT
RUN boot
# Thu, 06 Oct 2022 02:46:54 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:46:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:46:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2306aaa12630b303ecdc2ba04820df277229a5f73a0aae69b54a606863c98ae`  
		Last Modified: Wed, 05 Oct 2022 15:55:24 GMT  
		Size: 18.4 MB (18418115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5ffcb6d83959109ba90ac8d52ae2d29354de482b9408a7afd286ae78c70c97`  
		Last Modified: Wed, 05 Oct 2022 15:57:33 GMT  
		Size: 199.6 MB (199589965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc89b60cf0b12144ccc1ae0de4ca4cad86fdf3fdc966e0410f7be5777ab1c4f`  
		Last Modified: Wed, 05 Oct 2022 15:57:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498adeff18246079982835dc7c4fe89668f361157d5c43aeba2ddae80205066c`  
		Last Modified: Thu, 06 Oct 2022 03:06:26 GMT  
		Size: 101.1 KB (101138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a14aaf2fc9b9a3b3da9c1a8748d938b3e6bf0549cd7bd483d6180ba49d90a4b`  
		Last Modified: Thu, 06 Oct 2022 03:06:30 GMT  
		Size: 58.8 MB (58815711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc62d3d4ef95286f3043a13c5cad597589f21073f225c269fa0afe2bc6b6b18`  
		Last Modified: Thu, 06 Oct 2022 03:06:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
