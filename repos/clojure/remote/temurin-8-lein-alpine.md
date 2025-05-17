## `clojure:temurin-8-lein-alpine`

```console
$ docker pull clojure@sha256:f0617bfd05a3724e6933ca3c0cee63caf9306eac5e8ebb695f675ea7f1065f4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:874a611f51ef831ca3fbb8d856394bb13f5ab8cadc9f70654969dd38c112974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5857088cae8e360bce0dd3e7b22ec1de799079ef46679580d0e0ab6792c6b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='be8abae7586c328ceb3252aefed9e51c29be91616968c0130b41e7e57c846f0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7141be485741d41116a845b669643de63ccceb87c3be707c0a7eaa7f5ccf8f0`  
		Last Modified: Thu, 08 May 2025 17:18:28 GMT  
		Size: 16.2 MB (16176532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22b184abfb23338db1ce2eec5f2b1c5299eec68ec533ba9f0c96eb50f94d86`  
		Last Modified: Thu, 08 May 2025 17:18:35 GMT  
		Size: 52.6 MB (52621858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3726fa4c4e4f7f6fac67f7e4a3b9f88a7697235d9144aea259a488250ea6a4`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267111b8758c00ce54358fe646f25d46e043fc0ee6173035ede38ede1c1aaddb`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920cc4ecb79812edd5b8aa00525e13768da1fb56059f770ebe4a4cc137eb487a`  
		Last Modified: Sat, 17 May 2025 16:09:56 GMT  
		Size: 19.4 MB (19368985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c8c27ecf366729ea642ea4aa468e0cf6fd0664cdac60159ab169fb1b58f08`  
		Last Modified: Sat, 17 May 2025 16:09:57 GMT  
		Size: 4.5 MB (4514132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:59e59feeabfe606ef5101be8592c4281c797b0b5ab3d99c44e39c3fa5009d161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1106766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb85ec4ff4f9159b842883668f94a9afe048fc3c5052668e63d1ba9f2b10aa04`

```dockerfile
```

-	Layers:
	-	`sha256:2a88dcbaeecd4edf70bbc9f03c75bb17f2274de465d69f0b99c21cf8470587fb`  
		Last Modified: Mon, 28 Apr 2025 20:50:39 GMT  
		Size: 1.1 MB (1090979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef1b8906696ece1d00523fb3a33997dee3b1c6212ce627260b8b1b8dd8e27ec`  
		Last Modified: Mon, 28 Apr 2025 20:50:39 GMT  
		Size: 15.8 KB (15787 bytes)  
		MIME: application/vnd.in-toto+json
