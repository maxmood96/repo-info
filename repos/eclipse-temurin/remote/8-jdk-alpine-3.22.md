## `eclipse-temurin:8-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:9d8ff50bfc81fc0965a38587b79062fd152b47f4c339513553abc15d6c62a26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:96271e23d7b5065e837a482e01624612a5a999e3dc2894925afa6eff857ce567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72732041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128350df605d117696146f6be99a798fe84596dc40ef21ca8a33e40e04f7af0c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a0c5ed7112f5699c4ac207aaa6ff3f277cd53844121771dc304877183ab78c`  
		Last Modified: Wed, 07 Jan 2026 19:11:02 GMT  
		Size: 16.3 MB (16289673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00e86805e496de548858bb7bc241431402e110f0ee0f8b305ec3fdadfa6d820`  
		Last Modified: Wed, 07 Jan 2026 19:11:03 GMT  
		Size: 52.6 MB (52637485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a6f189f97323a29e1384a0017627bbd029f10c4f53f4e0a246317953e853`  
		Last Modified: Wed, 07 Jan 2026 19:11:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec39477cf2e25f9f8db348d31ff41dd8cc0c64cb6470887efe494699ba11718`  
		Last Modified: Wed, 07 Jan 2026 19:11:02 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c5321042024511ef5a55f52af73247c371b06d078a2f0bae22efe934e857701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1123057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5ecfd4d3fb1ff540dcc760339b320d2e5ce3fb6b9e176514c974343a75a76f`

```dockerfile
```

-	Layers:
	-	`sha256:487d29f11b06c552f1102956a69c7660db0e2d36c82f2f0bc00648c4d7f8a259`  
		Last Modified: Thu, 08 Jan 2026 06:05:18 GMT  
		Size: 1.1 MB (1103354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee3e099fb0b9fb802ae8b1a456f82b87593012a4ccef013c780fb7424ecd108`  
		Last Modified: Thu, 08 Jan 2026 06:05:16 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json
