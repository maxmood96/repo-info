## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:4ed285b1ef28b63079fe92d6b96e603313721842bf18a2c71665957e45a5da69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:12ee936dd5c70fc417fcf5d645b4bd34c353db8c4e60469075206d6364cf587b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66266754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2819dd78443abc530abc2d0e33b452f151f1aa822ce93661ffc86f4b885f53`
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
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:eb8680a91e51a67c6401d73e01e5bf67b7f9afd5035c4bc304a28e38aaec5c7e`  
		Last Modified: Wed, 22 Jan 2025 18:27:42 GMT  
		Size: 16.0 MB (16022263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e606d401b285926d746036f07f2fc61bebe358d2637b6186358545ae1d53044`  
		Last Modified: Wed, 22 Jan 2025 18:27:42 GMT  
		Size: 46.6 MB (46615821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75f0046194b40b59f28bf0af77d3dd8429991d930c63eb7ef9999b24a7d947`  
		Last Modified: Wed, 22 Jan 2025 18:27:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246e3e77337be35acd4ca1686aee748e92f75b68bbfc2fd6587f1be04adff06d`  
		Last Modified: Wed, 22 Jan 2025 18:27:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6b7a78a2f4cadce04407e8cb362249d573d26df6bb0738668ef89a6466f8694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.6 KB (901622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9e72e6af070b3ed56692fb597dab7b6fb1e9dee3708ca0f5118c7bae6f5908`

```dockerfile
```

-	Layers:
	-	`sha256:2c5ef3ecf744650dd6d200ddcd61a9d39257c646ed41b6edc8aa305cf1c9da45`  
		Last Modified: Wed, 22 Jan 2025 18:27:42 GMT  
		Size: 883.4 KB (883355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42565ebcf895cd1e9d70ab55b8d8ca91ecc36f7170efa94f4464494b5f4cdae7`  
		Last Modified: Wed, 22 Jan 2025 18:27:41 GMT  
		Size: 18.3 KB (18267 bytes)  
		MIME: application/vnd.in-toto+json
