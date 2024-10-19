## `eclipse-temurin:23-alpine`

```console
$ docker pull eclipse-temurin@sha256:e28f3fadcb8e498ae6c2ad0ba617bb193dea50c044cd8972016cfdcfbfc98f25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4e443572bd3c346280b817e63e47a2f55ac7d5132caaeded2881eac6f2b07a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183135666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f23c9dcf047df24836542bb796cc16b1ad66dc1d331ec6d00979189c60824b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465b99ed376b808b3496edf1585f2ad0cb453ae29a1d59ee5096f69d6be8535`  
		Last Modified: Sat, 19 Oct 2024 00:56:58 GMT  
		Size: 14.0 MB (14032592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bf0b0c1d7ee2470cc2bf871ee2b35c2857b0f7c9faced7f45d964eebc5b0c`  
		Last Modified: Sat, 19 Oct 2024 00:57:01 GMT  
		Size: 165.5 MB (165477030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e077ca61de339e804266d1ee1932d35309101b9b23394e95c804b0dc7e1de834`  
		Last Modified: Sat, 19 Oct 2024 00:56:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b359dd7cb5656dfcad483a65e7359531a980675f992e33c22da6803270508c46`  
		Last Modified: Sat, 19 Oct 2024 00:56:57 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7a20f5f2e68c135f4fbc946e4609664b4eba74436fb140e80c74eace38783711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.6 KB (985555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20213f625995d0ffa936d77b160c35bc1c9241fc0aceadf98e6feee4c22b1dd1`

```dockerfile
```

-	Layers:
	-	`sha256:e1cf8555de001154b3c866401010c7f08f5d8658857812869f6c4583b80de538`  
		Last Modified: Sat, 19 Oct 2024 00:56:58 GMT  
		Size: 966.7 KB (966706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb2e6ffd89ffd95f4c7854673d3881ca647a4dff884f6e0fb5c56072fa525f8`  
		Last Modified: Sat, 19 Oct 2024 00:56:57 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:628b01b277b85d50ade8c422d3d2c72ce8993f892edac48db4a5779584c02690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181719668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b36a607e3e4e5e365d1709ab2373e857e71c10f9bee4fb007049c4783b3c07`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ffed20e52cfa038b814b564cae31f18768ff4978e451b3979a4568ce125972`  
		Last Modified: Sat, 19 Oct 2024 01:17:09 GMT  
		Size: 14.4 MB (14362084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0dad56c14292d8f4b636f13fa54db72494c67fd2d0650a1ed17da33aa5cce`  
		Last Modified: Sat, 19 Oct 2024 01:19:54 GMT  
		Size: 163.3 MB (163267702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d194437ae17afcd17871df023bd2cc4d2216e7850bfb84e9b68c60d5b5aebd`  
		Last Modified: Sat, 19 Oct 2024 01:19:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58523fe2e2ac664663587856f69ced66f71c48e832aee670dcba01cd57822a98`  
		Last Modified: Sat, 19 Oct 2024 01:19:50 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cb216fbbdd95b5db4210382f162cba253e665e75059f9f065d6e7d5052c91e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620d8bd2bc846a88f337eb5de208a6799a593d96adeb73f62c03090e2dc018a`

```dockerfile
```

-	Layers:
	-	`sha256:af68d6a1f81d50f513992162c401268697293450eb223257c8d9367105c746b9`  
		Last Modified: Sat, 19 Oct 2024 01:19:50 GMT  
		Size: 1.1 MB (1070765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ac41d2bf199138409af37fcd09f7d5892c049d4672f4692a6ecafe0d0d6cd5`  
		Last Modified: Sat, 19 Oct 2024 01:19:50 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json
