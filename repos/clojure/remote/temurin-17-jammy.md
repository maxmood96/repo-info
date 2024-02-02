## `clojure:temurin-17-jammy`

```console
$ docker pull clojure@sha256:aa3b597b13f706953b10cfee446866227b9a2dd60880f593f6a300719c1355ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:caa6c6f287e92493e63ec5026b2c0d9e9d40d0718b6ed73c8b284751a8171e54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244478615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963877d1bfb3155c19fa2d85a8e49fbeb225bf60e8b21e0f0e0a35bd0e53bc39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:45:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:45:02 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 07:45:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 07:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 07:45:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 07:45:12 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 17:25:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:25:43 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:25:58 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:25:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:25:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:25:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:25:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26611c45681a8966387aee7b2e1494405e20bc5a46dc5da0af9228c45f8e8ec4`  
		Last Modified: Fri, 02 Feb 2024 07:50:10 GMT  
		Size: 17.5 MB (17458288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f4ac6e69541680073b21e32dd3de17885de514e36838468fe84707c7b5acf`  
		Last Modified: Fri, 02 Feb 2024 07:50:19 GMT  
		Size: 144.9 MB (144899989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c85a96a6da44b1c1559a390715fd929fae60db504c8b9c745897d737ca485`  
		Last Modified: Fri, 02 Feb 2024 07:50:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d3df2ee4d87245e77cfd06e96a597422956e0194064b0b71152e77d117ff54`  
		Last Modified: Fri, 02 Feb 2024 07:50:07 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542f513112623952b494e090dca06a2cd20f815abd6bdbfc3659decc5945f43`  
		Last Modified: Fri, 02 Feb 2024 17:40:29 GMT  
		Size: 51.7 MB (51670529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b17217c25201e8c787451afe23b6c551d05abdf6be76e99ab293609c79c295`  
		Last Modified: Fri, 02 Feb 2024 17:40:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256c4ca7bc03aa9f6869cbc46dd6f67b635b97fe92c6a1437db6130043f68ca6`  
		Last Modified: Fri, 02 Feb 2024 17:40:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05ba6368c9fd60a1ab74faa562e33efe76fee0a4febc19c16063f6a9f681ad96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242639911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94346599d49ae4fcc09ab8b55874c5e7c363ab88f792a52ee9c6ee65669c4767`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:12:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:05 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 02:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:12:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:12:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:12:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 02:12:16 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 08:33:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:33:36 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:33:48 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:33:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:33:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:33:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:33:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fadd8287e5e4b1c14b1004f595df3205cd8365f31f1b0076456952b05650140`  
		Last Modified: Fri, 02 Feb 2024 02:16:46 GMT  
		Size: 143.7 MB (143724140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad880943b8fd1c5f0f65fa519fb8db732d183e1b1874154300cdae4b8c69eda`  
		Last Modified: Fri, 02 Feb 2024 02:16:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fbd5cf8861f4691a12da0dc0356deb8d8eff4d52bd9c64fd2ff65b7aa9a4be`  
		Last Modified: Fri, 02 Feb 2024 02:16:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d12a80787f1fa5aad5165f0e1ca284ed9ad409380f4c2f18a6ee654aa974cc`  
		Last Modified: Fri, 02 Feb 2024 08:47:42 GMT  
		Size: 51.7 MB (51653076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c44468e95652b74eb400684f318c22e91b13d3e0f27fd6c9997ecb74819f0f5`  
		Last Modified: Fri, 02 Feb 2024 08:47:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b089e2d53ea05c181cc01ed3318ffea9c67063b995e72d143b853d327c4c34`  
		Last Modified: Fri, 02 Feb 2024 08:47:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
