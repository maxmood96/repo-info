## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:79e3e0daf6779d661285d1432d09a2398dc00a6c2b547ac9265238a21ecc5322
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a70d83458559c4b26ed3f3e202726a7cb394d9fc6507d0dcd6287607475c3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61598015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a902ea3016a8e890648e91294f5852b8c9b379a8e5170e9077ead11850f14b`
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:b2d7e198ae5284f8bcf7bdf0eca204d29448801c1c39a537863a8408f5c577d2`  
		Last Modified: Wed, 22 Jan 2025 18:27:36 GMT  
		Size: 16.1 MB (16135230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8559a37a29ffa4869ecdba6d70c4c486da4efb614d2a76a0b19da8cea4d8c3`  
		Last Modified: Wed, 22 Jan 2025 18:27:36 GMT  
		Size: 41.8 MB (41818658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40054bb8e19993e28d14a0c9417f25a1d853d706bf2abfd5ae55f43866dd23e3`  
		Last Modified: Wed, 22 Jan 2025 18:27:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239fd68696d7bf1834712d5c44b5209762b3ed4361672a79151220071425f91d`  
		Last Modified: Wed, 22 Jan 2025 18:27:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e425ef95d73bf279f0a7c1ff2c199d9fb71360e369c1f2261d0964901abf8dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.2 KB (941172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a079eb412fbafd885ad172a119c26cde26aa9b07db0c6b64dcba60dd5a5a23`

```dockerfile
```

-	Layers:
	-	`sha256:5f4bb06f0910f520688753a9b8666c033f79b0d424642a84fa8b2148165ebdca`  
		Last Modified: Wed, 22 Jan 2025 18:27:35 GMT  
		Size: 922.3 KB (922271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad104948bb78fe3927e798fd7050a11b763cb76a9d706e189178c5c3490b5a9`  
		Last Modified: Wed, 22 Jan 2025 18:27:34 GMT  
		Size: 18.9 KB (18901 bytes)  
		MIME: application/vnd.in-toto+json
