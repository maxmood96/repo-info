## `eclipse-temurin:8-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:f1fa6fe71338fa2d18a70fb92e4938105663c00b668eac9c8db48da4c7354d07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b52722f7e92fd46ed802292bb853ae32ab63ad0fbcfbba0a40be8e73a53cffd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72457064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88492a834f94b4b987373a87d9d997a97882f1ebe01eabf4598af4c91ac31877`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:34 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 08 Nov 2025 17:52:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c7058b15b74dfb201889d176cc8eebf0e009d1264ef4645766c89a8432aa07`  
		Last Modified: Sat, 08 Nov 2025 17:52:48 GMT  
		Size: 16.2 MB (16174518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed793964fc06808c1c48d2ed2f1e336af9ce8afcbed06fda7667adf8e53c6e8`  
		Last Modified: Wed, 07 Jan 2026 20:05:59 GMT  
		Size: 52.6 MB (52637545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a0b8a249e37f0693c58d4aa0249528b1b9f088579d67b571362be1b1751a6`  
		Last Modified: Wed, 07 Jan 2026 20:05:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7158bcde719674de50d451bb0d6f64b92d07de6bd5a4b13da699df11c96aa7`  
		Last Modified: Wed, 07 Jan 2026 20:05:54 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bff9b9bd255bb0f2f8a03b81faeccd94f677c19dc2450a6fc7e41c7a1fe28f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4689888eca74978dcb064683ea56c125499f369af0a16841d0af47d23a4472d2`

```dockerfile
```

-	Layers:
	-	`sha256:e49280c5801ecf7b20ae8231762714d802b6d4b1236510c6f661f80a10d6616e`  
		Last Modified: Sat, 08 Nov 2025 17:52:47 GMT  
		Size: 1.1 MB (1100805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97912f2acf05f09565daee258b0a9080128058136c5714f6a0a2d487dcdf6d4`  
		Last Modified: Sat, 08 Nov 2025 17:52:47 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
