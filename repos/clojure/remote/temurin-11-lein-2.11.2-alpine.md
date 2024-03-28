## `clojure:temurin-11-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:bcf4ef81d307c987e82cd8698976408ab806e8f905d46bc0ace84db48d449769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d28ef1c5b13cd645e356bd7d9cde8191c6140383315d8378cfdb07958815bbba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171638912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c4ce1e4c14c8a1b05ab65b2d8372aa6d63483db96f33274e2ec92d937b07d5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:01:21 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:01:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:01:21 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:01:29 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 28 Mar 2024 03:01:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:01:29 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:01:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:01:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e821e71d8d63599c03e25acaa57493f1c151dca7cdea91999cc8883003352b`  
		Last Modified: Thu, 28 Mar 2024 02:05:38 GMT  
		Size: 140.5 MB (140489305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609bda70c76d2028175d3b7ef78a71175a915bbeedfd01351b9da4c5e9b04183`  
		Last Modified: Thu, 28 Mar 2024 02:05:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186466e209e780b86f3ff83c6bd480c04712356ea99074c42ddc0db13b43fffc`  
		Last Modified: Thu, 28 Mar 2024 02:05:27 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a51d8d7b076012d810117daedcead7f3bd101b50ff0d9eca01dbeb8b018a11`  
		Last Modified: Thu, 28 Mar 2024 03:20:54 GMT  
		Size: 14.8 MB (14803381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825424cbb9ae4a609d3bc3038c015c23e7d3808b8980f0d545cb8cd2edc10ba7`  
		Last Modified: Thu, 28 Mar 2024 03:20:53 GMT  
		Size: 4.4 MB (4399189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
