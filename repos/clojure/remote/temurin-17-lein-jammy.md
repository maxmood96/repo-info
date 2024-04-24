## `clojure:temurin-17-lein-jammy`

```console
$ docker pull clojure@sha256:e889608f81f85f75ab24ca6b8b32dc41c6fe438fb08bccb5274d7322b1c035f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:4afdce15b767b2faf5614f326195047430656faac8540ffeebfaedc8eb6a7274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211861955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b481b27b4d963761d591fe3831d70478a3e107e3f4b9d732f376fa4298392949`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 21:26:17 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:26:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:26:18 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:26:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:26:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:26:31 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:26:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:26:34 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:26:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:26:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3320e4e2ae41973a279c466eba6f7af49750691a7d55baabde5b47c635660f`  
		Last Modified: Tue, 16 Apr 2024 04:06:12 GMT  
		Size: 17.5 MB (17456328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d1ab0e2762b5fba301a0551fe91abe41a8074d6d2406f41f5f58e06ce6abe9`  
		Last Modified: Wed, 24 Apr 2024 19:13:50 GMT  
		Size: 145.1 MB (145101280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00739168dc4afe8b7c88461673426d27825c545d22338e0bc9a0c2620f03e2b`  
		Last Modified: Wed, 24 Apr 2024 19:13:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529de4c97235ebe836a18b915388436c2f77f0b10dbf17d56d06c7680b6298b`  
		Last Modified: Wed, 24 Apr 2024 19:13:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f7b59e1f818c47698d6e43d3ae3645139815333320436482ebe8e5412d680`  
		Last Modified: Wed, 24 Apr 2024 21:49:19 GMT  
		Size: 14.5 MB (14464100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e890f95ad53da74f53526fe51f3a9076d078e00cc9121f04e76fa7a957fecf82`  
		Last Modified: Wed, 24 Apr 2024 21:49:19 GMT  
		Size: 4.4 MB (4399156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0a59ff4c73e72211ad4d03ac9c10ecf9c44c243a22f0d53ff6a6379af8836`  
		Last Modified: Wed, 24 Apr 2024 21:49:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78e7d345bb0acba3d725c531e3f929b8a6b8f206c69309d44e021df1b8dbac1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210019926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615c82841f76e24d6e525dfc7cef59bb0cb0630c7217808d4c0d3cf79bea8ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 19:10:39 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:10:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:10:39 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:10:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:10:52 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:10:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:10:54 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:10:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:10:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ca446d1269832583bab37518ceccaf1672995d944d4df514e3d74c11ebc63d`  
		Last Modified: Tue, 16 Apr 2024 02:57:47 GMT  
		Size: 18.9 MB (18858954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0898b87b1ef6cb4f04175fdedf2af363eb9806b440c2cb61fe3ac60fce1cb8c7`  
		Last Modified: Wed, 24 Apr 2024 17:58:27 GMT  
		Size: 143.9 MB (143896121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b56723e9819e854d0f4cc9b159cb754b02b66097b35a21e9eb594c1cef1f4b2`  
		Last Modified: Wed, 24 Apr 2024 17:58:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d4f0a90c6a854a1991528a567af000055f6ac6793d46faee0d0a8b63a8c57`  
		Last Modified: Wed, 24 Apr 2024 17:58:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f7e153e2f293e53e33875e485026d87b96838e990d419b138726c4d5597331`  
		Last Modified: Wed, 24 Apr 2024 19:29:29 GMT  
		Size: 14.5 MB (14464105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c82021ae2ff945b3f2463db612b0c85314bca93716f1dfa7d4ae2c63d48c10a`  
		Last Modified: Wed, 24 Apr 2024 19:29:28 GMT  
		Size: 4.4 MB (4399139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a23f883345e00a821db09d9fc55266de0d7632b4208f4ebe082d7b048da7924`  
		Last Modified: Wed, 24 Apr 2024 19:29:28 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
