## `eclipse-temurin:25-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:0c4c6300cc86efdf6454702336a0d60352e227f3a862e8ae9861f393f8f1ede9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ed4fedc9da0b231f7f8a6a9f09558489dd116ab457b68480f02a29e2978f095f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109329906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66da31cd0d50bfccf2a95e6a4339880a282e641150a72104b4f0275e7c292337`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ab655b026e5703579820f0d4485d514c6ec9d4b5b462890ac71da2da0ae46`  
		Last Modified: Sat, 08 Nov 2025 18:00:26 GMT  
		Size: 14.2 MB (14245329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f1a65d0fae852f6718306326728109ed1ddecfbfd653037dda93a9669e4a7`  
		Last Modified: Wed, 07 Jan 2026 18:58:45 GMT  
		Size: 91.3 MB (91279717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f288373361582707b01fea1abf34f4ff1053f3baee5acb21cf34af46e4f8c85`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3137254c0a4b1b24ea31eeee2f470985f40fee31365b16a41a6d5745dac38`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9b643ff411bb63a43a368325fdce410039f2b4b32dfca902ee32a9852221df11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **969.9 KB (969879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059b7fb004b5f81b09167b31d1e7125143d7a5763a84e4b4c19d42d90a5543f`

```dockerfile
```

-	Layers:
	-	`sha256:c672d62b54da9694a9e396cb710b3c9731f0325ed654b1671096eadd3f1d2dd1`  
		Last Modified: Wed, 07 Jan 2026 22:40:35 GMT  
		Size: 948.4 KB (948366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a18439c7b954a05876d043e2d8eae615a2323288ff79ffd90c0cc0fc418d21f`  
		Last Modified: Wed, 07 Jan 2026 22:40:34 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:75e0c6d894ec3c6e0f46e388b5b07dfee6e996cb2f2739c4d53eeb10615f259c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108683624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630ed80b72326a9dd13bb5974bc44ecd17ad6734d73fe9758f62922f674c5059`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:59:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b164f8b4d68be083596089650c1556ab1373815abc8abda59bc45d20ffd1c`  
		Last Modified: Wed, 07 Jan 2026 21:18:13 GMT  
		Size: 14.4 MB (14352513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde8e40d136c44f0d23e0b4d7594cae8888c80bed021fac4cf5ebebb75434c1`  
		Last Modified: Wed, 07 Jan 2026 21:18:16 GMT  
		Size: 90.2 MB (90190637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13765a23e62e85c56a5a54b976e0378167533c0495d297bb429a218799ab164f`  
		Last Modified: Wed, 07 Jan 2026 21:18:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c959ab9ac7fdf8f6393c84753f989ef0811ac7c86a2d184030c23e2d067c93`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:821925aa5a465853879fd4d397ebda7db6d0372e4a8573f4410c1d0626254e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a68e74db96dc69512501ceffc6ae5becc3387c79716ba9b973d95749d9aa5`

```dockerfile
```

-	Layers:
	-	`sha256:d449135f915bfadbeb598b7f9a698b2804052ebd9161037e36a499f13214fdf7`  
		Last Modified: Thu, 08 Jan 2026 13:55:00 GMT  
		Size: 1.1 MB (1098401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd667979f9d27d22cbb9508eeeca2f68a24b6d69b821c73c3844b977ff29a3d`  
		Last Modified: Thu, 08 Jan 2026 13:54:59 GMT  
		Size: 21.7 KB (21670 bytes)  
		MIME: application/vnd.in-toto+json
