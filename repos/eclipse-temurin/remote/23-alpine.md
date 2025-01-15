## `eclipse-temurin:23-alpine`

```console
$ docker pull eclipse-temurin@sha256:2cb34eaa1bb3d1bdcd6c82c020216385ca278db70311682d8c173f320ee4f4c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:422eeabd64ec28fb46c2cbdf185a19c3bddb2353808fc24cbcf1aa9b6393ce0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189807930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ea9c0a93ba8062962bf2013020811b23f281db052853eba759ee444d7ba67a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8882735e21c791a47850ff1f22712790c562600ba506e9e98739dda3287d50cc`  
		Last Modified: Tue, 14 Jan 2025 20:41:28 GMT  
		Size: 20.7 MB (20665966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce94b72b036e1d425a31307aa924ed0b24b4ad1974b1f5bc3ed24d68cdfaca06`  
		Last Modified: Tue, 14 Jan 2025 20:41:33 GMT  
		Size: 165.5 MB (165513292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e2c87a019600d2f26696ca20dd7ed14ec90d8f55f9fde0cef33d73b9d9a652`  
		Last Modified: Tue, 14 Jan 2025 20:41:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bc72d1ec48be88672f2eb506b9b0257785e4724f39526b36c3d4e94bd24571`  
		Last Modified: Tue, 14 Jan 2025 20:41:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2ed11c12b8b9281c9d9e1ffdf813303367bc60a0258d5bc459c320e387ff194e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82d8a4b54869a86e218990508661b8d97637cf334f7ec1e03ad988293932545`

```dockerfile
```

-	Layers:
	-	`sha256:05d04a393bde02bb0f10b543e739de4c4e75f0a5509fd2b454d51f6fd71c95d1`  
		Last Modified: Wed, 08 Jan 2025 18:14:48 GMT  
		Size: 1.1 MB (1069101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69024e873e9ce334edfbd3aba99d6efc9e4444fd2bea3ea089d81ea6931d552`  
		Last Modified: Wed, 08 Jan 2025 18:14:48 GMT  
		Size: 20.4 KB (20418 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a239c253aeb2220c5383abd0512a51e9c2157732a9e2e605988c2431f50d8f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188454647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6263942692cf4a57171a8c0029219b877c9fb468229661a075f78b8f22a2090c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc244ccb78c83c616d89c961944730515db1ce4b088ac7593cc03ac34c0d4128`  
		Last Modified: Tue, 14 Jan 2025 20:52:46 GMT  
		Size: 21.0 MB (21045593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bbbd31510343a48ad85d8eb5271f29474a062af26db072842b265cedbebf51`  
		Last Modified: Tue, 14 Jan 2025 20:41:16 GMT  
		Size: 163.3 MB (163315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d5a373cae903ba2284309e6c480b8b7059d21583d5f833cfc77927aabd4563`  
		Last Modified: Tue, 14 Jan 2025 20:40:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618db5c82c2ef581bd482cf264175fc635fff361d83cb0cfe1166d3be65fcb9`  
		Last Modified: Wed, 08 Jan 2025 22:24:14 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cf00340d18867b25393c80328efb572c80a7769a7317f38d4cbc6206b22b4e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1193540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefeba5acfca0cbe5f047f316d44d391a6b2b7d7cd80c7c509867a896dc71d5f`

```dockerfile
```

-	Layers:
	-	`sha256:0ce0b52d0773ea7daf987213713cfdff49f6e93ec5bc0ee1fbe470ebf80c7548`  
		Last Modified: Wed, 08 Jan 2025 22:24:14 GMT  
		Size: 1.2 MB (1173000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdf522a5c9dbae5c7f5a1864d97906a81cd1997fe07c9f5cff0f9e6f00692e8`  
		Last Modified: Wed, 08 Jan 2025 22:24:14 GMT  
		Size: 20.5 KB (20540 bytes)  
		MIME: application/vnd.in-toto+json
