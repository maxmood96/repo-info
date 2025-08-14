## `eclipse-temurin:17-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:fc47f4a190b599de0835d98830976f5938588b4c17b07f19dba903d5b29f666e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c10410b27cf9ee6589a4dcdfb8277a7264db331e8a548562fabdf41354c5f3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6999cec90cc852901ce7eee2b0d8d281ef1aabe129b5ea84e6b8caa1de37304`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='88424be8b71d7c801c39866cf19d3b7c49b1c499cdccfa292e103c7cba08c21b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2752d65a63e3b8c4fb7950d2928bf6d39b65f2e10205b7bd13ccf5294fda1fba`  
		Last Modified: Mon, 04 Aug 2025 19:11:28 GMT  
		Size: 16.3 MB (16280115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d077c3d94f53d4cc9f31623b79dfdf4d879371fb6b3eab31f31f44109e12af30`  
		Last Modified: Mon, 04 Aug 2025 19:11:38 GMT  
		Size: 46.7 MB (46664526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6416375b2a72eefb771654e6a1bb9ca50021d4e891a59c6feb058b7ecb5d0`  
		Last Modified: Mon, 04 Aug 2025 19:11:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b392aaebe6179613c78f2474bff6aecdd37380275b7d032d281864c29542def`  
		Last Modified: Mon, 04 Aug 2025 19:11:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bd3891987786191789dd500dab075e537702d6df406dcbe0c4df45a7adb35ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.0 KB (914039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fccb305dfe9d68fb07f727280e0c74b6119cd444c95b01a5406d44ce2e8666`

```dockerfile
```

-	Layers:
	-	`sha256:359065292f675f81b2a5520205754a9c23a4ee2ded4f25f0199e80e2b5ecea96`  
		Last Modified: Mon, 04 Aug 2025 21:18:04 GMT  
		Size: 895.1 KB (895108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c83b24ce3bdc2f6cce95956ab666fed82adc92204173bb035d9b9a83012259`  
		Last Modified: Mon, 04 Aug 2025 21:18:05 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.in-toto+json
