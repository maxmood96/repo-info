## `clojure:temurin-17-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:76a9b5bc247c9dc602f5f3f0038e65e481b6bdfc4115df229e86c98b3700b44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b55dbbc09d2e7d54c4b5b9dd7e882e679099a70c95a79023b59139ba4fd68ab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182284521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa85ae26872c4dc8e361bfa543d85d010f64cfecf9887b81e60d81a51072c528`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='839326b5b4b3e4ac2edc3b685c8ab550f9b6d267eddf966323c801cb21e3e018';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Wed, 24 Apr 2024 21:23:59 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:24:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:24:00 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:24:08 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Wed, 24 Apr 2024 21:24:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:24:08 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:24:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:24:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:24:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fd38fd7cf5b8d60c92e1aa46a24527229fb51b451491d35a7028a8a1d0aba4`  
		Last Modified: Thu, 28 Mar 2024 02:08:23 GMT  
		Size: 13.1 MB (13142803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08b7b3a74c4535b6568ccd03b6b5fb1de2dbd6cb55f506618b3471acf06b528`  
		Last Modified: Wed, 24 Apr 2024 19:13:06 GMT  
		Size: 144.3 MB (144331997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71edf4fdf61d7c4bcebfbe05d76931947068e88ea252a9ccab7c03b3b131f074`  
		Last Modified: Wed, 24 Apr 2024 19:12:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f852f18c8554898c2508d8273094bbe0d0a6d5fc3175658c756845270a1f5cca`  
		Last Modified: Wed, 24 Apr 2024 19:12:55 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069c1eaa6235d9d440f698c523128a0f6eba532bc1708405f59ad8c85d3d8021`  
		Last Modified: Wed, 24 Apr 2024 21:47:40 GMT  
		Size: 17.0 MB (17000492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533993458d033b7c833b23a6956e771034e9dac994eafe22b38f1d5e45795f0`  
		Last Modified: Wed, 24 Apr 2024 21:47:39 GMT  
		Size: 4.4 MB (4399185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664833089b19d199e83c2a1eb7a2790314272941b40e0e1d20b4be24d7399f35`  
		Last Modified: Wed, 24 Apr 2024 21:47:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
