## `clojure:temurin-11-alpine`

```console
$ docker pull clojure@sha256:e8ee1e1183f1c0b7825118b0c734f3a6a9647973aa8c5b78a0665dc049ae26ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:16e24ffc9b620790fc8b2d2017eab04c684ae3b68f272c26bea3c71f92a52569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187718954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2306d3f95404c3ddb9ff70e6ca9225695ffb0f885f55b9b4b6e923bca753fe4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0a431310ccccc36c85b1274b5d31e368fdc8cf62cb7c2ed98d7b59eb5a13dc82';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46235840cbe78a3ac40b06a4f84f57050b2b7b77a065d52d16d38717f629dd04`  
		Last Modified: Thu, 24 Oct 2024 00:56:41 GMT  
		Size: 18.3 MB (18307392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5eef817826778f540f993b0b73b2a1047666c2353b90e622355ec6f9197cb5`  
		Last Modified: Thu, 24 Oct 2024 00:56:43 GMT  
		Size: 140.8 MB (140775084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee12e3f6143eb1a07bc395f2146936226541f8bdbcfa988d88ffb58318094f`  
		Last Modified: Thu, 24 Oct 2024 00:56:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da054bf2d4eb45bce39bf892bcda0761ccf0484dee760944d2eb0ab3b7bd6966`  
		Last Modified: Thu, 24 Oct 2024 00:56:41 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865d90022d31b1688273ebdea17806e311abc54f0d1ba3b0836846247553abcf`  
		Last Modified: Thu, 24 Oct 2024 01:59:13 GMT  
		Size: 25.0 MB (25009607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ad88ef0f82f5f849ebdd1c43dab2410234eec1bd89c730dd0ab564a77e0b7`  
		Last Modified: Thu, 24 Oct 2024 01:59:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:10889ed610ccef1689e6a07c1deb9b3a23f6d0969bb1bef92819d2b9fca0fca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18cec6248632c6f0e7cdd6eb54c6b36506609e8405f6c7b71b5e1d2e7f6302b`

```dockerfile
```

-	Layers:
	-	`sha256:40f10773289091cb5e1ec1a766447dc1299a62b5409419c5ec24cb865960b6a6`  
		Last Modified: Thu, 24 Oct 2024 01:59:12 GMT  
		Size: 1.1 MB (1144028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81ffae06ec53dce623e8d5af1eacde4af444fc03b7fa6c0cdb10653e185d5de`  
		Last Modified: Thu, 24 Oct 2024 01:59:12 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
