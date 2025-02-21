## `eclipse-temurin:11-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:def5150eb358489a11c3edf089ecca41fcdad611565ef87e5c19d3b90d21c40d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6d6010d8f816281561337b346b5f83543e4b85070e294399ca7617ae9efde135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63228956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e11f8934ac5e0f02f53a06795e6e3b9954028fd445cb3f39000369c45f7911`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='69031fc68d41189691dbeca73447ca543040d26995f61cef83fd7aed8fb4dbd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1063d10af070209ebda15cf3e8eaeb1cf320f99b1e5cdd5c5016c9be1ad62a`  
		Last Modified: Fri, 14 Feb 2025 19:25:12 GMT  
		Size: 16.0 MB (16023347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51787e594500db994ded2dbff85430b9b6c09c57016ad86f6597c2beb1d2d1b9`  
		Last Modified: Fri, 14 Feb 2025 19:25:12 GMT  
		Size: 43.6 MB (43576303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f4c36918c7faf84ab0510d03166180d497bc3833d70477e5914b3d6df7832c`  
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a259b61dba80f9391214006f689fa13a5ca25d14ffb0a663c164b7220dca35`  
		Last Modified: Fri, 14 Feb 2025 19:25:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:546eec2edc4a009ed8809c7e116c4ccfdc6200c9465b9ed279972d4510908c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 KB (914097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58f1e4c999dedf9bca1a9f2bd204ce2fb0aa759c89cf303dcf93f72a12b33b9`

```dockerfile
```

-	Layers:
	-	`sha256:7f303414489765e3b09b3c1942e81f33649ba3b699c0f5938cdcd9fc5ac27807`  
		Last Modified: Fri, 14 Feb 2025 19:25:12 GMT  
		Size: 895.8 KB (895840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:879c762148daa8c577eb23ed82321d7d83ea1d7e512476f4a24fe91c4b7698c7`  
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
