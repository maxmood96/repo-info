## `eclipse-temurin:24_36-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:de5771de73039724b43ec147a2f8c67e443d0cb393a3f9486ebf9e3f28341429
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24_36-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:57d320e4896a3c015cc3f38f8f19ae6eabba5a315340e9be25d8f1b61dfebe35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114373410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3d825da4420607949888531408c4cee4c791e371714f24523ff6c6389c8958`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61bc7a4fd9d62b9bed52e9ec6c4e63e3ca0805c1646536573646f0bf2903771`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 20.7 MB (20670079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57085a5adc330c25742ed4711ba675ee1772044f6a98de26f185680bffcca497`  
		Last Modified: Tue, 25 Mar 2025 21:57:42 GMT  
		Size: 90.1 MB (90074023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6545ae97d5790ac1c20a5fb4db53ead103ca565db71611279889e12b5e933d9f`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff465b00e3c2356556dca353d65753983c3ec643a661e022ac4106a1ee5477`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f3f6bc3f9b1d083f03f76d34ab44cf75645310f25f8170f370844476c686f390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1035771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2890bded681cb6b0d33b05a8292480e78ea5257b12576517effbf955e0307`

```dockerfile
```

-	Layers:
	-	`sha256:8ae4ccd375377b06f0ba372edc40313b74796c8c6f86a0561bc206b05e4592b2`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 1.0 MB (1015370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87fe9a415ebe141d50623f4820dc42a3624e57b472653723e2f4a0b2786922a8`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5eec48acdd1be2e57225ccfba83f75042105a819148241d9b460c9227b4855bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114208811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718a7b25cfbbc4497eac95cd159199b494505ac163601bac7178c5ccc0310f4c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939da5a79730880af724e707a10f40b17b679ace112d8e726b12b65a8b176be2`  
		Last Modified: Tue, 25 Mar 2025 22:02:02 GMT  
		Size: 21.0 MB (21048630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8657f883cc4c186db95dafd2a1c66ec0718b4480c0d69e68abf9ea499f727e19`  
		Last Modified: Tue, 25 Mar 2025 22:02:04 GMT  
		Size: 89.1 MB (89066605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a9e2a00cf010e2167d3eeb7fd40c4f628e218c1749c7bb6144b6b1c72bd436`  
		Last Modified: Tue, 25 Mar 2025 22:02:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffae84c8e39d6e2c6ede93cc974ddc24d289bf9f6c3cb0f0c5d7be78cc1676b`  
		Last Modified: Tue, 25 Mar 2025 22:02:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:552311ed40ed09505294e47506d027688a9c0119b3b84589c774d59370b205ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1140411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67bb43de151ee6d33c2c3d2a409ca700870ce14658928636d6bd1d8c3b6d07a`

```dockerfile
```

-	Layers:
	-	`sha256:64e811c4b09afb3c3155330fc663a1381dafcd6031fd49959d4bf38bb8860d96`  
		Last Modified: Tue, 25 Mar 2025 22:02:02 GMT  
		Size: 1.1 MB (1119887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65d186a71f4b0a7308fa68b5f5d2a30d0079b535c56324ef6b69df3dc4bc7a8`  
		Last Modified: Tue, 25 Mar 2025 22:02:01 GMT  
		Size: 20.5 KB (20524 bytes)  
		MIME: application/vnd.in-toto+json
