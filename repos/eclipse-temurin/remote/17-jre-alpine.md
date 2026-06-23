## `eclipse-temurin:17-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:02320dd4ce20e243dfb915c686089cf9315c763084fafbb12d5c9993aee18b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b658bee7bbf0277559bd07dfb2e8473c30dc90c3da0d8cfe568e61f52792ce52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67891795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af15432fe4678068270da7f69356edd1e53555f15671a6373ce44d9e65c2dfcc`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 22 Jun 2026 19:57:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='22d4d5579902d134dede626d0fdfb95891abc7578e13dea9cb23775498c4cf51';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Jun 2026 19:57:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:10 GMT
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
	-	`sha256:1e2a2f574cbcb3f5f0d1d81c43cd8f7ed0ae3a658e4fa49f240978906d68f1f9`  
		Last Modified: Mon, 22 Jun 2026 19:57:21 GMT  
		Size: 47.2 MB (47229243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9b826e558088052ee5d0b1ffe535bfebc159275ee5601967839346cebfe243`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5bb06f25c55e382a04c0a0ba3681a1f392b0894814fcd6dfc7ec27615aad47`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:77a238910874c55e2e1fa7e6c775d79c73373a095d1fc4b49bd3361fb493348c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.3 KB (905272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02857be6a2bbfcd6e94df7d55563f779d3975c70848762cff7af7861640a703`

```dockerfile
```

-	Layers:
	-	`sha256:8078f8e9c2a0027864666723ac6d39bc1a13cd3f726587dbeee8d7dd24d65121`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 886.4 KB (886372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c5d715a7fed800d0f80f629f54d06c82c2d0f820b2b64f41c30c03db1f7846`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 18.9 KB (18900 bytes)  
		MIME: application/vnd.in-toto+json
