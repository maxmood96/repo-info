## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:990397e0495ac088ab6ee3d949a2e97b715a134d8b96c561c5d130b3786a489d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:464a8b23a76a845a1fc264c1556490c3617ee6f294c05b59c8e39deab0c9e1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73232516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8085de26b22c47624f9f83b1338c46b779c59970b13f1a18413755eb802bc3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34074eb544964325947cf053120e471db056320ce1089be54d122cbfd5d19698`  
		Last Modified: Wed, 08 Oct 2025 23:02:03 GMT  
		Size: 16.3 MB (16289728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb71aa46e6fc6589b7af5382eceb462d8a2544336a0c294d3715ef0ead06d7`  
		Last Modified: Wed, 08 Oct 2025 23:32:29 GMT  
		Size: 53.1 MB (53137928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c21783ef0dda74d68ebb56d6f5a5993644691702b4ddc6f1b0c162ee908e5`  
		Last Modified: Wed, 08 Oct 2025 23:32:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d459441faba5cbaf0f42a897007302e4aaeab0e3a4fe43ef0fa5e062ed1eee`  
		Last Modified: Wed, 08 Oct 2025 23:32:22 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6922b851273c34aae695ae2afcb0be98708c12be067bb4ac3b39d683f5dff406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.9 KB (919943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fc5679bdaf7878763313bfdd9cd3874e3c6293b41d078ccf9729bf9161429`

```dockerfile
```

-	Layers:
	-	`sha256:300dd613bb320635be869706c3228a5ebc9ab150478355a1209ccd8fd0467acd`  
		Last Modified: Thu, 09 Oct 2025 00:15:52 GMT  
		Size: 900.2 KB (900215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f64c7a00863e3f15748a5d3734423d174f35675d2941e347478c62488c7c735`  
		Last Modified: Thu, 09 Oct 2025 00:15:53 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9c1ab8a28bd037acb7180e4a2b5482e33bdf0d732a94e1c3736f090e00392644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72593620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec604df60fef8b66cfd52f67caf637f40a62778b7ae1bde9be2aef84340cf47`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ec98e526c319c733b87bc6e2535fa8894f12ab4142f4f93bdc3dd1938d487`  
		Last Modified: Wed, 08 Oct 2025 23:14:37 GMT  
		Size: 16.3 MB (16253662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fcc419d6343089f7bc4a8c81a52b00350ee115e32b700c39ac64d0d2f03362`  
		Last Modified: Wed, 08 Oct 2025 23:14:39 GMT  
		Size: 52.2 MB (52199482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6abb19b3d42fe19200b4a27fa6814a4dd05834414641368018ba39cc07778`  
		Last Modified: Wed, 08 Oct 2025 22:40:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec5a06921ce86a261b442e907c3a3b1bdd86f6e02c78edac8cad9f2605a04b7`  
		Last Modified: Wed, 08 Oct 2025 22:40:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:133e62adb48853acbcd7e2182e69d349a9120a17b231b1b5af125c44e963b65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.5 KB (919514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5081d72c7e1c3acc5dcb4838c8ac0918c7b7f2b2177223be2b13424bd8f14eff`

```dockerfile
```

-	Layers:
	-	`sha256:7072f587792d83fc5c320f16d2c17b1530b6893c3064224c85f40b2c55532e4c`  
		Last Modified: Thu, 09 Oct 2025 00:15:57 GMT  
		Size: 899.7 KB (899653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa98a9b05e8a9432d36da94e2d29807504d59fd92d5e738b94232394560d1a6`  
		Last Modified: Thu, 09 Oct 2025 00:15:58 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.in-toto+json
