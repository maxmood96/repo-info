## `eclipse-temurin:11-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:578a4f84efdb457370b74e9558877935680d72bdb8302e05b51ba58254842146
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a41d6a7257639fe3f673ee1a1c4c3dc5544b9e3378f893a5ed37b329b43cac75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63239433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951550e45548207424ef512e3d7ffd7a3ae7c90bade44f988975e7a7142422d4`
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
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5de5d17c737554ad3ba3b896679bb9af4d6c5dfe3b707931cc8b78f538a3f886';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:ae6980707d01bb405f6601f5675b8344636c73838740fd958a736f26fb6ae1c6`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 16.0 MB (16025871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b89da1b8ac1c90a030146b452e2c512f5227744d1904f0a63bf2a615883e6fe`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 43.6 MB (43584258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adde572e7b0251c5f57d01ac0648d15589708084645280b8ace8863c431da61b`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a1ff00d0fe30518bd8b61e50985503ea5afc05f511e24eaf54857b67dc4236`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:33fc0e3df27eae2aa9964a1a4f657dec6d4b7be868480b4a3f6b9d56478dec17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.7 KB (914719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55a52e40f8d725b25b17386baca709fb0c667f89b7b6d2ca1ae72be9905cf65`

```dockerfile
```

-	Layers:
	-	`sha256:7ae38fe61e0f05882d4669eaaf1e842e7ab4bfe767d0ebfe87406e54a42d2545`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 896.5 KB (896462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f19c099fa3c2ae1f4793e1a8122573dcc9992ad1990e892683e27ebf38c944`  
		Last Modified: Wed, 23 Apr 2025 16:31:27 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
