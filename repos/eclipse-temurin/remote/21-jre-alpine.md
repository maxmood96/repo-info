## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:4ca7eff3ab0ef9b41f5fefa35efaeda9ed8d26e161e1192473b24b3a6c348aef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3408c45e1faee20e4e68808939a75f87efa469b927d20e12309689ead053daba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73220220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab59740150ab3beff6f26cb814b36f6b3d51aae8959b288d98c2df258e093f5`
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:6a46580b98941ec4960dce678993b8f83a0b4d2d146c9d4e59e3aa6e788c13e2`  
		Last Modified: Mon, 04 Aug 2025 20:13:22 GMT  
		Size: 16.3 MB (16280189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f9d657519484ce2f35f23c98dec4ef4411ffbb8df53ae594b3563de635b94c`  
		Last Modified: Mon, 04 Aug 2025 20:13:24 GMT  
		Size: 53.1 MB (53137934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf466e9ba1cfaf9351b9b793d92033975eb18f8b2ffadf9b5720caea1fcb9f48`  
		Last Modified: Mon, 04 Aug 2025 20:13:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb760d495f93020b467e7edca17a273394c877a25c14ce0d90a9a039e90bcb08`  
		Last Modified: Mon, 04 Aug 2025 20:13:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8e4fa56e4bf8573d7cda32dcca29e51aabb857d451c52a60253df2f22023c5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.3 KB (917330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf8ddddad341a868577ef25d9f31617f7f706be4d661256f3402c2687ecd6a`

```dockerfile
```

-	Layers:
	-	`sha256:a2c1b46021257f6efbae897d324dd96baca232e402bd4ab3302285624276eee6`  
		Last Modified: Mon, 04 Aug 2025 21:22:01 GMT  
		Size: 897.6 KB (897602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55204dbe331af708d06c25429075186bad9a38ded10db51d0bd335b6f156ab74`  
		Last Modified: Mon, 04 Aug 2025 21:22:02 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d191c2eb1fc2ef6d07b4a2f4826a9721068b9e04dfc9f73fe9c36bab5faa4407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72574942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92c33ecf44d7d6ebe413dd757e11fa7ef89f23e5f7ad54aabdeb0b6547b26d9`
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:ffd236ccc4252742608647a184803cf19b13dab7c85740d319a502e276e8fef1`  
		Last Modified: Mon, 04 Aug 2025 19:35:51 GMT  
		Size: 52.2 MB (52199502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4789cfd3eee8c55f72c8490cccbeef6a351a5d9a39fda02bf49230337a064f09`  
		Last Modified: Mon, 04 Aug 2025 19:35:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e6dc79a2279a7c1de9e160680fa0150fca2f9ae5723ecc48b141f3c5378297`  
		Last Modified: Mon, 04 Aug 2025 19:35:45 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f89ebeef68dc78ad3640c6f7fe2ecaaca53d933178a035e0238ac4aff6947ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.9 KB (916902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cd8812c718cd6448004545f05cc2dd5a539b677f7420777ec6a191edc8fea7`

```dockerfile
```

-	Layers:
	-	`sha256:3d1076e442e908eebaa1522429251177aca4094a6f74d5e1afc7670575328f73`  
		Last Modified: Mon, 04 Aug 2025 21:22:07 GMT  
		Size: 897.0 KB (897040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6563b9dc9f27dd3858492f09e0b60e6490de5584fdbf79e74d325c74b8b5b90c`  
		Last Modified: Mon, 04 Aug 2025 21:22:08 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.in-toto+json
