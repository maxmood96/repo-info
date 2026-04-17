## `eclipse-temurin:8-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:8cd598ec8c17f76c787f3c9afe2c9d7dfbe40c7040bca9505d0bc35c39ee9e6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c961719266e3efcbaf1e3cc9503eecef310caa8ad10e0ba0de4cc8b515b5c624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72905292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e71d13fccc544b10f65cd6c9c93a3ec96a6e44d6cafc4561c842d6b4f7d023`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:23:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:23:43 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:23:43 GMT
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
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0d2ff061bb98df790902928057c9e18fabb4491b0f31aa4ef2a418d634e544`  
		Last Modified: Fri, 17 Apr 2026 00:23:57 GMT  
		Size: 16.2 MB (16198788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b811b2f3a8af8b0add6e57e783ffbb14fdbcb32fd875c1fc849681ae4e3fa82`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 53.1 MB (53057197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cba20360fc480e5ee5f820203fd745a471990829f9a39ff954e7492b7ae2f7b`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5389d00520a4dc65ca06454e6ab52613c543e42239683a063618119840b342`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c2bac2c525722d88c5db6421b8d3b5cdc7b30e81f72f729736892ad6b31d3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f690666df6a207c4f4e30a060af724f76709d7a01687432ab97294ca32696d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c4e23502f0deda996fa4d25aba14add6f37b276400d8485aea11cfc9f863a238`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 1.1 MB (1100761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c50cd4bab32ccc61b282ff94abc03368367d9e055c0115d8ba80e76c197bca`  
		Last Modified: Fri, 17 Apr 2026 00:23:56 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
