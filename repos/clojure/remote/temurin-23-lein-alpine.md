## `clojure:temurin-23-lein-alpine`

```console
$ docker pull clojure@sha256:d6d26e04b25a98a9d5e9870e3d0b1bffa3550cd83a5ab799a1ec0f271aa8776d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:712fdf81c929c99ed4494bf7ad36cd8aca46ed07243136f9c2a32c5f4ca6d152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213640076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a506a8134c6f14e226abce5f96972b26bf6952e9814c479289f79c60c2afc126`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["jshell"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229c05d87edca42fb39c5ffcb5e0bedea7fa96b9bad361c3f485d50d3924db86`  
		Last Modified: Fri, 14 Feb 2025 20:34:08 GMT  
		Size: 20.9 MB (20949783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b130aedac2651a9435f8d0805a2d5087c15a9d5fad2bd2530fe060ed83a2e3`  
		Last Modified: Fri, 14 Feb 2025 20:34:16 GMT  
		Size: 165.5 MB (165542654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074c3edf5c3e5f9ddaaa783c5b33ec8f9287af1909346c4f90103a9579dffd4`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c67efadec52153c3e21caad3dc817dc99704b643bec8d9324830842d5d29b6`  
		Last Modified: Fri, 14 Feb 2025 20:34:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b7018fbd3995c4c28883ae21bcf6773a293b68a6793a3a29d3212cdb9abba7`  
		Last Modified: Fri, 14 Feb 2025 20:39:28 GMT  
		Size: 19.0 MB (18988435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aea661d7c36b8b544ff8face431e6cc812b0486c6f4af56156b0bab9b1989f`  
		Last Modified: Fri, 14 Feb 2025 20:39:27 GMT  
		Size: 4.5 MB (4514109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825fe6c05f3fa1f2eb03be2ea9371dee8fee99378357b793ea6be058b31ab6d`  
		Last Modified: Fri, 14 Feb 2025 20:39:27 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:140d147be9ccbe416efad21442bfec1e9201f363c82c5e17fe9247bd8393e8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9d007a47de708896641b5cb65eefc55bb97e35ab70841bb5ed8221870534c4`

```dockerfile
```

-	Layers:
	-	`sha256:1ac8df0e1d53852bf42d7f5639b999a91c6e20366f8571f87cd935bf45b1403b`  
		Last Modified: Sat, 15 Feb 2025 01:35:46 GMT  
		Size: 1.1 MB (1092368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2192cd3c829ea58e988129d3879c4354e22425d6bb0b1eb51f983fa8107c8ea1`  
		Last Modified: Sat, 15 Feb 2025 01:35:46 GMT  
		Size: 18.3 KB (18266 bytes)  
		MIME: application/vnd.in-toto+json
