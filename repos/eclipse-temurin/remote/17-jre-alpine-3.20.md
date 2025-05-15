## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:c2f377c7a6ff4d1782d7f11f7948b04ff281a4703b1c4dac6892e563ad80a1ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2714f1f57d024b2c215b43ac685df30a4465aa816b71785d9fe101d7e02a4ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66283400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ed01f4046ead1b1806fc6d4e4507fd7cc71ac8375313c151aeec4de4820f2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='38c90337ca2471085f9292d24bec75413b4e56c7826ef25e150a40cc2f727e36';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ede9322895d9de4d43926de688cae026f40e3921603895ecf02696c104a1f76`  
		Last Modified: Wed, 23 Apr 2025 16:31:57 GMT  
		Size: 16.0 MB (16025632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5372158d72e0f344915f3f8f6c995f2d0b156f318aa4e4dbae733f1b9a4f1acb`  
		Last Modified: Wed, 23 Apr 2025 16:31:58 GMT  
		Size: 46.6 MB (46628464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0def7296aa5c013077f3ce647a6a7a2f105a7b67696bc602cfd50a717d06cd7b`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494be1751fc59910a6e1ee96772d1e86ba04b6c37c6b384b2ab38342ec4a43fe`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e03e41b25ae0feb64c256bad6bf8ac571da57dfa9c98c417b6e84370482262ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.2 KB (902230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9064643163b5e060ad1b323749903b7aec425729d9b975900a123a8e8189142e`

```dockerfile
```

-	Layers:
	-	`sha256:61b46b183021d19f34cfe24aded2b2089a876f27e5127a363c2c8482513d470f`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 884.0 KB (883973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab4be738ae50a5b78b05507eb88604a4dffe1077cad951a4f99f8a9b066f7d0`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
