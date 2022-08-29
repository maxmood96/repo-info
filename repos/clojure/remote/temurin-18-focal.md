## `clojure:temurin-18-focal`

```console
$ docker pull clojure@sha256:1d6b89a3d81719b7dbf683adf8583dfe092f04f92b903dd703a525643b9de12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-focal` - linux; amd64

```console
$ docker pull clojure@sha256:16aa5c222adcada305bfd070a4d0e6bf05a10d6d58fe25950f242d993fc0aa8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305265646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2af31c7f3bb34cfa0c0b258b94c0906a90292fb8ceb5e7e3e5a71ab748f4a06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:23:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Aug 2022 18:27:49 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:28:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='262be608e266fd76d7496af83b2832be853c3aaf7460d6a4da198cd40db74553';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='4cd49b92d13847bfad7b3bf635cca349e2c89c7641748c5288bc40d612cdbbd6';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='030261a2189a8f773fda543a85ab9beb4c430bf81ca5be37cf6cb970b5ccbb03';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='06d0f71e59b0d7112303a2eb95b1c3701054c868100837e642c6204ea71c0e2f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7d6beba8cfc0a8347f278f7414351191a95a707d46b6586e9a786f2669af0f8b';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Aug 2022 18:28:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:28:07 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 18:55:42 GMT
ENV CLOJURE_VERSION=1.11.1.1155
# Mon, 29 Aug 2022 18:55:42 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 18:56:04 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7eb9aa2ecc6c0abfdb1578d4b99ca7c2055111aafa38524a12a6fb76fe01f30b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Mon, 29 Aug 2022 18:56:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 29 Aug 2022 18:56:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 18:56:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 18:56:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff450785d414a328de85b6a3efa41eb49c35822535ae4c97558901c3c68dc5a1`  
		Last Modified: Fri, 12 Aug 2022 17:32:12 GMT  
		Size: 20.1 MB (20120218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2d97af7f65cc255d2415ce0e75861ec16e19f7fa962e6cbbe4990ff4a0f973`  
		Last Modified: Mon, 29 Aug 2022 18:32:07 GMT  
		Size: 193.6 MB (193573914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9119b226824d5fefe502a370e8a2a384d9ac169e2687ec3c2500bb7bc8efc5`  
		Last Modified: Mon, 29 Aug 2022 18:31:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b00b91f05ba3332f528174ef65c654ddf19c07346d14c47c7af9d92ed99d1b`  
		Last Modified: Mon, 29 Aug 2022 19:01:18 GMT  
		Size: 63.0 MB (62997723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62fae4abc74e3f86375c7a4d2c4a2e76582c706e9ad2294ab6e16c6cdc4a9ee`  
		Last Modified: Mon, 29 Aug 2022 19:01:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae51ffffe3abba1cca559573d75baf932264e8fc6fbd39a7e0176edf39d637d6`  
		Last Modified: Mon, 29 Aug 2022 19:01:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c10ba09f17fc0b6a99f2e20320ef29309142aeee70d16da47cc8e8e0d308bf11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303345975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0a309a68dc0ba71d0b1711f8344663bd2e69f64245bac6c80c81e98ee692b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:44:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:47:06 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Fri, 12 Aug 2022 17:47:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 12 Aug 2022 17:47:25 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Aug 2022 17:47:26 GMT
CMD ["jshell"]
# Wed, 17 Aug 2022 02:05:07 GMT
ENV CLOJURE_VERSION=1.11.1.1155
# Wed, 17 Aug 2022 02:05:08 GMT
WORKDIR /tmp
# Wed, 17 Aug 2022 02:05:28 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7eb9aa2ecc6c0abfdb1578d4b99ca7c2055111aafa38524a12a6fb76fe01f30b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 17 Aug 2022 02:05:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 17 Aug 2022 02:05:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 17 Aug 2022 02:05:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Aug 2022 02:05:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c0ceb097615de30aaa4bce5d78e683a09d3766624f531951238f11979cc7f`  
		Last Modified: Fri, 12 Aug 2022 17:55:33 GMT  
		Size: 20.8 MB (20839019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b95c41ddbe87405cd280a5b0e9ff73deba94707b2bc5aaee17048c77da3745`  
		Last Modified: Fri, 12 Aug 2022 17:58:18 GMT  
		Size: 192.4 MB (192432495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380a3a75fef9bb1214645b9b3be9316fa0eedc572e7eba1a42d71d63d59e6e1e`  
		Last Modified: Fri, 12 Aug 2022 17:58:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f98faa92af8a85c8b9bc7cd349a1ab0576ad8377a7ef30aceb1aca0849e9c0`  
		Last Modified: Wed, 17 Aug 2022 02:15:14 GMT  
		Size: 62.9 MB (62881485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733bedaf6364ddf27cd2249a65d982965f45f1008f3bb029063dc82a91c0687a`  
		Last Modified: Wed, 17 Aug 2022 02:15:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062eaa7f2471e915f8e7ebd9c9e3f86da31359a20b773ca1360c776124c2ddea`  
		Last Modified: Wed, 17 Aug 2022 02:15:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
