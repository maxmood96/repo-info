## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:8ee6d4e8a3d46907e424b4366eda7dc8b85089b60ecf29de8ecc76209d5bfaa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e6960ae5ff68e0d67a03cd1f3ccceac525035974d5afa8555af75a0e9d74ab94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72790643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0845432d7521724695989e078553e46a7210976d2948623c1222f0379ace1981`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05937e20b513bd51a728fddf33dfa4277303ec8ee7a331306eab46ea4a4b95`  
		Last Modified: Wed, 08 Oct 2025 23:33:09 GMT  
		Size: 16.0 MB (16023260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedb09d43347c87c8caf75f5738f0a36a4ff3cd1635a762dd23b02e7e79a1832`  
		Last Modified: Wed, 08 Oct 2025 23:33:11 GMT  
		Size: 53.1 MB (53137917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c21783ef0dda74d68ebb56d6f5a5993644691702b4ddc6f1b0c162ee908e5`  
		Last Modified: Wed, 08 Oct 2025 23:32:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b1498042c005285e382f16e912c007f6f4df87127e41364eed9103cfb4a1b1`  
		Last Modified: Wed, 08 Oct 2025 23:33:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f500255a1393699d39dbff2f5c8521f73baabad444423669d51bfc9bbcd96646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.8 KB (909791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7acbe25f3ad8801d3b24221b929ac757d6d2790b3dd618c144a59ee08670c9`

```dockerfile
```

-	Layers:
	-	`sha256:63ea454101d7d46a961d470ac2f54d833a4d1b0626d9d93d4929c6c46f68c013`  
		Last Modified: Thu, 09 Oct 2025 00:16:00 GMT  
		Size: 890.7 KB (890735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeeb34e15b1ffd1c84078a402d5c2c48a270f677496b66a614ac6c63450ab0ff`  
		Last Modified: Thu, 09 Oct 2025 00:16:01 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:03aed52bbe1efbb186eb68d560ece59d106ac9b7ec452da9e993bc1030806ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72482748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de60f9fff67dad982465fd34a881b23e7355fb5a60f0992450fd486dc1b2c926`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
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
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcea4325871070b7d1aebab704ea0e6dc81af81135cf0e041f0b63ca80067d0`  
		Last Modified: Wed, 08 Oct 2025 21:48:28 GMT  
		Size: 16.2 MB (16191451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7657bf4a746f21274d0115ec988173e7b89f29df5d378e6a056355978637d`  
		Last Modified: Wed, 08 Oct 2025 21:48:31 GMT  
		Size: 52.2 MB (52199513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce837704dd32df7d8c2fa54693e4fba0bb2ba2500b7feff82d4f8efb92294a0f`  
		Last Modified: Wed, 08 Oct 2025 21:48:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f849dad057f46537913d743c65f394cf7358b503e075f4fc599d154b58a7f57a`  
		Last Modified: Wed, 08 Oct 2025 21:48:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:33f96a050d2d9136edd65b5c34aab426c62de607d48ea03c96cf7a5f02dd6504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.3 KB (909315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8dd656132ec0790414d555d22e13f3a1fb942f6d93e8b3064e429dea155fa`

```dockerfile
```

-	Layers:
	-	`sha256:a4086f0eaf01130e1aa8b04ea9d6d9ffd76d69ff5ae184e98d8ff99ee3eebd95`  
		Last Modified: Thu, 09 Oct 2025 00:16:05 GMT  
		Size: 890.1 KB (890149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fceb1f91d49440886ba5cd9b31b0398079c8f583dcbabb851f34f6ebf375016`  
		Last Modified: Thu, 09 Oct 2025 00:16:06 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
