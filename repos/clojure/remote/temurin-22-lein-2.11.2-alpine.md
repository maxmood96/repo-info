## `clojure:temurin-22-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:175eaa2d34ad4c12f249f66e08a0319c45bfcacb61c1475999035690b0563733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8dca870f747cf51c557291a3068774b4802bcddceeafd212dbb9189953b9e07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197512138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d306c230927053da5f91ef0d7eded0ef89857de66ce961b8f401e48d796cfa4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["/bin/sh"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='8ac93a2d5a55aabbc0f7156c2f9032026e87c185689d628ef8a4184b6e9ab006';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='49f73414824b1a7c268a611225fa4d7ce5e25600201e0f1cd59f94d1040b5264';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["jshell"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl git gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_ROOT=1
# Sat, 20 Jul 2024 21:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db286bb27ed845b0633219d49e3c9b81f2c8fe547e4c14a6d4e3e4b3333d774d`  
		Last Modified: Wed, 24 Jul 2024 01:29:38 GMT  
		Size: 156.7 MB (156688129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e7a0d670b44b1232c37aa9614181f139acc22c1ed85392a2094dff3ad6c18`  
		Last Modified: Wed, 24 Jul 2024 01:29:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d13279157e3b042d431a8a47a3e50c7e6667569de4add5c886b94e82ffff35`  
		Last Modified: Wed, 24 Jul 2024 01:29:26 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350a1faf1b32d7f2ef84b86932167011f10c313a027d0bd607f7df65ecab2ae3`  
		Last Modified: Wed, 24 Jul 2024 03:04:19 GMT  
		Size: 19.8 MB (19781731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f28d5d69e8e137514fad770a520d5d0069d5f837e39248d5d691bf8f5acc79`  
		Last Modified: Wed, 24 Jul 2024 03:04:19 GMT  
		Size: 4.4 MB (4398015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871c1f1045bb8f8b3e6111284dcbbc1899203c8847ea056ae96607b870d5c3fd`  
		Last Modified: Wed, 24 Jul 2024 03:04:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:8411306c54c0cbe6af780e6feb3917610f2553e047a1dbb841bc209b8fb941e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.6 KB (1000604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da5ec6c19a0e8d9a2603bba1d7e55d015928697c9b09d773c04f6dc2cdbe246`

```dockerfile
```

-	Layers:
	-	`sha256:c2b7384d53a19668f3270f3f27c6eca767823a96cf87f71ab6043c81db5fa374`  
		Last Modified: Wed, 24 Jul 2024 03:04:18 GMT  
		Size: 982.4 KB (982391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00d59d47dbdea0025a23a604a575869f98992f6f32bb6bf3ff6d1b8005edea6`  
		Last Modified: Wed, 24 Jul 2024 03:04:18 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.in-toto+json
