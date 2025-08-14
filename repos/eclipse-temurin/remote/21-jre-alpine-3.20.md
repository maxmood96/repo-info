## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:d17653429d21ec7167938493252796ef5ace7ba97f35768b67bfc40857ea7ef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d6fa7ade67191738ec81734df544acc39edcc091e07b46d633fc94ae8bc8f507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72772430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3452d67a37eef2d93c08418e523a55d7cb3a5f4c00bdb2f28e77b28e78a101db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cf9aeff9449e710a790e709c931b64bc189298a358941de13350a343ab70a0`  
		Last Modified: Mon, 04 Aug 2025 21:37:07 GMT  
		Size: 16.0 MB (16011611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229ea679746a032ef8454501b6c2a2fb9fde93f7b6cda28f004dca291ed51a6d`  
		Last Modified: Mon, 04 Aug 2025 21:23:32 GMT  
		Size: 53.1 MB (53137932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfbdee8ce27d5f8610a65c88df4f721c28842ac41a03f21c8fdfdbe0ceb4e4d`  
		Last Modified: Mon, 04 Aug 2025 21:37:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7650c91a67c4cb3db4b4b5d38c4e1cdc8991cab6a2f540c0561a1c239d984568`  
		Last Modified: Mon, 04 Aug 2025 21:37:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9acb340a564cb0cd7b9461ff23f83f8fd07ed9f31880b2d82f88e1f266004ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.2 KB (907177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8fc4e2399656c610c8169f3e2a0699f81bbeee3bc4da97d782e6b780773af9`

```dockerfile
```

-	Layers:
	-	`sha256:b5a50aaa00d91f2642cdccd44f291ff50be99130f7e585b8e3838eca4bbc0005`  
		Last Modified: Mon, 04 Aug 2025 21:22:08 GMT  
		Size: 888.1 KB (888122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05859aa26607b0de7560ee91f3ae80cd8e682f6446050fce9077249e138979a3`  
		Last Modified: Mon, 04 Aug 2025 21:22:10 GMT  
		Size: 19.1 KB (19055 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f9715ce29532c187f93751afefa8378cae62528a9a91043602b22973e4090da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72473934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7d8a65ba09c26353677c0efa01c5722bf2473ba837c3773752c013a50bdaf3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88254c03f06475e00d661ab72b92e53dc4ce694d8a0761ed1e2ce49d2891281`  
		Last Modified: Mon, 04 Aug 2025 19:34:59 GMT  
		Size: 16.2 MB (16183605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f42f765ceac29214ba394afb4187ca0e7d2c0b6003748bbb03e6bc73e93227`  
		Last Modified: Mon, 04 Aug 2025 19:35:03 GMT  
		Size: 52.2 MB (52199554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8fe5c9e8c0567242f442d953029dab6114fa898bdd3955e7fdc2c3ff1223fa`  
		Last Modified: Mon, 04 Aug 2025 19:34:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be40b55565f56573d415138ea0715da9f649122e37e6084e69307f06fd5ec2de`  
		Last Modified: Mon, 04 Aug 2025 19:34:55 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d9f7eedcab34a010376d66a301c86b5cbd19cd6eecb379ac5a3b496455c99b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.7 KB (906702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30e475ebfea11e0bc73d0d50d2706140a303b475a189d905899ce9e3e1782ef`

```dockerfile
```

-	Layers:
	-	`sha256:409bfa1eaba61e3fb691492916d952b2b95b034fdb419479f7e4df2f09ba9df6`  
		Last Modified: Mon, 04 Aug 2025 21:22:14 GMT  
		Size: 887.5 KB (887536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c4e39f154e3f361fb967df5056a7319ad7354cf225b94e5c47c66ad48027e9`  
		Last Modified: Mon, 04 Aug 2025 21:22:16 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
