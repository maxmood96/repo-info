## `clojure:temurin-17-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:52aa8177b97cf215822577bd60f8a1a7ae81b7fb5e7742b46f921c71236936f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:0835998b8b759536c11a0b292bed79e3ec5690dbf2f14eee703147b3e9f127f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186246018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6fadec9308a69ff1d4e457643e17db4ca69ba12a7056a8d8fd363ebdfed649`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e384a19a9b0cde9f53fc5c79a581f80b1606cb9b0c477b8019b1716ffe026fe`  
		Last Modified: Thu, 25 Jul 2024 17:29:36 GMT  
		Size: 144.4 MB (144394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed71e81fa34c6c2e7902182aaf9da971d499b0e58d2dfcc2c789535bc6768e0`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb93379603195c1cd0e0fa2dfd4b31ab5a9580ed4dd4cc301f4ca12c31c1ff`  
		Last Modified: Fri, 23 Aug 2024 19:26:45 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb20d7cd9acd80b917c457b0dbf81cf84e824dcf75a33fd01afae24d30fc1cb`  
		Last Modified: Fri, 23 Aug 2024 20:01:50 GMT  
		Size: 19.8 MB (19788733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eeac8f49f127e7e792daeb549f739f7cd7bc8de1d2681ae7a2ab73def66269`  
		Last Modified: Fri, 23 Aug 2024 20:01:49 GMT  
		Size: 4.4 MB (4398002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa91f046d6bcd8e8c69c356c3a87926cf4dc5a2101173f93ed11cdcba96297e1`  
		Last Modified: Fri, 23 Aug 2024 20:01:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:8709a437ddf529b407f54686fe7b09b40a53bf4305bf5ae96e5b405ffe66da5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1018530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c81d6b923ff7c50fb2ea2d8bec34bc858db2bdd1c3cf5b88d2ba1a65bef941`

```dockerfile
```

-	Layers:
	-	`sha256:f2c76342fce50614fb6c2c4d24be4b91e7ca5cbbd1e0a52df4af6dd7358e2bb3`  
		Last Modified: Fri, 23 Aug 2024 20:01:49 GMT  
		Size: 1000.3 KB (1000315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf378e65b0319612b1cfba536c426b43f1d48753533f73ca4fe28dd343567846`  
		Last Modified: Fri, 23 Aug 2024 20:01:49 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.in-toto+json
