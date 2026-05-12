## `eclipse-temurin:8-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:df7894b2bbe772d879764db245ad077710dadae06734241da56cc9ff5e8e2444
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f66db7d9f5f66ceabc54ae16e1184ec59d6f599e0982d5acc98d1480c3b10e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72949454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c42a23eac0eab8342cd1ada2bc882f20b057284b96e7c719dade7d8a98a45a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:25:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:25:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b1b38da7734651dcc336b835bf0c62191decf4ec46beaa04577396e47ed397`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 16.2 MB (16219865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad3d014e6ef3a9d9337bc755d74def06ada02577f425feb83d66aa49deb5f9a`  
		Last Modified: Tue, 12 May 2026 21:25:47 GMT  
		Size: 53.1 MB (53080102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b985bfaada83106d040f27f566355ce8ef04613d136adb046487811950194b`  
		Last Modified: Tue, 12 May 2026 21:25:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2083585ec48a6056deb64dbbdc05a22c642e38d4714417303a899ef4b62f4636`  
		Last Modified: Tue, 12 May 2026 21:25:40 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6fe6444320b376440a36263528839eeecc07678a276bb4b0457ef7567cc65b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e56f51f4e8f35253ce5e353446c93829ded60573973254bd3b403693a2ed5e`

```dockerfile
```

-	Layers:
	-	`sha256:d5b41d16d54d5beab8f351a5ffb09729361b72e09e000bbfe6f4f980772fcb29`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 1.1 MB (1100761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099d0ebfbfe39322e74ca8055c42ffe72c44f32b4f64b5a68edbd09b4d61bb9c`  
		Last Modified: Tue, 12 May 2026 21:25:40 GMT  
		Size: 18.7 KB (18710 bytes)  
		MIME: application/vnd.in-toto+json
