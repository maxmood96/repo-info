## `clojure:temurin-11-lein-2.12.0-alpine`

```console
$ docker pull clojure@sha256:7c43acf344853ac882b7115395acaeca39d5b6383fd1ebcea73d2d115c72cdfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4a349c1bb20aad84a9d04051e2434bc36408b8ea8346613b498d128f4c9b48f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181054902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6785af13f92a5689e29553e81a9329ff61a0afe7f40909f04e4cec757bae48`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:32:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:56 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:01:52 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:01:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:01:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:59 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 15 Apr 2026 22:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:01:59 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec914d871e26d0465399fedbb12a944add78359e4bacb45111654e407011389`  
		Last Modified: Wed, 15 Apr 2026 20:33:10 GMT  
		Size: 16.8 MB (16837789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0f2de0712b22eb820b820ec9d10381f0162a40034dd9db90063cf9bc5b7f9`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 140.9 MB (140916718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836bb5bbf19dc634eaea3ff5cfbc9b0ca22932b1bbb49c9a806a0bb040b842`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470514f36b76e7d4fbd25626009aade331446b35fde7acb2f42ae8b0b5c53a1`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef5a3060d44ae05453f75c02599ad2002f0033c42691d052d95717aeb4856a`  
		Last Modified: Wed, 15 Apr 2026 22:02:10 GMT  
		Size: 14.9 MB (14916075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b6aa3def49dded927151de3268ebdcca14bab1c525258e345a5eef98f866de`  
		Last Modified: Wed, 15 Apr 2026 22:02:10 GMT  
		Size: 4.5 MB (4517693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:70ebd6e47e09e7c34ee16f0406307f7c2cc313520ed04aa7e41a0a1c94508782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.4 KB (976380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a139c2d8afc1ea58d9bac65b3e619af8a11c58d0ed3d4e72551d1aa5a805f`

```dockerfile
```

-	Layers:
	-	`sha256:88260c70ce3bb7e4553d83d848d1107d644e8d9267e45cfaf7ba6f31dcd184ef`  
		Last Modified: Wed, 15 Apr 2026 22:02:10 GMT  
		Size: 960.6 KB (960631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4a606286a5883bb901c2cd02126ccba191dbcc15fb4ee3f8f16f84b832f002`  
		Last Modified: Wed, 15 Apr 2026 22:02:09 GMT  
		Size: 15.7 KB (15749 bytes)  
		MIME: application/vnd.in-toto+json
