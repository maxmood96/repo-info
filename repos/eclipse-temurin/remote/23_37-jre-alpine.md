## `eclipse-temurin:23_37-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:ad2b64309402deb0253c9027ee9f96357607b33a030666b18b9f8e2c793ee7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23_37-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f232a068b43494dba98b6cc83f50b3a533a0a5431b8eac3a99e134db64e9b787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66135051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f1209f5b92fc31b1e9361ac789a76a30406904308e76483c0637a9cc0a0a5c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='858aa6b255164e535e2fd6cc8dfbf129327a9126ebb9e8f24115c2089efd36f3';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='7acbc972b0dd84ca10ec6f192b20e76445a22f4c5558e1657ff393e4868e9343';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9250dc2876db7840239fbb88331997f2d4bacdd12cd13ec17445edc00f141a6`  
		Last Modified: Sat, 19 Oct 2024 00:59:29 GMT  
		Size: 9.4 MB (9389055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e6692bce6997fe953d567cef80c3791d496df3ef13133a61fa6421775af07`  
		Last Modified: Sat, 19 Oct 2024 00:59:31 GMT  
		Size: 53.1 MB (53119954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ace77dbeb490107e5d7b0a4e0dbdbe170314bebde3f014183196c5bcea94a4`  
		Last Modified: Sat, 19 Oct 2024 00:59:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3355cf598d70e26b49c8aaa0016e645c1d9ee078a618a077ea989895bb4efcc9`  
		Last Modified: Sat, 19 Oct 2024 00:59:29 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23_37-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a8a23c3fcf565427b68aba6c1b566ceae711ebcc248fdfb41c92558acceb77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.9 KB (801918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e1b86c7e24d0e3d2e051343a7d5ecbf00cac20ac224ee2092e1109beaf6dca`

```dockerfile
```

-	Layers:
	-	`sha256:6e60dfea9a1dbafb64c4f07df819301f41667d148591dd932a8d8640539eb695`  
		Last Modified: Sat, 19 Oct 2024 00:59:29 GMT  
		Size: 784.4 KB (784404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009aba3e1dba14f8f4134c3d55d6dfea0fa7e61ae189f45cb5604dbd4e28ec2a`  
		Last Modified: Sat, 19 Oct 2024 00:59:29 GMT  
		Size: 17.5 KB (17514 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23_37-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1eaca820e6e66c1b13192815dbf9979877f287b0af634ad47eca9e314668c626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9d42adbb8c4a1d197f807772e24c01e78c4f91efe2771695a399b504c84ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='858aa6b255164e535e2fd6cc8dfbf129327a9126ebb9e8f24115c2089efd36f3';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='7acbc972b0dd84ca10ec6f192b20e76445a22f4c5558e1657ff393e4868e9343';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe858122ab028c64a3fffeb0f39cf14498fc825d71dd5f74cd2ea534e7a84c`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 9.5 MB (9514761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e19246f2bbed2c8752aa5a90beef7702671c97756fd8ace382711158b12ad09`  
		Last Modified: Sat, 19 Oct 2024 01:21:19 GMT  
		Size: 52.1 MB (52068451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef95aac7ce39b6ac16ab07db5e4e181151f63a26a735156935857f987fb85f78`  
		Last Modified: Sat, 19 Oct 2024 01:21:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25afb00855c5ff0d43d4c9eace92a614da78c2ad8923b7f14ca64406ba10aed1`  
		Last Modified: Sat, 19 Oct 2024 01:21:17 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23_37-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c23d3882da146666a4e54e8d5a8ca099497528c31506e2be40ccae67f078de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **800.8 KB (800814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a2743730d59ea3b53f9d42634ba09de2cbf52b92c71772c2a98f9e28754061`

```dockerfile
```

-	Layers:
	-	`sha256:92e6de09e54279e4c2e32464b2ea5a24a7addbdc5189a6fafa8e0ee25b25ad8d`  
		Last Modified: Sat, 19 Oct 2024 01:21:17 GMT  
		Size: 783.2 KB (783195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d06cda026dc07f159c4001b09f1e76e5731ab6d9c2b38675060ee4eef8a6bbe`  
		Last Modified: Sat, 19 Oct 2024 01:21:17 GMT  
		Size: 17.6 KB (17619 bytes)  
		MIME: application/vnd.in-toto+json
