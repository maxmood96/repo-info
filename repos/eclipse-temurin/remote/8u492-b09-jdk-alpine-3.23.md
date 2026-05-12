## `eclipse-temurin:8u492-b09-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:4c71112abe43c03f85027d5fc5f20818af20f5fc1719194edfbbb5985361c8f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u492-b09-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4765b076b7f1490f0fb1396ee59c83a15e0022514cc681894efc97073db05cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73803982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8647c474db2ad3213c337d46d96da423c6f746ef9850422ea26326884a299f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:54 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:24:54 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:24:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da768393bd1fd01f1eb6c504dff19511d9e30c336b824982cfaa816d7ae3bdc4`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 16.9 MB (16857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805e08e2635133b31c002e70773f34ca1d11e644912952dedd445645df358cbe`  
		Last Modified: Tue, 12 May 2026 21:25:10 GMT  
		Size: 53.1 MB (53080117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058485af113ceb7c1eb1d8ad0c051356cb888365a4b326efbc1f02420996a473`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da3b2c25d4119dc7bdb3820a5b39c43fedfd01438b0158496000c4fe4625c1e`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u492-b09-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d5a024eb75780b0cb12e61f7e29fd77424f8a4d841897d9b4df8a8371c139acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1127346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3559421819bbd1608520353226547fc47213c17bfb0fa08d6c82808a9fe51116`

```dockerfile
```

-	Layers:
	-	`sha256:3a1e998595ef96f81f7e386e133dbba0ae3a478b5b75fc8e62f009b4d65dfa0f`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 1.1 MB (1107643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca4cb8c2cbd364f3c6b0762618cf17eb15b965dcf6cd7698b129d4f941a48e3`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json
