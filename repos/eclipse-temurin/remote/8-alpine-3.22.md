## `eclipse-temurin:8-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:7a2f257ab9331bc5f0cc38b5544e762116236528a1c79e6c3f552a1745b8c41a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dc5649620f63038cf3c75a6e0722d5569bac75340fdb8f26ed363de61cf1eaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73184765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd553ccd916be6bb936070f9577f4ee7639e5f4cc0ef31a30aa3524756af7776`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:23:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:23:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:23:42 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:23:42 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f59c604b500830a2abe2f4e6464b6c7608c6e19703462e42682184fd6b22dfc`  
		Last Modified: Fri, 17 Apr 2026 00:23:57 GMT  
		Size: 16.3 MB (16316946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b811b2f3a8af8b0add6e57e783ffbb14fdbcb32fd875c1fc849681ae4e3fa82`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 53.1 MB (53057197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cba20360fc480e5ee5f820203fd745a471990829f9a39ff954e7492b7ae2f7b`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2f4b1418d15b4d32415478b6b59b6a0858ddf1b828f67c3b189efd3ca1bfa`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:951497dcc658b1854eb76a6184ae513d616c49557cd68f148b35d1a46e9e3a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1121019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee824b1bfd9238620282cb892543ee6a527fcd34242b5b6d11b52527a7f528a`

```dockerfile
```

-	Layers:
	-	`sha256:39fe6e16f83e6b8e11801fc037cbf336050acfa88c42560620caceff6dcb460d`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 1.1 MB (1102308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f07e2caae75e142c8e3ad094fc993309c8bdf0ad19480555494da7fcabcb2`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
