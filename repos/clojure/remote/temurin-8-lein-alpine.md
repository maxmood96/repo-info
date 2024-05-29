## `clojure:temurin-8-lein-alpine`

```console
$ docker pull clojure@sha256:6502db1770248f55787cc37305f99eb650819e4462237cb430515ca0ce778507
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6ca9f2b21f4728a01cac1b2f15ffd219c2b8be01d462e649cafc1a642fd490c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134867075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a0ca8e9e0f089fcc7354d9f5fb60208af243dea07203ad51e0585ca7a10064`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='409091665e5f8cf678938bbbc0d377122ef8bad7b1c97a0f809da054db956e51';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c1055a2ad6292da34c7007392014a7a5a8939d32d297c43fa65f0faaec5bb`  
		Last Modified: Wed, 24 Apr 2024 19:06:44 GMT  
		Size: 101.5 MB (101520753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a846daf1a23fd92d6d59d3dba57bda463e910cd200bb9914603682a117fd8`  
		Last Modified: Wed, 24 Apr 2024 19:06:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3546951364d504cdce98ebf79d8e5f55edd67fe2ac6b83e4c6e13afbfed84ba0`  
		Last Modified: Wed, 24 Apr 2024 19:06:36 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29543327e316687d1148d7636aab31a3fc0fa2055150ab2bc55fa3f8f9b23829`  
		Last Modified: Wed, 29 May 2024 19:56:28 GMT  
		Size: 17.0 MB (17001263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253a4836c1b8bbc58bfe39c2e11de26935d4c522b88a09b5cd010e7aaacdb515`  
		Last Modified: Wed, 29 May 2024 19:56:29 GMT  
		Size: 4.4 MB (4398007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:5e1fdd151ac2eef2bccdc8f7941955e39272ca86b948628551ab160000d16471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c637b8299a9c115452a4bde757bc24a37444338aea0f40507f8896fb793308`

```dockerfile
```

-	Layers:
	-	`sha256:cd89cee417e06f8df7aff2e8da935713ee87cc2a9d02ffcaf3bfa832d6ebc2ea`  
		Last Modified: Wed, 29 May 2024 19:56:28 GMT  
		Size: 1.1 MB (1115081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4866dee42e116cbe833a91a8168b10c17bd881f33d309bbe1095eb642f40b49`  
		Last Modified: Wed, 29 May 2024 19:56:28 GMT  
		Size: 15.6 KB (15639 bytes)  
		MIME: application/vnd.in-toto+json
