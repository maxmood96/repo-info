## `clojure:temurin-23-lein-alpine`

```console
$ docker pull clojure@sha256:c635f8b04499c61dad8aaea89b5e946996014bcc622a4b84a6992b71bf088f2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:03c406f10b8c3619b5c95ef9578cfde0fa71cb6e5b4537e187894fc0d77cb892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207453070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0374dc8901cfccdf0a5e1fd14d014dbe837a5449ad0695eb629d77094173483f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515fe7a20d9848ae77a0dd2fe590ca44111e3a72a0696fa6b73e346b3514a4f`  
		Last Modified: Wed, 18 Sep 2024 21:24:27 GMT  
		Size: 165.5 MB (165476640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4108fead0afd7aed117dbfb1ae2a0bba1a6d4427cc8292f8fbc79e9bbcf4280`  
		Last Modified: Wed, 18 Sep 2024 21:24:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6363deaddf9a060529cefe0fdd8773e4a9daa37eff2e63cfdc5ccefed75bd5ff`  
		Last Modified: Wed, 18 Sep 2024 21:24:14 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00fb249cac43d96d8655e6b21ee403b5710f9db5a1a65014d4b06661cd4b1ed`  
		Last Modified: Thu, 03 Oct 2024 19:00:13 GMT  
		Size: 19.8 MB (19803171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dcee833d6ee2c9ae802536c28b46e84a36f0326109ddf0dbb0226a02c41fb9`  
		Last Modified: Thu, 03 Oct 2024 19:00:13 GMT  
		Size: 4.5 MB (4514123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688df8047695a1cbfb8884b95a8fb9af814c361fee604c2fe7bbe19bdcdeb5`  
		Last Modified: Thu, 03 Oct 2024 19:00:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:622c1cd124b4e45d5f80eb41997c26da2600ceb723177a58c2219ffc72eb41bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5d371517c2e248b80de99567a4862290a8a90a25b19a642eb505ce745195c0`

```dockerfile
```

-	Layers:
	-	`sha256:f514f058f4c0be7da0edcb79faaa53bf882ec9f22fd18b32e7edc485a9f08134`  
		Last Modified: Thu, 03 Oct 2024 19:00:13 GMT  
		Size: 1.2 MB (1154849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c0479b5cb171928752036ca97672b35d3aa4e988197682bfffa094750d1c82`  
		Last Modified: Thu, 03 Oct 2024 19:00:13 GMT  
		Size: 18.2 KB (18211 bytes)  
		MIME: application/vnd.in-toto+json
