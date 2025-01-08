## `eclipse-temurin:23-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:5aa334404315c590f8262d1bdb1fa855c127aa219df30bad4ea35d553de58d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a0e9a561f3262b5679671ca7636dd641a22dfa360302cb920bab35a2d94699dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72746443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ba92c0964061143273455f6753c74ef761ce19c0b2d2e708bf52e2137b0bd`
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:39b935d8651fbb7964ef2bf39ebf221a1f442568de7694629e1761452a65b6f9`  
		Last Modified: Tue, 07 Jan 2025 03:31:47 GMT  
		Size: 16.0 MB (16005516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d5faf03857af103610e05659ec4760969cdf4009763feecfeb0572e148bc0`  
		Last Modified: Tue, 07 Jan 2025 03:31:48 GMT  
		Size: 53.1 MB (53124521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710623e6f9eef1d39a833696002c1e1aa241b4e12fba44c362d4aac7fd981339`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4758c61697a11e01955dac2d14d4c8a0753794a4213d900a0403371fc7907`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:92be42542ed6657aac52066cba91a8551fe5d6211e507ecf56ff20a5fa4c205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.3 KB (900293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc336592dfef6e2765a37eccb9f23979cd5ea8f4c4c3674c69d63349f506d482`

```dockerfile
```

-	Layers:
	-	`sha256:d7352efb9bf999cd2850727bced1938cfa6038ac1bdf47069013de3ce6b2b265`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 881.2 KB (881205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9aeef019c968bf3f644bf5b4201272661c30b0441791881c89efaa4e860260c`  
		Last Modified: Tue, 07 Jan 2025 03:31:46 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b49d10b11c15e5af185f578a199525ed0d3cba8e144706bb46ef8d6777c39c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636bdf2a0fe0c0e45a21da923f69e6bef89fec3464e98a86da63d6dd85c1a7d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b56eaedc094cb9107be2d5be9ad34c3dd9492c45aa671d102b5829a488cfc744';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='38a1b20b5ee8869b20e9f9aefdc91eedf245584d35287842a66540f0745dd3d0';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e61d1ed8c9b433eb57a691962584a6412357c544ac832c38bb6e22744d17ce`  
		Last Modified: Tue, 07 Jan 2025 07:28:09 GMT  
		Size: 16.2 MB (16178922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6563d42bd3be9bed6a68f47927bd2480bd126e4287bb7d4c9acb9da8a821500b`  
		Last Modified: Tue, 07 Jan 2025 07:29:21 GMT  
		Size: 52.1 MB (52076142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a534dc9f3984c6c787e3d8fa1236ac0b00fc9bcf496a12548e714098e9280`  
		Last Modified: Tue, 07 Jan 2025 07:29:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415d26fb7980d3cf6b988ff345c325d0e28a3d96c9d17805099bc6b9bc5a40cd`  
		Last Modified: Tue, 07 Jan 2025 07:29:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:70a8bbd4daf48cc1f0036cc3739ac06e15da1613820e496b12730805943066f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **899.2 KB (899197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a1a18e0fdd313f9c2178d09728ea798e51ac3815f3d320e8118c0734e64fcb`

```dockerfile
```

-	Layers:
	-	`sha256:f7e688884d88342d937574e36cdf2708ca9b14779dd8ff7a9754253afb4b4c16`  
		Last Modified: Tue, 07 Jan 2025 07:29:19 GMT  
		Size: 880.0 KB (879998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6458c0c541f18197c05b27b091d3ab8fc3a9ed45e05abd3b7b466ca40ba1f4`  
		Last Modified: Tue, 07 Jan 2025 07:29:19 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json
