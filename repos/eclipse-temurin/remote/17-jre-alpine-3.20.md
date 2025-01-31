## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:1aea098107cccee34debf17542bdaa905e531b8fd5892516b0530f3daa3b65ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:49ce716ca9f0a76444c2a32e1ee3d5b8a21f35b65ddeaa9633f652f3c39e6046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66270289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbf3c29b6a4526f3f32aada87855423d7f0661faaf49210ae38ef22e305042c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee8c945b514a7d33a899c66856ec7965d1f8b79c5cdc6fc97481aaeb06c997`  
		Last Modified: Fri, 31 Jan 2025 01:30:50 GMT  
		Size: 16.0 MB (16022312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae2d166d9e3d3d163198ec702f858f4291c40e6c9d75d5ccf65a14d73b4f6f`  
		Last Modified: Fri, 31 Jan 2025 01:30:51 GMT  
		Size: 46.6 MB (46619310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c5bd4062773e5b0f05ae439c2e9c03ab0d09556481a56a4805a146d2efefe6`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1e883321ea78caee9c64d84267e12dc2b63ca32e4c57c808c3f3857f03b9e`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1fd54bff16dcb01928d9727fe02256018aa616c2d7baf1712908ee5e077bdcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.6 KB (901608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0ea13577f977d3bc03f809859753afc34d5012f1c66626418a84b2ba0f1aab`

```dockerfile
```

-	Layers:
	-	`sha256:082dbadf99d81752ec2658677b2e692db0b7002a6a51c72d59d40eaa924555a4`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 883.4 KB (883351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af460b1f50d2a5e0d85699064f45a6011bea4075f5221ec82e8b47661df5cef4`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
