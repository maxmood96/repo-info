## `eclipse-temurin:8-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:52b7a6ca9b8c91d25aead177206b64f5b96d235caddd6b844c243ed07ab15ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9c632bf9a1af279c815ec8621392fb55db8b93137079d70a4008c3239ded8d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62348982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc1992785271386c5dd51e5ed745a43f19e013f02c089058a54e6d25cebfd89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:33 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 22 Jun 2026 19:56:36 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='82b74dc9042ce6735624a1ca9585e6a43c44f0f6093a7f2088b0a622f304d62c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Jun 2026 19:56:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbea586607fa0682cd2d4c3b94934cecd16a10108970555ec911f04ae2e4a68`  
		Last Modified: Mon, 22 Jun 2026 19:56:47 GMT  
		Size: 16.3 MB (16289454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12951ff47d9096c206d41e76d37adbf130c4d1886f2d179d417c89966b260976`  
		Last Modified: Mon, 22 Jun 2026 19:56:47 GMT  
		Size: 42.3 MB (42269344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e95dcb681cea273afa452d1321e56f5f3112511723fb8df867cc3ece51493a5`  
		Last Modified: Mon, 22 Jun 2026 19:56:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a502f5dac97114ac4c3bda56b65f55dd9b6a5be950d222bcd55cb2049cda37`  
		Last Modified: Mon, 22 Jun 2026 19:56:46 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dd5e1163d43966373cd3589fb150b0b362c08f0cb489fbc233b25da97ef3258e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.6 KB (929645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae693c06dda78742f54ac98f11eb5884c6efd5594acdcba7eb57437eeb4e052`

```dockerfile
```

-	Layers:
	-	`sha256:565bd7923d3bdc7cb8d2c821563f0d2728d5cfc3a96fcbfd79b795689d624396`  
		Last Modified: Mon, 22 Jun 2026 19:56:46 GMT  
		Size: 911.5 KB (911459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3468b2b9bb82b28442edfcf79d0b4e0ea5a01c70a6679759f5d1e1a356f29fe0`  
		Last Modified: Mon, 22 Jun 2026 19:56:45 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json
