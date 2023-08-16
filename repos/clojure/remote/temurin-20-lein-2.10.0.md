## `clojure:temurin-20-lein-2.10.0`

```console
$ docker pull clojure@sha256:c1d76edbb976b7dd7d83d7ed4953d8b6411e6b6432d87be2618cb511461e56cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-lein-2.10.0` - linux; amd64

```console
$ docker pull clojure@sha256:8b6e0ec9d3f6311e906beeced67b8609df53b66cd564314410b1f2eb3e2894d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218069107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480b952e24a645b249f8addbb666ec1d314846a12d97844a53b0f353a0b4c8f6`
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
# Wed, 16 Aug 2023 15:41:25 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 16 Aug 2023 15:41:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b475bcc23db0bd618c815bb8f11d8e084dc58288ea3bcdf4e7f389ed41c89f56';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d91842e9c172967ac397076523249d05a82ead51b0006838f5f0315ad52222c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 15:41:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 15:41:38 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 15:41:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 15:41:38 GMT
CMD ["jshell"]
# Wed, 16 Aug 2023 18:11:57 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 18:11:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:11:58 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:12:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 18:12:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:12:11 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 18:12:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 18:12:14 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 18:12:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 18:12:14 GMT
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
	-	`sha256:b374d45030b6b986633ade41a535a4b01afe18c9fd2e0e410195d38514f95010`  
		Last Modified: Wed, 16 Aug 2023 15:45:35 GMT  
		Size: 153.8 MB (153798593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebb3995102b07bc04f0484e66c9d8c2bb56050df970aa4ca2fffc2b80bb90ff`  
		Last Modified: Wed, 16 Aug 2023 15:45:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f7cfc7ea2088b59b1917148caf409a46964acf2235419a8b9accbcb11b1f92`  
		Last Modified: Wed, 16 Aug 2023 15:45:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9e6024e23f87abb481fb4bf0136b535a36fa2aef0ff8e2ff91396163065063`  
		Last Modified: Wed, 16 Aug 2023 18:20:38 GMT  
		Size: 12.0 MB (11975716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dcba17d8c4a16a579f359410bf59e10cdb3398ac84d3e03b2d942169acdb1c`  
		Last Modified: Wed, 16 Aug 2023 18:20:38 GMT  
		Size: 4.4 MB (4399187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4f51f965914a6a163bab2815834ac5e99294b88a08aa3f0f686139394d0979`  
		Last Modified: Wed, 16 Aug 2023 18:20:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-lein-2.10.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be622a563177af01e214abfc3f8a293410c6a9e4079401c8b01a0107b96928a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215753978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775510a911983ac1360a6bc21e1730a8ee9c950b38017288a4dc8e847cc46502`
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
# Wed, 16 Aug 2023 14:25:18 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 16 Aug 2023 14:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b475bcc23db0bd618c815bb8f11d8e084dc58288ea3bcdf4e7f389ed41c89f56';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d91842e9c172967ac397076523249d05a82ead51b0006838f5f0315ad52222c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 14:25:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 14:25:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 14:25:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 14:25:31 GMT
CMD ["jshell"]
# Wed, 16 Aug 2023 17:28:28 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 17:28:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:28:28 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:28:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 17:28:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:28:39 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 17:28:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 17:28:42 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 17:28:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 17:28:42 GMT
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
	-	`sha256:06f75afb18f557e5c651981203c31143846350f9adeedccb07950c4ef5a98f29`  
		Last Modified: Wed, 16 Aug 2023 14:29:11 GMT  
		Size: 152.1 MB (152127056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b222e17fca4cd35d24d7fc6c3c538c6eaf4bee1dc764089b001f2151d51558`  
		Last Modified: Wed, 16 Aug 2023 14:29:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad875b1a22fedd9a22d6daad91b4bede79873b90122d8cc925a587247692904`  
		Last Modified: Wed, 16 Aug 2023 14:29:01 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e691818f16946a803e91d8cc2ba10059299f488d1b54d6531d325fff77f91e5e`  
		Last Modified: Wed, 16 Aug 2023 17:36:44 GMT  
		Size: 12.0 MB (11975779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6499be3218c03e17e27c99b752b1ba18e0ed2f55cac940b9378af286c2094eb3`  
		Last Modified: Wed, 16 Aug 2023 17:36:43 GMT  
		Size: 4.4 MB (4399207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb499f86a57b916ab4c3a21170cfc26d8f6eb4647e905a6128dbe44b3fdd80e`  
		Last Modified: Wed, 16 Aug 2023 17:36:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
