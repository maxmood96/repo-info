## `eclipse-temurin:21-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:0e0546003ca7a6c9374c556a620bd7d473491f68e583f5a805eda70153160049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6ff627fde7cdc96b1eaec43e349638053831ff594ba7e4d434eea7551c7a1ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72940584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3db396b4a15ef55ead64e1de0b2808916bc66a1d30e18a7e3d8bc568418aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfe9407f97c5a3827be879ab9af74bfb17d46f835370cffead35e0378d78bb`  
		Last Modified: Mon, 04 Aug 2025 21:23:32 GMT  
		Size: 16.2 MB (16162674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229ea679746a032ef8454501b6c2a2fb9fde93f7b6cda28f004dca291ed51a6d`  
		Last Modified: Mon, 04 Aug 2025 21:23:32 GMT  
		Size: 53.1 MB (53137932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90e240ccfd2dd071291ab367adf045fb6cc8cf23c252ab903fe0fb3f9f4d02`  
		Last Modified: Mon, 04 Aug 2025 21:23:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f12107c687d793a6d868c79d26bf94594fb9245d01fc0b2a787e481082f3eed`  
		Last Modified: Mon, 04 Aug 2025 21:23:31 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:af258715e124649897eb89f9b30b2f646e876352497fe2928dc3475ed4ea3583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.4 KB (914429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0563d704cb829fa7ea44b74682953a99c45e6e8a99f2310d14b867c1ece6022`

```dockerfile
```

-	Layers:
	-	`sha256:78903d664f5236a9d4442a531f65cb0c107172e17ba5bfd8256a4235a7df8d2d`  
		Last Modified: Mon, 04 Aug 2025 21:22:16 GMT  
		Size: 895.4 KB (895373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e7a183e30dc3fc7c00080914d9590b6827e63bc5dc3ba529200446c5293983`  
		Last Modified: Mon, 04 Aug 2025 21:22:17 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:434fd3380f9bb303a3965c5017bb7835db2990bdde9b08bc400fb8e5ce0bd3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72324057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daea980d60c4d8d6a2629790bfb3340e3e4a18e4eb0a58f6969f0de04312f738`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe7a243e393b0e786543dd9f5baddfc1b85c7bef5e769f84ae7021986cd2b05`  
		Last Modified: Mon, 04 Aug 2025 19:35:25 GMT  
		Size: 16.1 MB (16135229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69424351a2d65a677d1add3d945be7d0ef7fb6f17877e4e8edc3723a8f3a3961`  
		Last Modified: Mon, 04 Aug 2025 19:35:29 GMT  
		Size: 52.2 MB (52199484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a06c43c22cfc83b03851a3756ddda62961748985cd97f5b6a65c03a679c5fea`  
		Last Modified: Mon, 04 Aug 2025 19:35:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a8a02826550260391b4b424cd4a94f1e01da9b3cfc93efd7918888b245c0c`  
		Last Modified: Mon, 04 Aug 2025 19:35:22 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5fb31d9bf1ddeae030616ef13d037bc50f3fe69bc267f84ce25e223499dc5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.0 KB (913953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d718ae8dc85fdd446213101075f1ac7f6b3bf20c7a01acf26627f57118a765`

```dockerfile
```

-	Layers:
	-	`sha256:12a6f8d764b9bc92e02a957df2e3d2a1664dcaf3a0993d2e7bbbfa33d8a18442`  
		Last Modified: Mon, 04 Aug 2025 21:22:21 GMT  
		Size: 894.8 KB (894787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9594aaa4d2e08437c8e1688f5a7806fec3d73fe6a5f24895abfdaecc93d8c678`  
		Last Modified: Mon, 04 Aug 2025 21:22:22 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json
