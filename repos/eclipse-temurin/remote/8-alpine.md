## `eclipse-temurin:8-alpine`

```console
$ docker pull eclipse-temurin@sha256:0a67288aa987bc8bf6eafcd7f3eb0b7684e458b4587dd459523830854acd4ff5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9df8f8cc4993c8dd7476aa721e9588a1d60a59b6bd833ca749b7954ee81f1150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73742919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20469d705717f6f36638874d5b407584929ad087008e89be524f3195fd2b5394`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:23 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:23 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 22 Jun 2026 19:56:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33155d10cbc71fdb14f9df0a7aab9f4991457ef842a4b3faba9384696971d92b`  
		Last Modified: Mon, 22 Jun 2026 19:56:39 GMT  
		Size: 16.8 MB (16815722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66e7959afd4ff0c5fb87161fdc42c3d1c570e4b61756803b867c0ddf2df27c0`  
		Last Modified: Mon, 22 Jun 2026 19:56:40 GMT  
		Size: 53.1 MB (53080163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c11fcafb6f48be9be1990f57b024b04d05423281859902ca4e7398354bf49e1`  
		Last Modified: Mon, 22 Jun 2026 19:56:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e222a224728f8fb8cdacc2640e57bac24376e1b11d15cd7cbc27b02bb0ed8642`  
		Last Modified: Mon, 22 Jun 2026 19:56:38 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5255e8a266f71d633216c6ddbbc53b5cee2a4f06314db0d41ae1fc8322521599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43ae4b74cef24c914453d8af2a38a99e3e3e69f019198927ad7b453a28c1d33`

```dockerfile
```

-	Layers:
	-	`sha256:6baebbec243a4280a1c8edef206ca94536ede9c144563f8aef322e51caba3244`  
		Last Modified: Mon, 22 Jun 2026 19:56:38 GMT  
		Size: 1.1 MB (1090751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61711079d65abb55cb9ba786741b94f4a240d60c389cd590ee04536a27088351`  
		Last Modified: Mon, 22 Jun 2026 19:56:38 GMT  
		Size: 19.7 KB (19702 bytes)  
		MIME: application/vnd.in-toto+json
