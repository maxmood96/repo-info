## `eclipse-temurin:8-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:7326a30be690a12bc992d33bcccaeb8c5add3b9647b6705021adb21168621e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d58476e7925dac537ba1b5f1db07cab19fdd4f3ab0622e269cc0582c4092a319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89626e93e927efd5c3661810df742a54cdf7887af330855a5c86f63e83c9a66f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b69af96aea51a07a67a16f78374eae0d189a7369ea8e0d415119496735b460`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 16.0 MB (16022331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e50fbf6cf18aba2f01b38290fc88880984f957f115287b7ebab2a2585be4c27`  
		Last Modified: Wed, 22 Jan 2025 19:42:17 GMT  
		Size: 41.8 MB (41818658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869d909d00e4cb6420fadd1738ded32d22c0ec0b5fded0bb479aff98116d445`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25660c2d01d5b99e587c8602a2dd062c2b074f5ed63709fadc92d9463068d277`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7987ce646973dfc5f83098dc6c345811138e428941aa2fa4f0c6c3ff930246f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.9 KB (932938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f7b36d8b164f1dbf69fa2bcb261c87b87a7dd186384dd298baee220c612db1`

```dockerfile
```

-	Layers:
	-	`sha256:e134a747f78aeaf00bf9bdc48ecaec31fd9a96d19cd6f02f25a3a9aa45c815d8`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 914.7 KB (914708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66710223152d9a336349d7a86181646960233390096949988c5eef713aa408c7`  
		Last Modified: Wed, 22 Jan 2025 19:42:16 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
