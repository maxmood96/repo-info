## `eclipse-temurin:24-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:4044b6c87cb088885bcd0220f7dc7a8a4aab76577605fa471945d2e98270741f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9a4bd30f02e82e4987d56cc8ac5d7e9d13a2451c228c1f5d6978a317d18d1cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81136135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f124345954221a2af9aca8d818887eb3f6760d3094ee26bfecc6fd9c0a0ae44`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='389100187cf328c7b6b6b390fc0f5071ab38e93e8a6c06beb11e59363d2fd0d0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='b63b888d2415828168c4d35a62d88f385a5532a20b7391e30a5d5d0a9a73b892';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dda662de862c31e361aaf9941adb39df0ee900619ad7ca7ec794490d684cbc0`  
		Last Modified: Mon, 04 Aug 2025 21:28:53 GMT  
		Size: 16.3 MB (16280122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cdc3450078982fe52f70d0cb244632ade948838e3eaf449ae4faf73264f2e8`  
		Last Modified: Mon, 04 Aug 2025 21:28:55 GMT  
		Size: 61.1 MB (61053916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa02523b85136c61cd89327e04d7db5301c588ef3ee91a38115c6a059b205816`  
		Last Modified: Mon, 04 Aug 2025 19:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57288d3d16f003430fc38ec8146d9b1206d2ce550dbe94fcf0692599f1ffab1`  
		Last Modified: Mon, 04 Aug 2025 19:25:56 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ad7c88b0df031deab6e756ab8a57a9f98375f08b40db0096a6b1f60743460693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **924.3 KB (924295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c491ad3937774997c4367405cf16cd1a3c02afe7cf4c05d15f48e775490af04`

```dockerfile
```

-	Layers:
	-	`sha256:13f8990dbaaa4f2aa639691fde7fb97b5f36b63786f35e02bb4f1e223119268b`  
		Last Modified: Mon, 04 Aug 2025 21:25:50 GMT  
		Size: 904.6 KB (904553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868dbc13fd63355c52123fc9052a43b2bb2f5a69b634a5b7fa00c1dfce010457`  
		Last Modified: Mon, 04 Aug 2025 21:25:51 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:00323d2fbc01646e5e072702c90b832aff15b4e61d75d97886bf6fc4d2169d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80419932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e27fc7ec6c4c48053b3980a7a53265663b30b7137b9b71e31b715071871840`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='389100187cf328c7b6b6b390fc0f5071ab38e93e8a6c06beb11e59363d2fd0d0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='b63b888d2415828168c4d35a62d88f385a5532a20b7391e30a5d5d0a9a73b892';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b71ebe70c7a16e0a9ffdaaff0d0ce7808eb197bfa3724d8cd4df50d91cc442`  
		Last Modified: Mon, 04 Aug 2025 19:35:46 GMT  
		Size: 16.2 MB (16242283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d88f8e971f90754ac8f4d9f7266e371ff3b7ca6a37eaf376be3d94b64deacb1`  
		Last Modified: Mon, 04 Aug 2025 19:42:55 GMT  
		Size: 60.0 MB (60044492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195f3cc362cf26ad9609bd376f9b4d7f479cf811fbeb0c2be891eac9ea6ffdd9`  
		Last Modified: Mon, 04 Aug 2025 19:42:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0caebc32f589de398b1370c6150c6eebecb9726af74b0ed6897f7bd3ea1c89`  
		Last Modified: Mon, 04 Aug 2025 19:42:48 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5556272e9d23b65115eebff5591f3d00be2641fa0eca470b614a6781ac44f65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.9 KB (923864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560223162e6da4e6e04f26f40620f108091590fd023ede4cd5bafe248d1e5a52`

```dockerfile
```

-	Layers:
	-	`sha256:1503733ea1c390cc1bbbd6e40874e11e798f1e15b68b78cf794a5486d062dac0`  
		Last Modified: Mon, 04 Aug 2025 21:25:55 GMT  
		Size: 904.0 KB (903988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbe3275f596e6414416f127572df9eafb632037d2c09de293b30edfa259b7fe`  
		Last Modified: Mon, 04 Aug 2025 21:25:55 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.in-toto+json
