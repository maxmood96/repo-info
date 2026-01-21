## `eclipse-temurin:8u472-b08-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:a71179cd5fabc87bec9ac6b2dee1fb4e61a6d858bedbaa8a7ab45dbd44b35389
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e74c814ab44714f33f5075a139deeb2ee6f45c0be382efa0afe791318fb8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72290386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2b9b6a98ec8defabcce896ff5f6f21927780c3ae21129417abb9a72ab85223`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:05 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 08 Nov 2025 17:52:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed3a176af17e013de668113328e26aa67569861f4f68ed60c528f20cc85b6b1`  
		Last Modified: Sun, 11 Jan 2026 06:21:40 GMT  
		Size: 16.0 MB (16023376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3d2fa979d7690987cbe42cc68615268d3eaf8d115f47b935c4d2e5b3da5834`  
		Last Modified: Tue, 13 Jan 2026 04:12:46 GMT  
		Size: 52.6 MB (52637525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a463aae538bb8e74d3606d8f5a8894d6d127b79c14deb3e549bf510e7b12ea9e`  
		Last Modified: Tue, 13 Jan 2026 04:12:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a84b328027f8539506a14decf3c86838c30346e6283c876e8897d15b11619c`  
		Last Modified: Tue, 13 Jan 2026 04:12:44 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4eb648eb68ca39c06090f1abcaba743d532d8f3a9605aa13938eba5b35054a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362da931d7bc43ed2a26c3352f3bb391f4a7a0ce18042aa994a5911d92c5782`

```dockerfile
```

-	Layers:
	-	`sha256:41dd50352dfdb3966ca7b7a318c9f78e0a27c1d0c44135fe2cb16171858f1c35`  
		Last Modified: Sat, 08 Nov 2025 17:52:22 GMT  
		Size: 1.1 MB (1093554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1221f2dc8e8dc43eb0a8d798f14786bb4bfc5a462914208849a218cac5cab3f4`  
		Last Modified: Sat, 08 Nov 2025 17:52:21 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
