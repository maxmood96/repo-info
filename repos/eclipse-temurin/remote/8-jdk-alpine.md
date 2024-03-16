## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:60746a1f895eb10d69cc1d82b7aabde8be6f316c700a06f8fe8889dd64438eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3edb7757572cf43970b9a56149ba6fb66c6d452e51be88523937f287f5cb9e0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113440292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0039aa5307d69adf4236ead0172978f2c1d446a71b124c1a41e1b017eb652440`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Mar 2024 03:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 03:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Mar 2024 03:22:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:22:34 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Sat, 16 Mar 2024 03:22:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c911fc057440f48c95f3eea8ec688732f43584e93fc0b090f5a361b2b6a64b71';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:22:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Sat, 16 Mar 2024 03:22:41 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:22:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976103255ec1c30e915c990ab7c4afbf0348497ea66d200421c4d2bc23d6dd76`  
		Last Modified: Sat, 16 Mar 2024 03:26:22 GMT  
		Size: 8.5 MB (8526752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ca92f67d05917686333845e142afe8b77283119a8374298674e4cbe88b24cb`  
		Last Modified: Sat, 16 Mar 2024 03:26:30 GMT  
		Size: 101.5 MB (101503933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd418c5265b9d736e8fae4b6cb89634551a9a3510e4291f24d4c2da36aa73bc`  
		Last Modified: Sat, 16 Mar 2024 03:26:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1171a607152584c1fb6d80ae47b5950d3f2a2618c2ea1db7042e17be383b8c32`  
		Last Modified: Sat, 16 Mar 2024 03:26:21 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
