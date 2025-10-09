## `eclipse-temurin:17-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:eb42bc053cbff0d750d76fa0705b6faec2677131a1358d0bafcc844051b8872c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:444fcc044076e6f4541e9dc4b5638ba396b2e90cf532341a48b7c342b6ada288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168766413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4a4f978301df7d08e2c938570dec9044fa0c3a03691c08a53a238968aaee3d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1937952509e436077f4a70b207391ff2952aea2922b7deae7361fbc9118ca2b6`  
		Last Modified: Wed, 08 Oct 2025 23:38:33 GMT  
		Size: 21.1 MB (21112251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d81feb8e4c44b7ff1badd0be8121868c9df3dbb89de14480386c09be1dcc56`  
		Last Modified: Wed, 08 Oct 2025 23:38:40 GMT  
		Size: 143.8 MB (143849301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c726083d78dcb9d36bda1ddbff32af0c7984e6b7988d4b5d2b7a0d4dcd16122d`  
		Last Modified: Wed, 08 Oct 2025 23:38:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4359672316646bf68753af35443bba0f3c31a7c0d4ace7f9c32b39872c9c64`  
		Last Modified: Wed, 08 Oct 2025 23:38:31 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2930afa797e9b8ca8edb2388bf8a3c79b557b0446f137616918158c6ed0fcc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd4cb1841ac65deba162135d61078b26d5e0d5c36bd89bb14019442a301555b`

```dockerfile
```

-	Layers:
	-	`sha256:6ca6c0648313ae49c4ecd5865d43742fcbdd7176f83157ed460428f816ec88ea`  
		Last Modified: Thu, 09 Oct 2025 00:13:42 GMT  
		Size: 1.1 MB (1103767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34b274805a95433b1c8f997759dcd2a96d0905f8fc331d0e139ec73c3b2674e`  
		Last Modified: Thu, 09 Oct 2025 00:13:43 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json
