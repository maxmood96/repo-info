## `eclipse-temurin:8-alpine`

```console
$ docker pull eclipse-temurin@sha256:46b9cd0be9515b7994570f4dcacf54acc6a45cc18f74952d2dfcb47fafb5d410
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d6a907d30e024efdeb318c9e9320518b46629e703e0bbd2b029b99ad8d3d74a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72390190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12e7d9e425cb77ef49fd5cdf1b23ad7338d64e2a0876031589899f112e8e5eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c424ce528b8a969200c72fb8dd59bb4245ca7ceca1e0338e8e20243cf13105`  
		Last Modified: Wed, 22 Jan 2025 18:27:34 GMT  
		Size: 16.1 MB (16135176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5d45ed21cb09747b5d1c53aae5f27c01da74be5d9248b1c3d518e31692af6f`  
		Last Modified: Wed, 22 Jan 2025 18:27:35 GMT  
		Size: 52.6 MB (52610867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227d4657ee96815baf764041d2d3803f17f8dd8a87a828071f83b176b68fcb19`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073cdb653eb72896613ee4b3625fbc727fa740f7dc1aed1d4d10d218bafbaf0f`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:99fd33a6d49f93f92f276fa968c1a47396c1ad35159641b1b893676be2de4c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a62eb25a257e0fba1da8cc2bd94417d886a847c254918ebb3bc6f4ae9ea2295`

```dockerfile
```

-	Layers:
	-	`sha256:e0b8d3b9cb2b71c950b0bf34a2066bab6e7de77b74f913fc6801cb1c2b3b2f18`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 1.1 MB (1096549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b058d11414dd5e09208c0a45067cb667adb7ea1f3c681174cc06857b244bb2`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
