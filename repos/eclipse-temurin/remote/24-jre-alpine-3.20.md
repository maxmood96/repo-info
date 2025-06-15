## `eclipse-temurin:24-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:578c2a0100caddab1fd3d8fe85773495707ec5791fe0f732368935cb20a783f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:90e8d9ad1129495e5fdb15329135f59f6d32277d3bb96808c9081dfca2236265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e3b6e17e0b3f1617c490ad67ea5baeef912e77a899e3cc75479d59f1469417`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1e8b49129ce3208299c93a73455b090909a65478313ed411b4574d09c8ae9670';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='409eaa7cf973e5d47b285cd86082b620422e6bbbcf0314c10346250f1e6c66d9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43c0fe76148e7ac583a8455c84072973d698d2486f9ecef14ce4da7c06529f3`  
		Last Modified: Fri, 09 May 2025 14:34:02 GMT  
		Size: 16.0 MB (16026140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a40b417a35da8743b34d65b36e383fa28a99c4d4729049e9b06012f2f496be`  
		Last Modified: Fri, 09 May 2025 14:34:08 GMT  
		Size: 61.0 MB (61018026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1815f0e0b0d92477e621a07152c4d5fc54b292256745ac3262ba522e315e26`  
		Last Modified: Fri, 09 May 2025 14:34:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495aaa0840683b65827b28a3693c34ced8c575583fb8f609c0308603b1f3c92`  
		Last Modified: Fri, 09 May 2025 14:34:01 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:539de02159911e22b4e0d38b50caa5db51758c838c840dfeed503c9a71e96c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **912.5 KB (912470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1fb113813afc5fd02d688b2ea94291814488428cc6607f68152167232e78c3`

```dockerfile
```

-	Layers:
	-	`sha256:c3c51114c522a19b11a259ef8d432d94a0000d1fb114363523a3105f3ee03459`  
		Last Modified: Fri, 06 Jun 2025 01:58:28 GMT  
		Size: 893.4 KB (893414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a7b6ceea3c238e9688a90e5325527d2998603bcbbb53a11973673c36834d8`  
		Last Modified: Fri, 06 Jun 2025 01:58:29 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:30113d0b08d049b8b66f76042ce965637e95e9517cae72f7dcb6e9edb9901ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80287520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5820a99fa153e2a6ddfd11761deed37e721b7a01fe7ac7d0c4becb7b29d1a41`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1e8b49129ce3208299c93a73455b090909a65478313ed411b4574d09c8ae9670';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='409eaa7cf973e5d47b285cd86082b620422e6bbbcf0314c10346250f1e6c66d9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bb2c8ab96ec5802c937701f95ed05e1ce8ea25900c4742cf1f574d1f43df3`  
		Last Modified: Fri, 09 May 2025 11:51:36 GMT  
		Size: 16.2 MB (16190846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1240a095235c738c60db9f2f52a00d9d8ff493e5617bc6987c6dd8d21d8a40f4`  
		Last Modified: Sun, 15 Jun 2025 23:17:56 GMT  
		Size: 60.0 MB (60003103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53139f8b41005f912a822dd2ddea640eaeb6dad783a113805fc1df6a1d0361b`  
		Last Modified: Sun, 15 Jun 2025 23:17:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2e57b37406ef01af7d3af5e8564154b6d243f765927c68a5f7d63562c3bfb6`  
		Last Modified: Sun, 15 Jun 2025 23:17:55 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bd9709037721e1272f19d01b27b822ccfc0c5c28f5e716c49ecd6ffe3421b901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **912.0 KB (911991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ed212ebbd0300987b48f85b6044f0a2b010ca101e0f01b1789755e915bcde2`

```dockerfile
```

-	Layers:
	-	`sha256:042a5fa22653c3321b273fe9c42fd34feca519a055560568f03f3a4066e49419`  
		Last Modified: Wed, 23 Apr 2025 16:47:15 GMT  
		Size: 892.8 KB (892825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9f3113f490f8aac973856bf377c22f59bea8e22095a0fbfa9497f776ca41f3`  
		Last Modified: Wed, 23 Apr 2025 16:47:15 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
