## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:352e77071a1d60c3fb60184015c8e11414efc404192af794b505e78ce3ec779e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6cde7e6ae3c23c3636f3fb4b92836d1323c13929d9ee27da1885cc231c086101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63689128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9d8253d6d5f2641369fefa39c408391a5f50de368af205380f95fa0b652879`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b0092a3f753beb13221fab3a1ce713390809b4841b4a5eb407f9819d628c8856';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34074eb544964325947cf053120e471db056320ce1089be54d122cbfd5d19698`  
		Last Modified: Wed, 08 Oct 2025 23:02:03 GMT  
		Size: 16.3 MB (16289728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55c2448f5039642ed84b453072a289bdad7e7c123d466f2a45ecafb78c2676`  
		Last Modified: Wed, 08 Oct 2025 23:02:08 GMT  
		Size: 43.6 MB (43594541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6fbbf2f4ff5fc7d014b56ae82e41a306ecb8182422609f0a72653be4fdec3d`  
		Last Modified: Wed, 08 Oct 2025 23:02:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927dd97f74e93c542946e8769c26367f3a4ddd16b0bd3f629f472ef5fc75af82`  
		Last Modified: Wed, 08 Oct 2025 23:02:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5eb97410da75fced84bb8bbb4b2f6166c6d99f7fe42fe04ec23356e46e703f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.1 KB (929141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92067a8b3c8845ce2bbd8f297d82b36227c86f78ce7e0b72c0b52397e319d07`

```dockerfile
```

-	Layers:
	-	`sha256:e0890da27258f2b7d95daf014b63752d58559357ca314b6c2fa6bff33f7bc731`  
		Last Modified: Thu, 09 Oct 2025 00:12:50 GMT  
		Size: 910.2 KB (910210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d144b38ca2753ac38430bbbaa9d071e865dbfeac1dbdf9851e02451a031caa9`  
		Last Modified: Thu, 09 Oct 2025 00:12:51 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.in-toto+json
