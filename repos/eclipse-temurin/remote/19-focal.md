## `eclipse-temurin:19-focal`

```console
$ docker pull eclipse-temurin@sha256:856796efd4592258631c09b18f25e9bfc877c8adec342a5392eaac70a55631e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:19-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5a6542a0a1ca973f4f4147556ed530a75172dfb9b706cf967090cd61ea492d8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249531544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6aa77f251bc93c3ed4663abe96dd3d601ce41e46965ef8a4ad999bcc6ea9d`
-	Default Command: `["jshell"]`

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
# Wed, 05 Oct 2022 17:02:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:03:45 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 05 Oct 2022 17:04:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 17:04:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 05 Oct 2022 17:04:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d22208b60b954bd6e09e29c05404ffe32c8235a504053cf31cf6a197edeece`  
		Last Modified: Wed, 05 Oct 2022 17:09:41 GMT  
		Size: 20.1 MB (20104176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ecd72ae9e9953a153c31e29e1c8a831e2bc44e11b7abcffb08e505e445103a`  
		Last Modified: Wed, 05 Oct 2022 17:11:26 GMT  
		Size: 200.9 MB (200852744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a59de99a1801a99ba204afe2a9860b356cbc70fdbb5adf8b83d9306782490d`  
		Last Modified: Wed, 05 Oct 2022 17:11:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:59c8d8988f35fadbef97088b94e203db21b9a50701e1276ef4ed609ece37b51f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241297989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e80392e20ed6e3d41673393d1d21d7076bdcaed9156b77cc7489985c3f4b013`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 06:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 06:29:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 06 Oct 2022 06:33:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:35:52 GMT
ENV JAVA_VERSION=jdk-19+36
# Thu, 06 Oct 2022 06:36:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 06 Oct 2022 06:36:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 06 Oct 2022 06:36:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41907152dc3d2a88b7d6198bc932fdc3b22116159df581d360b9067781f9ef1`  
		Last Modified: Thu, 06 Oct 2022 06:42:22 GMT  
		Size: 19.5 MB (19486102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27021b243279f1bfe6ed82fada5d1eecab38d29c6d97966ddde9942ebcd7588`  
		Last Modified: Thu, 06 Oct 2022 06:44:16 GMT  
		Size: 197.2 MB (197221619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08744a0626a57dfe06c5127afd2d435cfe5cc9024febe2edda51926f892e5645`  
		Last Modified: Thu, 06 Oct 2022 06:43:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:546b661a41945e7fe6c3de4042c6f099a4a480b6394a34cdc13fa6bf4a3ea6a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247606382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a934ce231deb7cad6bf0e0c178b6b3cb36743852a6cb3d9c9da549e0c6a32`
-	Default Command: `["jshell"]`

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
# Wed, 05 Oct 2022 15:46:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:48:15 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 05 Oct 2022 15:48:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 15:48:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 05 Oct 2022 15:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288ead58ec06eb395c14b048ac8fc356428b280f77e26e9930aed4045c4f4d68`  
		Last Modified: Wed, 05 Oct 2022 15:54:54 GMT  
		Size: 20.8 MB (20823803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11a1e8f1b8ed65143569c69d02c336a57f5cce509066475e358bbcd809383`  
		Last Modified: Wed, 05 Oct 2022 15:56:59 GMT  
		Size: 199.6 MB (199590798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca263d2cce67c5f4adba323f135c952caa20b4f7af9fa58cad7772d73ae241f7`  
		Last Modified: Wed, 05 Oct 2022 15:56:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4791c84505737b8bb4795900400744a7a4cd9998952457bacd6db215782d6594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255344871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02763485d2d52abe2a5d40ebac49f9136273a9c9107aba1e3a71fff6e511e38`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 13:45:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 13:45:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 13:51:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:53:46 GMT
ENV JAVA_VERSION=jdk-19+36
# Tue, 25 Oct 2022 13:54:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Oct 2022 13:54:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Oct 2022 13:54:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a64ad4bc2ecdf82e0999c7ea9f16fd927cf85d64f83821bf651ceec25f8908`  
		Last Modified: Tue, 25 Oct 2022 14:02:22 GMT  
		Size: 22.1 MB (22079033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603eadc2e953566c427625b9cc84044d572bbcddf321cad37e8b5d81ab225b80`  
		Last Modified: Tue, 25 Oct 2022 14:05:04 GMT  
		Size: 200.0 MB (199965120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c7924bc96b00e99369e88a99100a6ea7faf45283969342ab711be6294859d6`  
		Last Modified: Tue, 25 Oct 2022 14:04:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d95968a5eed5b4b746c64c50efe3c683bf648335d06ca8e0ff30cee16dbee072
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234976544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a3b4f6b3c4c943e18572db195a5297e2870e42dc6012c2e5e4521a62e5869a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:58:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 08:58:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 08:58:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 09:03:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:06:12 GMT
ENV JAVA_VERSION=jdk-19+36
# Tue, 25 Oct 2022 09:06:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Oct 2022 09:06:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Oct 2022 09:06:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9e8310c059ea81f37516c947b6ad2e266b5df4f83665270795602ff3e8d9f9`  
		Last Modified: Tue, 25 Oct 2022 09:12:03 GMT  
		Size: 19.5 MB (19546934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64c4f7395b19f6afec967eef894a2838e167de985b24a899772ee5f5d84498d`  
		Last Modified: Tue, 25 Oct 2022 09:13:26 GMT  
		Size: 188.4 MB (188413409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0545f9787a31d8799b19d9af7419dc276599b235578338e1ca4971487f989ae8`  
		Last Modified: Tue, 25 Oct 2022 09:13:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
