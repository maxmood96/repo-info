## `eclipse-temurin:8u402-b06-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:dff37af60caf65653f457aa2927e0374ea9bad79e465ed74200fbe85c3c408dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u402-b06-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:220904a2ae2499eb9ea78165bc30e96334445cffb0821c8268157ea8574fb4fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53738075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c1871877ba9e3709cf8f583b367ec228291c5b4dae43797f7935675f319d5d`
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
# Sat, 16 Mar 2024 03:22:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='abc7861abda181ffe4527997ef8267e701385f11b82d91bc3a56077be228b0e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:22:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 16 Mar 2024 03:22:59 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:22:59 GMT
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
	-	`sha256:a9af73063be2b192bd2e5c9957a7a51f4271f855365c7292a21b58bee118d6d8`  
		Last Modified: Sat, 16 Mar 2024 03:26:50 GMT  
		Size: 41.8 MB (41801718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8158b733087c5df5b96dd7fcd47015cc38fa47d24e7b91d64c087aa407fd6`  
		Last Modified: Sat, 16 Mar 2024 03:26:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5920ff788ce25d931abcd8429c86bf9dcb395b3a67308b261fec0545b08e00`  
		Last Modified: Sat, 16 Mar 2024 03:26:44 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
