## `eclipse-temurin:23-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:2942277c4201d4d80258968f27a6fd978962efbe3dc017ab6019b74ee35c5f8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e32d6cc19eccf6fa708571a680750d2b82b962cd18450380a43227cc699cb417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72784868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ca7abb8e15d3edc76c12412b1171f1a3a6c1f667f581cf10ab8f10f5172ff7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='248a2ffb3abcb0cee7841ce648af7af415c96ee88cba4f8bf676c0115d38de5e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='4513750bd10cc6c38f0c19d335dac7dcc112bba64e52010f81ba29e7a71e2a76';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47871035e49a74d24752f1df92308f5e3f511f9462b2d1ca61a88b7659af5a7a`  
		Last Modified: Fri, 14 Feb 2025 19:25:42 GMT  
		Size: 16.0 MB (16023365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56daabb5a04f92ed40c1b0a33228fb79eefc5a3bc0adda3d46f4a282a781417c`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 53.1 MB (53132197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8a43ca58a1d8a68953b4198a5a4d21ae206491b45e2b158444ca98534574a`  
		Last Modified: Fri, 14 Feb 2025 19:25:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729a8c4393a4876bb9d1546e7adcfe1fc214c28cb182a5f972c1fe8408f99ed`  
		Last Modified: Fri, 14 Feb 2025 19:25:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eaf04f53d31f2a346a2326464b63cbf4ecf4a9b7880281d134f93c986659f14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.2 KB (906154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f93518598e89f7ebd6efe26c31d00ed4d1e5ea3e1cd813e0a36cff52551bd7`

```dockerfile
```

-	Layers:
	-	`sha256:2aa95d616de07f327e64a7441ebdb819b2358f9247ace23a0230f994e7fecc0e`  
		Last Modified: Fri, 14 Feb 2025 22:15:35 GMT  
		Size: 887.1 KB (887099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b795bb79a20bb1dc5b53d1ec464d1fe89abd1e3a9f8df90dfca3c5ca6ac1a6f`  
		Last Modified: Fri, 14 Feb 2025 22:15:35 GMT  
		Size: 19.1 KB (19055 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aae7a87a2ad22c153af8e29fc07146bfe61fe85bbee454214b2e2f4dee7263f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72405409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7955a1edd1a5e112fd8add219c65c30947281a007523aa2fb0ff0d9a0439f4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='248a2ffb3abcb0cee7841ce648af7af415c96ee88cba4f8bf676c0115d38de5e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='4513750bd10cc6c38f0c19d335dac7dcc112bba64e52010f81ba29e7a71e2a76';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b958a013f248c526fcd471b7bd0d5f818c22cf4d8645053fff999c8bfa740e`  
		Last Modified: Fri, 14 Feb 2025 22:43:56 GMT  
		Size: 16.2 MB (16188631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf7edcb59732a386f0f8448b14ad4e9a7ad7cffb0353bd0bb0dd98fc51a706b`  
		Last Modified: Fri, 14 Feb 2025 22:46:06 GMT  
		Size: 52.1 MB (52123204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71ccb64ae85bce9272ea1d1558352d40d68e16725409ed2c277a7a5bdceff12`  
		Last Modified: Fri, 14 Feb 2025 22:46:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41255e6e7d23e0d102ddde291a1ca85998a689bd5fb49ac8f5ab4dcb31a303b`  
		Last Modified: Fri, 14 Feb 2025 22:46:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ebf13dd8175684a0d9c1216b659d30608dab2f5498b5b41cc261b91ac5d8ab1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.1 KB (905057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecb65c342e4c935fbc448f6bf549723801bb530e580682ae805fa7e6e17f607`

```dockerfile
```

-	Layers:
	-	`sha256:5c58dd4331e4b6dacacd04c1a46c56e43fbe44216aa11da8f4c60644970d3d7f`  
		Last Modified: Sat, 15 Feb 2025 01:14:58 GMT  
		Size: 885.9 KB (885892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e100375abf7df55749f2841a530ac4885d741e1be366b712969241e009929298`  
		Last Modified: Sat, 15 Feb 2025 01:14:58 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json
