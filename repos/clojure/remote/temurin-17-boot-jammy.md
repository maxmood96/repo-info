## `clojure:temurin-17-boot-jammy`

```console
$ docker pull clojure@sha256:37a0a0c08b3014e6c4bae8c76aeffbf860cf55e7e01173bb2e36925dce61fbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:8bbd0397aaf3485e0429d3121c258cc4f659d5156e2a601c88774a7f9ad08af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251836593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d44876a911224bf73a9a04ecbc3a01908636bfb1e8b9e69573c62b75718e0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 15:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:39:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:40:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:40:43 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 15:40:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 15:40:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 15:40:53 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 15:40:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 15:40:53 GMT
CMD ["jshell"]
# Wed, 16 Aug 2023 18:09:28 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 18:09:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:09:28 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:09:33 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 18:09:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:09:33 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 18:09:51 GMT
RUN boot
# Wed, 16 Aug 2023 18:09:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 18:09:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 18:09:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5980221a1ce1b53ecf2261f165c9bf6a24b845a2418dcf3c7aaf2f3f9e43f2a`  
		Last Modified: Wed, 16 Aug 2023 15:44:40 GMT  
		Size: 17.5 MB (17456341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76044c9858927386b794898d42e68eef89781c3108d02e1a501707a0af7abc3e`  
		Last Modified: Wed, 16 Aug 2023 15:44:49 GMT  
		Size: 144.8 MB (144780035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb65ccf6411874bab2b83dac615eb9dbfd400710230bb445104981793a186c`  
		Last Modified: Wed, 16 Aug 2023 15:44:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e19229f3474f427826915e773f077c6be31eaa7d636ecba6c6978886ef08124`  
		Last Modified: Wed, 16 Aug 2023 15:44:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da18846f13613771866c508d6d6fc07f2689a42f296c11bfe76e400244b7ce1`  
		Last Modified: Wed, 16 Aug 2023 18:18:17 GMT  
		Size: 340.5 KB (340481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef40017ea9f2379cd422428d4fd07134813a9bf80cfabca579b4bf6a94cbd94`  
		Last Modified: Wed, 16 Aug 2023 18:18:21 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a69d353c194e46af41005bca0b6d34ef5c389b72316bf33d009420ab7762802`  
		Last Modified: Wed, 16 Aug 2023 18:18:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67fb7a519c5ae9d8817c1cfafd18de54ad8b31ddf7ec3f3e4d595963ae8fca94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249964793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3271a75be3ccdb5588591383bb1452cacce43387450a5bfaab21db0338b92f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:23:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 14:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 14:23:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 14:24:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:24:46 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 14:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 14:24:57 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 14:24:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 14:24:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 14:24:58 GMT
CMD ["jshell"]
# Wed, 16 Aug 2023 17:26:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 17:26:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:26:27 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:26:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 17:26:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:26:30 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 17:26:48 GMT
RUN boot
# Wed, 16 Aug 2023 17:26:48 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 17:26:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 17:26:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c321f4fb81c9a8d9170f2e66e24c105f438bac179a8c09632ea442be47ef6a3`  
		Last Modified: Wed, 16 Aug 2023 14:28:14 GMT  
		Size: 18.9 MB (18858726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c00170ce19917ea14b85f4fa9825e11b4b74e380192404eafdf981c4df05ada`  
		Last Modified: Wed, 16 Aug 2023 14:28:24 GMT  
		Size: 143.6 MB (143550480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414075e7edcb54ea8db49f693f01dceb960c31d1a8b9fd1d0985a1e3d5f14ea`  
		Last Modified: Wed, 16 Aug 2023 14:28:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc086f9e3d9c4aa949f8fb5501b4e590f4dc111b091ad4037103964f04a4c75`  
		Last Modified: Wed, 16 Aug 2023 14:28:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a10d8ae83333d879806835934f3ab06314f9961d1edad17a748c9d1c3040e1`  
		Last Modified: Wed, 16 Aug 2023 17:34:30 GMT  
		Size: 341.9 KB (341882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014dc86fdfa5443320ed66f072d9939d104ab06b5b67eee25956291143580ee`  
		Last Modified: Wed, 16 Aug 2023 17:34:34 GMT  
		Size: 58.8 MB (58820494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7cfcfcce5e4f2f37100130ec5f86577032ab1d39a1c0900e170497ed2e4dd2`  
		Last Modified: Wed, 16 Aug 2023 17:34:29 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
