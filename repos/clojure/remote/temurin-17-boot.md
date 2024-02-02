## `clojure:temurin-17-boot`

```console
$ docker pull clojure@sha256:3d11cf3a283e892868f1bf481a8333bd54335a9644deb942e73ba0a717c5ae15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot` - linux; amd64

```console
$ docker pull clojure@sha256:2b32afcc6cfe1937e5b34b79108bfb609107695b4b037e32ee70f51c8d3f7875
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251968399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa0c2f53c8ef5349143afa52ca4b692797bb500710f1f320a596ac5ccbf1aa3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Fri, 02 Feb 2024 17:20:56 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:20:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:20:56 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:21:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:21:02 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:21:19 GMT
RUN boot
# Fri, 02 Feb 2024 17:21:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:21:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:21:19 GMT
CMD ["repl"]
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
	-	`sha256:2233acc4adb5f25818146c1b8af89d5b4d9aa4d66d0d9a8c7117409c95106cc3`  
		Last Modified: Fri, 02 Feb 2024 17:37:24 GMT  
		Size: 340.6 KB (340597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab24135b5f200993c854c5386a1e32254fbbb73fe56af0a7bcdb8c715812b40b`  
		Last Modified: Fri, 02 Feb 2024 17:37:26 GMT  
		Size: 58.8 MB (58820336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ae1aa6c11329d48ac73fd34203a61967f050a42ef60c33d558ac2a8b00082f`  
		Last Modified: Fri, 02 Feb 2024 17:37:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:438e0dc8c7f99957b0fe37109dff04f4397fdda81cbcfb798f9f701e311c990e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250147538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acf1e84f4688e4dcf4fa6b1286e0b1e1448e3041f1277765d43891590352ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Fri, 02 Feb 2024 08:29:42 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:29:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:29:42 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:29:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:29:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:29:47 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:30:05 GMT
RUN boot
# Fri, 02 Feb 2024 08:30:05 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:30:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:30:05 GMT
CMD ["repl"]
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
	-	`sha256:004b8813ff21b952fe1b8d841a47a510ffd01b4641c67cd5e7af05ca1a9fbfe5`  
		Last Modified: Fri, 02 Feb 2024 08:44:50 GMT  
		Size: 340.7 KB (340707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82e74a08ab704075870157b5a0914dc40d9b8c2eaa2d0bb46a4d498b2421603`  
		Last Modified: Fri, 02 Feb 2024 08:44:53 GMT  
		Size: 58.8 MB (58820613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad2c4a34971c1618193a9842a628be69e17cb36047bfdf1a72d6902881b85a`  
		Last Modified: Fri, 02 Feb 2024 08:44:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
