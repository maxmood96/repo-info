## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:b725dcad6ef659dd63dbb4e2e7f5c64152b513ef6b0e9aba827530ffcb8b5ed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:10ec0933ac950a51b908103b1532443200472e0278af7571cca544af97a0d9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114565267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cd1e06ef559d863966c80fa6f9775731dbc83ec162b28d7b4e6008c7dbf2b1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
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
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='525a7731331cad502b9293ccb4ac2b13e85516736e98a57cb27c2767005188e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0210391ff06386c858b74d27ffa9aa8216d62faff8a1a2b8cda5a7443bde9684`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 9.4 MB (9389054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c493cdb4e467167231a52b19c3c347c1bad39ef0d36290b76197a57070523a3a`  
		Last Modified: Sat, 19 Oct 2024 00:54:58 GMT  
		Size: 101.6 MB (101550149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799853a821993f97b0bbe41959b5714f589bb3eba5b54f2ba9bc56ad9389e0e9`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1759b110d7b8c023033f17c4a086e83a7eb738d3df75b4be5aaddf1f34209387`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 2.1 KB (2129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e72de1e4d4dff85d5ce72a394ff56a84ec6fa58d418243b8fd7cb149a5d60bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe5028e69d2c70682c06bee13e8ad8b57ec6adb44009a48ebb719fa0c44d6f5`

```dockerfile
```

-	Layers:
	-	`sha256:e0f27de57aca3930b3de28396059267afcd7acfc895fe32544460631ff8a2193`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 986.7 KB (986682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb576c920c5d32307d3ccbf7ac93d934f3191741e4295f513ad0a2300bc78b20`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 17.2 KB (17205 bytes)  
		MIME: application/vnd.in-toto+json
