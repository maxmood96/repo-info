## `eclipse-temurin:17-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:9afe7b233bcecb9561b4c6e467e7d3af6b4f58b59c9c20e600ca36545d252f2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:354adb53bf75934546480514dbd0fec041de9b667d03f7c22da982993460a94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66538441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dbbe8ffaa2dcee5434394f569e6dadc4909cc67cdd57e63929ddead6fa265a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:29 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:29 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fc3becd0350ea4c5cd83a43618feebf8dc234f1a282d1deec1a0f04615346d`  
		Last Modified: Sat, 08 Nov 2025 17:58:43 GMT  
		Size: 16.2 MB (16174520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bd5b47abf113b66566abf1291ea7c79e27f693bcc749036c6de2e6b01c9bf0`  
		Last Modified: Sat, 08 Nov 2025 17:58:44 GMT  
		Size: 46.7 MB (46718945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd8b29d0efaf2db0604c3ef5315727c96d0e0ef88c5a666d15e9794dda2a0ec`  
		Last Modified: Sat, 08 Nov 2025 17:58:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42605608b32dbec8b32c6eceb0f0385781c7f8a78095e3d816d07e99f7b9fa1d`  
		Last Modified: Sat, 08 Nov 2025 17:58:42 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3361452c2751f2c99589d2e0d8ef6e2a7993bec1a8cd24597cef46f22b67381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.7 KB (913718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e02e03140b8c5cb75c887737dcd6923620d2f1952e3e74f29b340b881a9f4`

```dockerfile
```

-	Layers:
	-	`sha256:f47dffa6cf889043b719b9914931e834ccc9b0e1de29a707eb8d17d0676cfd2d`  
		Last Modified: Sat, 08 Nov 2025 17:58:43 GMT  
		Size: 895.5 KB (895494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d9a80450e9af9cda6612b8830ab9973ba59c19fd61fe4553ede9ad2516e4c16`  
		Last Modified: Sat, 08 Nov 2025 17:58:43 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
