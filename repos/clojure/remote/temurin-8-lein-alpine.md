## `clojure:temurin-8-lein-alpine`

```console
$ docker pull clojure@sha256:70ed25480faea72ef434ea05ae97f2517af462b077bc8ff68c400cf56acc1a41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:511e7fb7f44442547896df682f51085db22b24e35173ca04639965dfb157c7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139142183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe43bdf99bef24130fe17517dabfa5c0fdecc7d615e48a1c3a351360c8ac557`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='525a7731331cad502b9293ccb4ac2b13e85516736e98a57cb27c2767005188e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff7dc6fc2858af0a16833a15a63741d58d895a9d1a9a2de411e9921a0de0dd`  
		Last Modified: Thu, 25 Jul 2024 17:25:18 GMT  
		Size: 9.4 MB (9394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5b4e8863d905ec4a9cf899ab58456bbf5e69c77c880195237b730f54b1ec3`  
		Last Modified: Thu, 25 Jul 2024 17:25:28 GMT  
		Size: 101.6 MB (101550154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fb9bd12016294f8b7643104b6af5b98398ca45d4f000a0492f82f5b017db9`  
		Last Modified: Thu, 25 Jul 2024 17:25:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b196e5c22826b2e8a8b0eea7dc9ff9697a5aba3c119d627499ba7285ec46698d`  
		Last Modified: Fri, 23 Aug 2024 19:24:23 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06d56816b520e9fed5576768677830d222a3b99f623889c0c8f60d7ebb3c7af`  
		Last Modified: Fri, 23 Aug 2024 20:01:37 GMT  
		Size: 20.2 MB (20173899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2f2a1a569c866712c4e4ee9253ed054427d1290e89eae7726919f20776b32`  
		Last Modified: Fri, 23 Aug 2024 20:01:37 GMT  
		Size: 4.4 MB (4398047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:aab14aeb30f180c449c326eca9e0be822fc09455a570b6b4ccf2bd1b63946274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.8 KB (946819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4811974addd7424f708f1daad1d3f006fe47be219b8be11a9e191e89e9077a6`

```dockerfile
```

-	Layers:
	-	`sha256:f085b0c7443a99e21b9a9ef489b7d967b0d915da899d169c09802c3db67b77fb`  
		Last Modified: Fri, 23 Aug 2024 20:01:37 GMT  
		Size: 931.1 KB (931118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa9022ac04e36b2e7482f88dea3fb66c3ee71113e7c2853e27418f00fc1bbe3`  
		Last Modified: Fri, 23 Aug 2024 20:01:37 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json
