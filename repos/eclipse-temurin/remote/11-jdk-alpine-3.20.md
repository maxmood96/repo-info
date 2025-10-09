## `eclipse-temurin:11-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:d489b1ea92171ebc502ab34133c0d955e0ccf4d3370ef5941b4a72ad3a54c35a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:54bbb70a32fa8754e673f826540a769f1379a21281216c467b013dc96ff293cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160494486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d806ebeaab237438e741f44f37bf0e45ead79c0950fc4cf436e51894a6599faf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee812c61135edc8d84ac1eb1e31c69593b8edc5a20b7ee1c05376bf10f496389`  
		Last Modified: Wed, 08 Oct 2025 23:01:33 GMT  
		Size: 16.0 MB (16023412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85591cc6df739bce5336c773f25423038dc84dc3ec455962adab1eafa561f4`  
		Last Modified: Thu, 09 Oct 2025 00:13:07 GMT  
		Size: 140.8 MB (140841609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80d87e1e391e254ecece5c43911c68edfddd2bd6a7582367fda36de120a1f7`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bdd4fd061488ee64b0cbdf528189bbaeb832ab8ac062395d9dbc574b5cec95`  
		Last Modified: Wed, 08 Oct 2025 23:36:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dcb1cc750bfc409618579913045ef3bdcc846c643a8f183b243299e62518fa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1011447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea6bdfe134717bcb3db2c6976150efeaec8934477ca165cb05b2ce3da8bfb93`

```dockerfile
```

-	Layers:
	-	`sha256:8639c4b1c20c3ed6c37f2969dc4a4f46bdf637d52ff775a4b1a339607a0f4a4a`  
		Last Modified: Thu, 09 Oct 2025 00:12:24 GMT  
		Size: 992.2 KB (992234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d1e3f83a6a1fb617155101e4246c6d1a271c1a0d26895aaefc07305a137a9d`  
		Last Modified: Thu, 09 Oct 2025 00:12:25 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
