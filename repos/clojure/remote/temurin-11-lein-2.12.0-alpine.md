## `clojure:temurin-11-lein-2.12.0-alpine`

```console
$ docker pull clojure@sha256:61fff25d0fabc19520f19d347af656d4047dc24d45ae56eb212e8f3cdbf964e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c8e878fafec79b7d90794a8dc85024e1b74b9bfd584dcdf8b96f792c61ccc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181212715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28f9c7b8772abeab93ab7fdb36f20885fcab370da7e6d58237a4624c46c60ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:17 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:14:04 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:04 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:10 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 29 Apr 2026 23:14:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:10 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c175c39880efd27b1b0b6f4b68db4424c3664c1899709c2068bc4301855817b`  
		Last Modified: Wed, 29 Apr 2026 22:44:33 GMT  
		Size: 16.8 MB (16837661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b06a78b6e346324b4ccae7f54064e05cc8059b37b593caf9730186b81c6cd`  
		Last Modified: Wed, 29 Apr 2026 22:44:36 GMT  
		Size: 141.1 MB (141074590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27e99b60546186d5398cb848761881034ad4a2495edd58778348608ab13b34`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5cbe1f675378862d1c920e9f972f54caa6e00e0ef8bf232fd844c01fa839ac`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e8f76123a3ead835d9bbff3e56383153da7473ad8e31db5a803f5b153c3c7b`  
		Last Modified: Wed, 29 Apr 2026 23:14:20 GMT  
		Size: 14.9 MB (14916142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885eda0d87a49cba65673b819e416e29dd8c76d29405eeea5c163f8693f50cc`  
		Last Modified: Wed, 29 Apr 2026 23:14:20 GMT  
		Size: 4.5 MB (4517692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:d09e86e36678decd6045b12986b03ce9e061007e9989a3485d7bb73d2d57e80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.4 KB (976384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dda4c88c4f99c66f60199ee753fb300f5b0c38addcb42132bbe263536acd3d`

```dockerfile
```

-	Layers:
	-	`sha256:f16e84d77d6fd90acb2e617f1c910ec08812166991feacb750bb2808a4896812`  
		Last Modified: Wed, 29 Apr 2026 23:14:20 GMT  
		Size: 960.6 KB (960633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fee04ba0e918c4f26beb588de8b33027875e46e72fad2b2599993ab452110c`  
		Last Modified: Wed, 29 Apr 2026 23:14:20 GMT  
		Size: 15.8 KB (15751 bytes)  
		MIME: application/vnd.in-toto+json
