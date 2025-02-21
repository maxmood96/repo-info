## `eclipse-temurin:8-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:0404e82e770043a571c26e1f5175a63d9c33450ab7156a5f50a0c4f37dded730
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b25310fb103db9ad13763c6f617eb230da8791bec813a368615b23891edcf110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61476725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd869d0cd7d48811a091fa6eebcffee57116d6eca0951562db27868276804f4`
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4fb0636534b0cd4534a3cdcbbe7cf2e937523d6376d9cef00cc6cfd5d19537e8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:23be4c441f4ce771b459982d75caad67dc9e4061bdf094690f7cd9b290188667`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 16.0 MB (16023471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c0e0b1983b1809c642030aa99358cd266837575b9b0bebdce9305ae2dd1425`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 41.8 MB (41823947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb653b79f50152b98bc9181e457100d854227740b5903015ff279145de70b2b6`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560d57b3f543c50f0deb4192457704b9e0cb22d145819bc8bb7f68f607b0a0e7`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0a00210a02ae935ec66193aa7850ac91fd571e4eb3f26bea20215a54648820cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.9 KB (932938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aaaca756d20e71bba2db060eb093cadfa9979fe4157fc5c65aa2eccfaeff78`

```dockerfile
```

-	Layers:
	-	`sha256:d34dc2b1192d25cf8d1b51dd572a1ecb8d4ed905d73cef75ab9c0c154e3ac601`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 914.7 KB (914708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b65f3b14e64ea150442f479c17f94bcea54c56903b9e515b51f37d8c371edb`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
