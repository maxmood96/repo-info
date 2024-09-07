## `eclipse-temurin:22-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:d8ac5f15b7dc0a91bdfb89422f900383469e5de12dcce3949f145d713f455b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:22-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fec50eb3e37e43d833d53a7efa4485061f6ad59a8b0e5dfe5d2bd592bce4702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65861183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314adbaaca76e9f85cbf2a2d0ed8c4cc0dca288ba30e91fc8aaae7c0e7ae1a1d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='749e7372a7dba0de632592fe55a0e387d96922c84dcdc039e0efc1f7ecfcd70e';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='459342f5210cfd185aeed05abdc052fcd61cf6ff066541919b786236d69c5737';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb0eeeb44ea727a6840e888ba4140371726ac8b86f199aa403faf61b4de2106`  
		Last Modified: Fri, 06 Sep 2024 22:43:01 GMT  
		Size: 9.4 MB (9388900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce2a15a8add659833780eb59ebfb8b8005215f02283d96b6bb197577348aa83`  
		Last Modified: Fri, 06 Sep 2024 22:46:00 GMT  
		Size: 52.8 MB (52846231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f6a4700b23e40e7834144d380d3e8464d0ae32c6c06c3be1664d9c7af9f8c`  
		Last Modified: Fri, 06 Sep 2024 22:45:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638cbd597e80439cde2341262b3731b4cc8bdcc498bd4fb089353de1a8d40a48`  
		Last Modified: Fri, 06 Sep 2024 22:45:53 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:eac35f6d05df2cb7c1e78e732b8d382927391b3a5a1a651ae8234bbc74bf173f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65395011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ea339f611f053044012a5656fafd931cfb3d71f7e40df1bb96d13bef7c0e6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='749e7372a7dba0de632592fe55a0e387d96922c84dcdc039e0efc1f7ecfcd70e';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='459342f5210cfd185aeed05abdc052fcd61cf6ff066541919b786236d69c5737';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb1949836a78536caed9d385bba3def5c0b3e61a39783f843784225c480f4bc`  
		Last Modified: Fri, 06 Sep 2024 23:28:57 GMT  
		Size: 9.5 MB (9514486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fed4a34e643cfbb714bd7083f2d2a36bce1c0b913d450764b0025b207b3e06`  
		Last Modified: Fri, 06 Sep 2024 23:29:39 GMT  
		Size: 51.8 MB (51790633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b035e9f7a8c0524da06ed33a2b626673b0c421b622b50f01579705d78208bd06`  
		Last Modified: Fri, 06 Sep 2024 23:29:32 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1294c90da771d97170869fdc6f166798906a5de8a52179e39c69b4a01cfbe40e`  
		Last Modified: Fri, 06 Sep 2024 23:29:32 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
