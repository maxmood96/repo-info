## `eclipse-temurin:25-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:28db6fdf60e38945e43d840c0333aeaec66c15943070104f7586fd3c9d1665b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cdd967aa55f1d0175ebe57245e4450292e6e6dd185dce73f93580598934128aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75362585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcf41d8b2a9b6d20f8fec0f7b0bf4a5c62ca877e6e8f3995fd7798ef43ab026`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:44 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:44 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739e8e642ebd599428113cb43cee9976efa2397e34005467b539f79132805b73`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 9.4 MB (9394417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5487bef4f38569166492c4252f8271c83cce645ad1303f91774cfc5cc137e5`  
		Last Modified: Mon, 22 Jun 2026 19:58:03 GMT  
		Size: 62.1 MB (62121340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb38d5fad5f753833237367685319d168ca3195f7bd69271237a1f740bceeb09`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcdc018fdaaf0ba22d47f939720896737cf7ae0a72c11cb129a7a7eef27cbe2`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:791157c7162af1598c1471fdc404c8227aedc7a6096775480c6513087fb2ea69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.6 KB (804603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6037bb1c1a23b4763136762fb0ab99def4a860679fa1a5ad8761ba130df88`

```dockerfile
```

-	Layers:
	-	`sha256:ccc291cde25f5f5d18163a37a1bd2d41b85ac724e06698989ec3c5bb1c088290`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 784.8 KB (784810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2103903e18a995c151f9932f905f1d648e9168c888731e21d31eb026f73aa69`  
		Last Modified: Mon, 22 Jun 2026 19:58:01 GMT  
		Size: 19.8 KB (19793 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1193e3ec5639a22b20739276c5bd9cce7665606bc4521336e334bb6d7daf79dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74655535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fc2a7faccb33105c845cad9fad6903564a787f71097a57fd15a8841fb80119`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:14 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:58:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='48aa0908d9f4d501c1070ebbc8a4da93ca1f066c41ff2e34a22a34dd3ca2dac1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='ad202c8f8b216800ed0d6581130f92e5680b685ba394ba38e62e7605c3fd9494';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b71626c8a0ebae23ec9a352725bcb478bf4acaad954f4a7fcbe48c494dec569`  
		Last Modified: Mon, 22 Jun 2026 19:58:32 GMT  
		Size: 9.4 MB (9424319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0d2d57410157a9dfd5b5a601704040069e9a998acd65c53377e437c33ae57e`  
		Last Modified: Mon, 22 Jun 2026 19:58:33 GMT  
		Size: 61.0 MB (61046950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8cfecc0c6b2469085b1c841ab59aa1aaf34a0212bef115ae0ebd3e2227d8f`  
		Last Modified: Mon, 22 Jun 2026 19:58:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec18017b4ce80f51abc295f6ee09f3889bc1931e06b55ea539498d229cf5c666`  
		Last Modified: Mon, 22 Jun 2026 19:58:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bc358e7898fa22bf3fcf7477682b2a23ac0499973fe3e0bcd5603b2cca1824c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **803.5 KB (803522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecca038e8185e2f5a2f97efdbbdd8028cc98f280da99b7c149394b304b828008`

```dockerfile
```

-	Layers:
	-	`sha256:cd9d9dc57549513c0a9d4d3fee373c93d952a9f3f5cbf3cfe7811831a90e34b9`  
		Last Modified: Mon, 22 Jun 2026 19:58:31 GMT  
		Size: 783.6 KB (783595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054765018fcb7fec818692770b1d17310d9d09160d448160af8cd45d3a61aa25`  
		Last Modified: Mon, 22 Jun 2026 19:58:31 GMT  
		Size: 19.9 KB (19927 bytes)  
		MIME: application/vnd.in-toto+json
