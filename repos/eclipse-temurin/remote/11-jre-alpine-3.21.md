## `eclipse-temurin:11-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:1ab781a9b6655cfbd703de40fed9fb9ebc2b2bcec06a0f2d8bfd491bee8c56ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c261157e90a6706d46980eda5b09b2b11513b1fecf0848c9dd16ca56231071b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63450751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643711189276b87009779771da0189b1202265d8644c1784a8ef5367e9e4c60`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:16:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:16:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:16:23 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:16:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:16:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b30f7db6fd41047c60978bd2c88b6b9bea108803482db4e163dd7fd2b1aec1f7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:16:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5368de0e20ab16925a91241d0853a0d57a9e0277599204670cd574359f422edb`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 16.2 MB (16174595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff12de03c27f866cf52724e7bbbb050360c6db0fb90f44cb5daf6ea8de53466`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 43.6 MB (43630006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319038bf655b5164f1949d6a5f1254d172b9780861946dab64f9a36a31c887dd`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe8e9b73940abfd43abce503f126679a3bde80483a4c95ce3488e529a7df428`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c332bb039cb7bcc962b1c086c76ecc8bfb54107e350c1c25df1ff7e75fc3bb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **927.4 KB (927446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221b89297b93086b389962cfba83e8f3b520d5b22633f6266b591e37b526858c`

```dockerfile
```

-	Layers:
	-	`sha256:e4f9dc0e1b7bd97e96174874f5fe93609cf026d34827484a1e39ed09c8919af0`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 909.2 KB (909233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f53aab958d1dc250f722f85161abdea125bc947d448a4b6f251fb779d39ac5`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.in-toto+json
