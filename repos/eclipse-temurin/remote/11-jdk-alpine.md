## `eclipse-temurin:11-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:9907fe14da2b77adfcc98e7eaca3367df723155e9a8a9726a1224912187d1e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1f0a1776f7bcbf45443c479fdc4075b753b1786d437fcb6af3e8558d2aed0da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160936155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30f92cfeca85b64151c6330e819dc0f42e7b7e2e5f636623e57f17b827a77bf`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:5fc9e5a155a7ff06c0190ea62107ab1a927e87f603ebbf7a293a0f96aa156ee7`  
		Last Modified: Wed, 08 Oct 2025 23:01:38 GMT  
		Size: 16.3 MB (16289659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7cadbd3f978eaee4ce9a81527bb2dced7d116e33e7e96e77af514781073ee`  
		Last Modified: Wed, 08 Oct 2025 23:39:17 GMT  
		Size: 140.8 MB (140841635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80d87e1e391e254ecece5c43911c68edfddd2bd6a7582367fda36de120a1f7`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e292129e0fa0f3fd5d4c68c90a9ac89b092e4768cf7bdef779596a5f99c513`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f90feefaa3e1d9c02873c059d6483b59dc1e4ddff0252f1357b50c9081284c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1022247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825a326882e24b4d458fc060f7eacfccacf537ede160002ced7d4b3d76b96e54`

```dockerfile
```

-	Layers:
	-	`sha256:fef4455fd54831e037a9c855afba869b78cddcf8dca4937bdf269dc44f952da7`  
		Last Modified: Thu, 09 Oct 2025 00:12:19 GMT  
		Size: 1.0 MB (1002038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6418e739f274a66c062ed5c27db8971cf88e6981e6b6cd2bdcce9191252fcd2`  
		Last Modified: Thu, 09 Oct 2025 00:12:20 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.in-toto+json
