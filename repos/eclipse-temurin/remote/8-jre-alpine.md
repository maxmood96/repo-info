## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:59975ff6c596db462345fca2d8cbe07111a1fb8e6eb261d74b76233ffe543f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b700759379daba5a5d3224bf059204929683632e8a48e10c34041ca9f645fcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61440582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7f05640e81a1ee79700d9d782bcb08c33eec031169c9f8f773fc747693ccd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4a7091318439a22582d83eb8aea2835f2d69cd676dda553fee3e529df2828`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 16.0 MB (16005457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af11ddd595e2b74a9b722af0c9dafadead6e3bba40f85f2315287ced3705fcf`  
		Last Modified: Wed, 08 Jan 2025 01:37:40 GMT  
		Size: 41.8 MB (41818718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9431085ea9f47302df8b525243552dbfbdedb7f0e9d4ae4b5fff0bdba985338e`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433f318eeaf47ceba55c535d79c262193cb62bbf946de4b0c11cf6100a1f9f7`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e8e95cdbae4d0cb8a9c0ef04a98a5675d9ee7fafd2f6e3d67247fa7e4a9097c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **927.1 KB (927061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39b940596b282757cfda158f2ed38ee279bcbb1688843e034829727353506ec`

```dockerfile
```

-	Layers:
	-	`sha256:e99e231bb2635651d8f550c270e1027c07695e06008c0a06fe6a042895d1ab8c`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 908.8 KB (908810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83682b12d7e3320cc0ad4b0e64d43ee6125d859d0c78ebc5c675dcf5f51add9`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 18.3 KB (18251 bytes)  
		MIME: application/vnd.in-toto+json
