## `eclipse-temurin:8-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:55fa30bff6b04913f331f966e6e1ffa0a164523c2002d4a9f9a2a06c77ec3769
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:518ecdc7297960fa966a4fbe49d33e6d4257f352e0bd369b5e8b4949cd2c9b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62932080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e8ea3888747acb275604c0237cf22c6c4fef9cac613aef8bf8e74e501f2655`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:31 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 22 Jun 2026 19:56:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='82b74dc9042ce6735624a1ca9585e6a43c44f0f6093a7f2088b0a622f304d62c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Jun 2026 19:56:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37871e84e40af454a54b03c545cfa7a05d360b1cf8bdc2b2faef8da08b487358`  
		Last Modified: Mon, 22 Jun 2026 19:56:45 GMT  
		Size: 16.8 MB (16815714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56739af10fac7c15ef0298116718f18348063174e6e3b0ee36c8d07ffcd7337`  
		Last Modified: Mon, 22 Jun 2026 19:56:46 GMT  
		Size: 42.3 MB (42269356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f736371aa6115da269a7968295b3cb37e0ce6a9d62ac341b9d7e118132e51b`  
		Last Modified: Mon, 22 Jun 2026 19:56:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fb47f6c197a7941ac8f592b95605f2c809c14225ac31e3416edbf972d822be`  
		Last Modified: Mon, 22 Jun 2026 19:56:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:23810a68fa613018cfc4762011a6dbef5428ca22c2731608ac0710765d5154b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **935.3 KB (935328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727d9736283c96a9ba97d3735ce29fe2587c2990dfc44212c86760ba47c15672`

```dockerfile
```

-	Layers:
	-	`sha256:3f756dec6562c3e63cf5b768175b27900687ce65dc76ef30f95a8e0fb62ad216`  
		Last Modified: Mon, 22 Jun 2026 19:56:44 GMT  
		Size: 916.5 KB (916469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efc74fc8f9624a516723d4ceb39bfec7ebb6514f14a14fb0f4442e7e9ccc0c42`  
		Last Modified: Mon, 22 Jun 2026 19:56:44 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
