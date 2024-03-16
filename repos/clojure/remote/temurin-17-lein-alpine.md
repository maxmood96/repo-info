## `clojure:temurin-17-lein-alpine`

```console
$ docker pull clojure@sha256:0480caaccbbdb7be2e802d327413734f340f16e5853db3b8b0dfb00218373c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:483be08819442bc632f979a4295da2ba681c6b0a55e26cd73a97146a199a78b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179896129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d39517b66e1c351764102a6d7fc135c9c84f886826d9638cac8840be7c32c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Mar 2024 03:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 03:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Mar 2024 03:24:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:24:03 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Sat, 16 Mar 2024 03:24:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ce4085548f73ec97fa870de3f7da87634b4cbbf9753600365e2e0b255585e7e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:24:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:24:14 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:24:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Mar 2024 03:24:15 GMT
CMD ["jshell"]
# Sat, 16 Mar 2024 12:03:10 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 16 Mar 2024 12:03:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 16 Mar 2024 12:03:10 GMT
WORKDIR /tmp
# Sat, 16 Mar 2024 12:03:18 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Sat, 16 Mar 2024 12:03:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Mar 2024 12:03:18 GMT
ENV LEIN_ROOT=1
# Sat, 16 Mar 2024 12:03:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 16 Mar 2024 12:03:20 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Sat, 16 Mar 2024 12:03:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Mar 2024 12:03:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6fa00702eb0aa7934afc50cb28145402935b385451bcb6ae891ecc0d4a9b90`  
		Last Modified: Sat, 16 Mar 2024 03:27:45 GMT  
		Size: 13.1 MB (13136633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc145c2c40b090019607ad8d5618e1026c57507c6622d156be1870fa790a7339`  
		Last Modified: Sat, 16 Mar 2024 03:27:56 GMT  
		Size: 144.1 MB (144142428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65413771e18cd2c82e4675596f5160e42af611ff7d9eabbe7621c2d626bd9b6b`  
		Last Modified: Sat, 16 Mar 2024 03:27:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f39855dd57cb06f224fd5f6e6327f6551e336425c751b77c2f53f11ba7ce94`  
		Last Modified: Sat, 16 Mar 2024 03:27:43 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11c32fb174f338e9523460657a1c173144221bfe5eaa5be171de22d75574237`  
		Last Modified: Sat, 16 Mar 2024 12:07:40 GMT  
		Size: 14.8 MB (14807859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccf588cb80188dea667173a8c6cdb4ba3abe2217873686f9719b5d071d4e58e`  
		Last Modified: Sat, 16 Mar 2024 12:07:40 GMT  
		Size: 4.4 MB (4399177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aedd9ada57c7058058269a06d7d8da5a265ba54413f4d66c4d023b80957164`  
		Last Modified: Sat, 16 Mar 2024 12:07:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
