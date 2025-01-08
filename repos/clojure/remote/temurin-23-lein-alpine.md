## `clojure:temurin-23-lein-alpine`

```console
$ docker pull clojure@sha256:c9ae9f70831eb37f8daeb18d6c065fafd503bb93d351992cc45b8371a450a227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:5406537b9db614da95a1cc4066d0da7ca711e7d1b1fe259237cc20dce86d03c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213144343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa16dc7c17e5843bc2087f3e41504c38c468b816e247354b68dac4be880896c`
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:225cb0f2398c82803e0a664bca2838b6952c8625269bacb10309a51d08b246a7`  
		Last Modified: Wed, 08 Jan 2025 04:32:08 GMT  
		Size: 20.6 MB (20646818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372a9834e30bc1a4ac9cf9ed49635b1495df06f03aec898ef29d50dabefc1db`  
		Last Modified: Tue, 07 Jan 2025 03:31:58 GMT  
		Size: 165.5 MB (165513260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9c3a812f9de067e26e45678b86e96db89e7f0dae9089fbdc3c188e4238f4f1`  
		Last Modified: Tue, 07 Jan 2025 03:31:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9ff0efbdd4303d78867776fe04d39637d68c10fe145cb24df20fc8b1f2478`  
		Last Modified: Tue, 07 Jan 2025 03:31:55 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6633bb401dca529470fa5cbdc45d313dad23087f9c1bc45479f6c5c9989ce`  
		Last Modified: Tue, 07 Jan 2025 04:23:06 GMT  
		Size: 18.9 MB (18853263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58868b77cfdf328a86e418b6bea0c1486440ea591450bf83f26b19cafc01b435`  
		Last Modified: Tue, 07 Jan 2025 04:23:05 GMT  
		Size: 4.5 MB (4514160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5a8c469f8a8404c1b1529c01f787f59154a328d769eeb023793c597636759`  
		Last Modified: Tue, 07 Jan 2025 04:23:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:d1b3d1a13e8a10cba73c57b1cc0918ed0058ddb0ba0b13f18c9611ea917a7c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1175220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9292a2466b9ee36e57f61dfbe17dc459608e14f8089781102d3c489f6e8411f3`

```dockerfile
```

-	Layers:
	-	`sha256:526683fb326554aced9adda6f08f240c49c02593851a02838665f69e4dbf2f19`  
		Size: 1.2 MB (1156952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e9ffad2a99956673d426e26c4e6a1ff2acc59b5b2321a5aea1094f96741560`  
		Last Modified: Tue, 07 Jan 2025 04:23:05 GMT  
		Size: 18.3 KB (18268 bytes)  
		MIME: application/vnd.in-toto+json
