## `clojure:temurin-21-lein-alpine`

```console
$ docker pull clojure@sha256:2d2c2eb5acc6dcccfc853df3aff1fdbb4ed2770f72c733b73f553c13e96248d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-21-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ffdd12f0d7661430d7ce617b9556122195d6be0de2d24adaee5ed1059e954223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205410654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6942bccec0a03771a3884cebef18298d480ff77b67a96d6e39aec45255ae62e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74124278afe2b18a31c86c5481b70f13610d72f9251456efb60077c008ba80d9`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 20.6 MB (20646874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fcf39531b5efa8fb9a8f692b5b7b7feca498796d140b94c6255523f4c7f6d`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 157.8 MB (157779528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62fe376e35d90e3e99f049badca94e8fe7301d699d6a2539330a8994d9f8799`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5d46d44a8796aecf2575f05400a60dd8d65d4f9f801590d09cd3b4f278318d`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1604f4d683b26f19a619009739765d86fc0a0ee73a8cd2c0ad1c90a02b56add4`  
		Last Modified: Tue, 07 Jan 2025 04:23:01 GMT  
		Size: 18.9 MB (18853241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7218abd041bc0ae4796f763c6cd87b02c9cf4df6bf7b8575464a3feaf21be`  
		Last Modified: Tue, 07 Jan 2025 04:23:01 GMT  
		Size: 4.5 MB (4514170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05fe948d11d1390fe6d1610d06f623dc0c94ac0a06894875472db7c01464505`  
		Last Modified: Tue, 07 Jan 2025 04:23:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:c2003c53e5f6e76d480a2f54c861638a6fc1cc8f161f1963c3786c128db68f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f0feed7b8371bdb7a91b06d0b1a7809c104c04e5a5882aa3111fe98c60a232`

```dockerfile
```

-	Layers:
	-	`sha256:221be406d59c74ad4f77d930bb7fdc47907e73181cf7fa65d76cfed2dadaea42`  
		Size: 1.2 MB (1155049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923b6cd9c50772af4928f6a8378f145086fca77269dfeb9457f9e8903089f6f2`  
		Last Modified: Tue, 07 Jan 2025 04:23:01 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json
