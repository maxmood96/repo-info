## `eclipse-temurin:25-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:0a1ea0a7ceb4ff5f466582fec653e2893d75357b9252f3c38fc3e456d7293400
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b77425ecd2769712fe5196c8c380dbc1384a4147d90b4a71219d73cb43e28f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75282164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c54ad9efc2b6658330176d63238e85e92d101514a0bcba455659dbe6636baa5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:45 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b31ae810dd4774dce9b4c07a8ea8a254be7a1148dfb3b05ef6dfd8b0826ed7`  
		Last Modified: Mon, 22 Jun 2026 19:58:02 GMT  
		Size: 9.4 MB (9373214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0178f11ccf6d603fccb88123325425f47c455adc6f90e2d1356ca2ddf51ce85`  
		Last Modified: Mon, 22 Jun 2026 19:58:04 GMT  
		Size: 62.1 MB (62118948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb38d5fad5f753833237367685319d168ca3195f7bd69271237a1f740bceeb09`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eecc86c9fde347db9de1c0535f9a1a30fd2dd90fbe349b3ac6be4c8ea49c48e`  
		Last Modified: Mon, 22 Jun 2026 19:58:02 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a17327b3a1992ebb337fb1c65d4f94cef82ecbadac6e332a45ad43d2d3197cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **802.0 KB (801982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675bb862479ab18bf88ff0152c847e162f60801c95331f793e1e3fc1c87fb0e7`

```dockerfile
```

-	Layers:
	-	`sha256:88d766030baca39d5fefe2ed0c809a0669379427fdab3f644d1a1a3c51d5fe8c`  
		Last Modified: Mon, 22 Jun 2026 19:58:02 GMT  
		Size: 782.9 KB (782861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c8003afdaf3a56187b6db5c5c986d624370a2eeef0cc1394a325acb2200bafe`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:bd0462c378f95a44f34b780e919d5220f25efdebc1b2c1edc8436abc306b9efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74556459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244323c1c36bdc99c8a3cd44a17a59a9ff496f16f41b409bff5aa128906c8bd7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:26 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:26 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:58:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adcc9c3236e52fcaaa97a43b4e0d6ea8caf2685f6188623f545259708fc6bb5`  
		Last Modified: Mon, 22 Jun 2026 19:58:43 GMT  
		Size: 9.4 MB (9390884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5927ed6332b8de8ab778c31cd0fb7effe4539aec20663a9b0df5f06105bd0a4d`  
		Last Modified: Mon, 22 Jun 2026 19:58:45 GMT  
		Size: 61.0 MB (61042683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ee13dc868feb60b397358a5ddcda39aa4b197721563124b33ea6532eddf6f7`  
		Last Modified: Mon, 22 Jun 2026 19:58:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac0242ee70d2c450b1e328b90d4932b585f16d74eef7067d883eb27b8414dd8`  
		Last Modified: Mon, 22 Jun 2026 19:58:43 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:466e0d2fcfbc5a380664d08f803813bd25f941179ba919598fef9544f5f11fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.5 KB (801503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca156c624244563f539afceb64ae266762cc0b783d076b7f4bb3a64a3d00572`

```dockerfile
```

-	Layers:
	-	`sha256:a00050f32240f05b8fedfb65415f5015dc4f82451a7e253b62c2d222eb9ccf96`  
		Last Modified: Mon, 22 Jun 2026 19:58:43 GMT  
		Size: 782.3 KB (782272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfa5a4f8a0b86986873601a9fd559c744cf508a87385bcf54a7a11003ff53ce`  
		Last Modified: Mon, 22 Jun 2026 19:58:43 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.in-toto+json
