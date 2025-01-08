## `clojure:temurin-8-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:8793b12ad014a5b08966d689ddf9c3b3aeaf7076cec87293e44a0dcd95946b2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8998fd580cce38eb3f1986ec82ec3fbf913a2f5db4f14c6b70267bf6ef46c4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144917782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dac1b3a1c911ef2ceb202cb47ad7fb29b7cdd93892e0a2bd8f36ddafb39e0c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6dfd5a5e2f33448ac26d2a57c3f54ae2ccdf4daf44580748feb134ca9d018`  
		Last Modified: Tue, 07 Jan 2025 03:31:21 GMT  
		Size: 16.0 MB (16005492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89412a9591e0dd26815b7ea9db5a452352dd76998189f07abb56d784b1e1b1a5`  
		Last Modified: Tue, 07 Jan 2025 03:31:23 GMT  
		Size: 101.5 MB (101542475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4233d01232ab4d34c864cd6b3c052e216dd74eb06d21e79ce4dda95a8fe2cfd`  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f230d3f854701990cfaac714a5e83e61caeca6cc0efdab1d522bf78d0954d7e`  
		Last Modified: Tue, 07 Jan 2025 03:31:20 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718a4d7c6d762be187789c914445b4bc604e3fe660832b19475a8c7b417d2bf`  
		Last Modified: Tue, 07 Jan 2025 04:22:55 GMT  
		Size: 19.2 MB (19239227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8fec1239a1cb26da005e374dccba000d392d42d6ed9123c2d671461bfca1ae`  
		Last Modified: Tue, 07 Jan 2025 04:22:55 GMT  
		Size: 4.5 MB (4514126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:df2f309d8b1ac5d8e302202858e836f1ec3c14156f93b546a560fc2d8c2485ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c2f5824b94242436c13a4c93f40e95478c8ff9ab0e811eb7d633d88dc9206b`

```dockerfile
```

-	Layers:
	-	`sha256:068e5460ffc9fb219a30482f5a1ed1b4154ca036adbb6c54f63836793d6637e9`  
		Last Modified: Tue, 07 Jan 2025 04:22:54 GMT  
		Size: 1.2 MB (1179951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5151b05aeaed2226e3d630d4294254220058d850c97ca9539ac372e1177744`  
		Last Modified: Tue, 07 Jan 2025 04:22:54 GMT  
		Size: 15.8 KB (15791 bytes)  
		MIME: application/vnd.in-toto+json
