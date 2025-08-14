## `eclipse-temurin:8-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:5bed78cf0b5bd72f094cd7f392fbb952970a5305aea25ae6782456f203ff566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:70ba0b161db5b498e60a9b82ebf737025eb38ed245550cdc09f8639202734423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72269941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e13d4a168b95f7aa09d25d2135cf4f4645c09cad67cd01d4a2dec0b4b7599b5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb16f434c055d3ff72141911d21afdbed9b254a4ca5f910982950c5fcc75036`  
		Last Modified: Mon, 04 Aug 2025 19:10:41 GMT  
		Size: 16.0 MB (16011629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486ff238d336d90bfbd75b0ab60af077fae939b716abe528c7833aa64f5e32d4`  
		Last Modified: Mon, 04 Aug 2025 19:11:01 GMT  
		Size: 52.6 MB (52635405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a724bfa29637b63e720243a4bf4a04b7dd50a3164f5f9665b4968d69a7c592e`  
		Last Modified: Mon, 04 Aug 2025 19:10:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa50d8a9e4630e4c66e4028b39d952f38ea693970d1932ecaacd9eacfb370b`  
		Last Modified: Mon, 04 Aug 2025 19:10:39 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:79456dd9c68a1529548ea6716b5253a2a76de91daa07ca60ee5dae73146c2766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c979643e9364230772293190889a3b4e0cfbec8cbd870e4f3d9a344a1cd851d5`

```dockerfile
```

-	Layers:
	-	`sha256:38e02ab6d99071d070f0339d1df7d7f3e4643b06c9039d5cce6337f2a23f62fe`  
		Last Modified: Mon, 04 Aug 2025 21:27:51 GMT  
		Size: 1.1 MB (1090941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bbdabafa5f5b602ef2b604c6be12ec08ac200b3ccfbea25f22adae75920444`  
		Last Modified: Mon, 04 Aug 2025 21:27:52 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
