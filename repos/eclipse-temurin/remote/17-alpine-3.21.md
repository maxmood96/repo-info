## `eclipse-temurin:17-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:733db8dc78c0ccd3b4d99012d992b0361b543debd936e53cd96dd86eb0fd40f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5e6ef093af64b2740aa0471db62139bf3722ed51c5eccfdf59304822d5b95f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168442748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1494617e5054736f0f6fd14a02c6e18461891813354e891a5a1004b0c8b05150`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db05edaa40389dc3379a8a8bed4bc87964c5544c8dd6b5877beeb6f59d8b3708`  
		Last Modified: Wed, 08 Oct 2025 23:34:06 GMT  
		Size: 20.9 MB (20948502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb4845cfb386c2025e9e6126acb47a43cd6da133c1df4d18f17068d2c3f0dc0`  
		Last Modified: Thu, 09 Oct 2025 00:41:50 GMT  
		Size: 143.8 MB (143849267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c47c3fa1a6ccf54135026e652e509acbcb0b8362416c5ffc8c02df9844eb56`  
		Last Modified: Wed, 08 Oct 2025 23:32:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d83d2bf972c7c76695eac325168340bfdcf0a6a6ffca93bcf34bb2564264d`  
		Last Modified: Wed, 08 Oct 2025 23:34:04 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f79e1105fe49d5b74bd32bf49e7e96de7847cb55367c8aaeef333e2a99a666ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c345acf73d74bd1f02cfb8c85be3714f2d4d81fb168afc016c1fc2cf6fada87`

```dockerfile
```

-	Layers:
	-	`sha256:4275b4147d8812f8c17d3619e4e8394d4f21937ee29772c44833a39ac761922c`  
		Last Modified: Thu, 09 Oct 2025 00:13:52 GMT  
		Size: 1.1 MB (1101218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41964226bd9ea1df31a46e322349e519406575a275c288bc4a7fd4cb7a59ccab`  
		Last Modified: Thu, 09 Oct 2025 00:13:53 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
