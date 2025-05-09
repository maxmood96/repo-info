## `eclipse-temurin:8u452-b09-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:9d2888ee830fd3b657f2a771606ac31c36a91010f2decbbfce72991ac0f100a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u452-b09-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:93de8e1b8a18c429beeb1bb3a413e9cec8c82847a3fae13940968bcc93fbf699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61640889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f5a985771452fe676fc793245b29788749f7ef93213739f9a8bdd58156ff8c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3282abad4d63a1cdbfa9f98a3d73e7e09bc810a5612f5f37586c0df901478082';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c668af62970b4de5d59dec2be3c7a1f58548a07633a144ab80003c977c9895e`  
		Last Modified: Thu, 08 May 2025 18:23:34 GMT  
		Size: 16.2 MB (16176563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b607b9e46b772c125c916dd6b8614cf795fec908918a1c560e68980cc012578`  
		Last Modified: Thu, 08 May 2025 18:23:37 GMT  
		Size: 41.8 MB (41819671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9876e4c65a536c01eb83dd439047aead82848674d43cd087320c26735beff118`  
		Last Modified: Thu, 08 May 2025 18:23:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062de40987aeef360de18d3eac683c24b505fef8fca608340c9310aa51644dde`  
		Last Modified: Thu, 08 May 2025 18:23:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u452-b09-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c2c61836212fcacea6ad4b040d068a52256738d368893f2fc9688bb0227a64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.8 KB (941801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6e2892dca72696ba16ab5a0b62e2b9136ede8f7387cc2e39de96beb3bf2cc`

```dockerfile
```

-	Layers:
	-	`sha256:a51a7985c7430508bfe5e350332f1d3922d2f0fcd823c06cb7feb27e1c8c8122`  
		Last Modified: Fri, 09 May 2025 07:11:53 GMT  
		Size: 922.9 KB (922899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3f58db7e686926a8576ca0d6393284ad80cfb9df2f9a8c426aea7d670d1f7d`  
		Last Modified: Fri, 09 May 2025 07:11:59 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.in-toto+json
