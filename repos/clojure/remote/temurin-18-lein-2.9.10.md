## `clojure:temurin-18-lein-2.9.10`

```console
$ docker pull clojure@sha256:f5efa5d32679ddc626b7a28cb968b320475420386dcb3b33ed8cf12d250ba461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-lein-2.9.10` - linux; amd64

```console
$ docker pull clojure@sha256:f361ecb3fbbabed266319999c48e292612b4dd1beb323bca0cc74cd9cdbd5e2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257779494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc5d85a6f7014dc014bdefecbdfbe70043b3f6d4b3d8406ee0596cd2febf5a`
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
# Fri, 12 Aug 2022 17:23:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Aug 2022 18:28:09 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:28:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='262be608e266fd76d7496af83b2832be853c3aaf7460d6a4da198cd40db74553';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='4cd49b92d13847bfad7b3bf635cca349e2c89c7641748c5288bc40d612cdbbd6';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='030261a2189a8f773fda543a85ab9beb4c430bf81ca5be37cf6cb970b5ccbb03';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='06d0f71e59b0d7112303a2eb95b1c3701054c868100837e642c6204ea71c0e2f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7d6beba8cfc0a8347f278f7414351191a95a707d46b6586e9a786f2669af0f8b';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Aug 2022 18:28:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:28:22 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 18:55:10 GMT
ENV LEIN_VERSION=2.9.10
# Mon, 29 Aug 2022 18:55:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 29 Aug 2022 18:55:10 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 18:55:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Mon, 29 Aug 2022 18:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 29 Aug 2022 18:55:28 GMT
ENV LEIN_ROOT=1
# Mon, 29 Aug 2022 18:55:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Mon, 29 Aug 2022 18:55:30 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 18:55:30 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 18:55:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ffabbc7d493a0023d83d0a6b1e82866abef587a22c60708a4f07dda563de6a`  
		Last Modified: Fri, 12 Aug 2022 17:32:48 GMT  
		Size: 17.0 MB (17001621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dfd3c955c87cc4f481decbed8d811ef68d88cd6f8161c17bc1a5a28214f2a8`  
		Last Modified: Mon, 29 Aug 2022 18:33:39 GMT  
		Size: 193.6 MB (193572386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa48bd4c65a5e9df5d3382230e8da11fae1429ab96f3caf14ce71a77704c2ba7`  
		Last Modified: Mon, 29 Aug 2022 18:33:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b79d427fb2e9c3a0c6895cd1cf31a25e52c7c39dac2443c044e1049b635574`  
		Last Modified: Mon, 29 Aug 2022 19:00:40 GMT  
		Size: 12.4 MB (12380098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73474faee3127649e7f74b218dd34614665ee90b1f81e7560fde4e77fe1f38bc`  
		Last Modified: Mon, 29 Aug 2022 19:00:39 GMT  
		Size: 4.4 MB (4398675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d1a2c73b75af23c9cf34f3b253bdb618a62a91bf0d0fe32d4477727e601868`  
		Last Modified: Mon, 29 Aug 2022 19:00:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-lein-2.9.10` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ae1e871c842b3f38080de55fdcadef4021067c116622445c5f4de0dc1588431
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255787531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e090db0dbd85d2051a9c6d6e46d71d596ab98b66c6a540e61328c0f2e8de31ba`
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
# Fri, 12 Aug 2022 17:45:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:47:32 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Fri, 12 Aug 2022 17:47:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 12 Aug 2022 17:47:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Aug 2022 17:47:44 GMT
CMD ["jshell"]
# Wed, 17 Aug 2022 02:04:29 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 17 Aug 2022 02:04:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Aug 2022 02:04:30 GMT
WORKDIR /tmp
# Wed, 17 Aug 2022 02:04:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 17 Aug 2022 02:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Aug 2022 02:04:55 GMT
ENV LEIN_ROOT=1
# Wed, 17 Aug 2022 02:04:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 17 Aug 2022 02:05:00 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 17 Aug 2022 02:05:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Aug 2022 02:05:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3daf49bfff4711ea3e9c4de6d7bb8d1733d4b962c4d277384d83f2d8d98f367`  
		Last Modified: Fri, 12 Aug 2022 17:56:05 GMT  
		Size: 18.4 MB (18434264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea620e7ab9ca6807e4d0b946afff6497eb2c57c131c81cb5ee81986c5155c0e7`  
		Last Modified: Fri, 12 Aug 2022 17:58:48 GMT  
		Size: 192.4 MB (192432156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4f2dc9eabaa8ef7de91a6adc9f2d3b613163e3b2e29d88a30c0985af39c959`  
		Last Modified: Fri, 12 Aug 2022 17:58:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09ee7e8bc86f35aed41419c6530f54a6db5240f7491c3d5a4483ca3285f76e`  
		Last Modified: Wed, 17 Aug 2022 02:14:48 GMT  
		Size: 12.1 MB (12140863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3be6a5c7bf03019fe782c13e529af659284943dc387b0175625478787932cf`  
		Last Modified: Wed, 17 Aug 2022 02:14:47 GMT  
		Size: 4.4 MB (4398535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3de22749f018ea9e7eefc9f87582208c1f1de1689c41c0de4bd35a7371f35e2`  
		Last Modified: Wed, 17 Aug 2022 02:14:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
