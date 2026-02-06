## `eclipse-temurin:8-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:c0ac572ef777b670022e03ed2ca46c22ee42e83c6db0a8dd9dfbce136360d4ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6d412c533ec42cabbed5bd61a7259422566f5f168504459e0ad34a50d52e6c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72878019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de04b041bd95d0e3d7b9bf6e152ced598eab233101adbd4a82601484c6f6c6ca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa92feb649a4fb8d7d1fb59d25aefc768eaf769fc0146084a45700bdcf747740`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 16.2 MB (16174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139044d6516fd53cf499322d945d57a044ef7026e60b967592f3698aac69e1f6`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 53.1 MB (53057192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ec9d3b4a0ae2f48cbd3f356a2342c62ba56808906410a919e563894ca3963`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceabaf44415bd7a392a9f7e17f46af37fd8839b43e97d33c918fe8cc39e0798c`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2cd988617fbce6f461889efde0494c6647d02080f92946422f93de0ee0f3fc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46412f8ad620db278ceb19671820853907f6591bd04e6a0afb16745ee641ce3`

```dockerfile
```

-	Layers:
	-	`sha256:cfeca4262088a8cffa29fc4ff28a1d6e2e25abb7688de4594cd637362c5539e6`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 1.1 MB (1101436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e0d10e11cd28be69a8fdb1e3dde33ccdda8bba92e7b32780e9aa93818d29ad`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
