## `eclipse-temurin:8-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:ee8ce0e58bdc8e809a8227d739b8edcdb03f918a1396e05ebf8db2e21dcd9e7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b19e447a906ae9b0a739832a618ac108dfd19683bbe43591afba9f95a34eaebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62138606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e71d55052a68a7d9b197f105c319379335ca51f037576a5ae25a27dbbd05fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:26:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:26:04 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='82b74dc9042ce6735624a1ca9585e6a43c44f0f6093a7f2088b0a622f304d62c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 21:26:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f331690fa6273c622b66c6da013109b0617a6f337f3118cdcf143581dfcbdf35`  
		Last Modified: Tue, 12 May 2026 21:26:18 GMT  
		Size: 16.2 MB (16219814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2abe23b9d671a2a4f60c2b34b23dd4ebc560b701302d2b9b36b6432489c97`  
		Last Modified: Tue, 12 May 2026 21:26:18 GMT  
		Size: 42.3 MB (42269328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305012812e9654bad510ae6f4f3063a8884b712d1e8bf9c158cd74b34b69baef`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316332ec49cc0f96322c816d446104173bed84a16b00f33fe6913f1e42c51a11`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a65fb6d9e59e76ed56eafcaef570fd11acf6584ade98e29bed7d2ee6ba71950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (944983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601d86b9d42b56582740f0a8080326d32524793f2c9fa3a4db4ac477e33a15fc`

```dockerfile
```

-	Layers:
	-	`sha256:471d5fde9351f83817d2dbe82d0e115a10dc9721ac64ed971b3e04c961a9b7a0`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 926.8 KB (926799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746784307a17508795a2f647d3eb9090b8f6f9f7402d46e44d544864dbb076cc`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 18.2 KB (18184 bytes)  
		MIME: application/vnd.in-toto+json
