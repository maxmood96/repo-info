## `eclipse-temurin:25_36-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:9723f527a9d58c6675859fed206b8d41e3dc6bd0a894d4d6e21bef214092d045
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25_36-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a231630dd5688281a46068769b91e33460f2c47db2107b1b3f271dadf697e902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74999491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33983c0f7bdf277dd867d07f46f3fb8159ebbc31a8b9f9e58009a085893128fe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e88496ca31d2e0a0cdeeba385ab4ea668bbb53a03018f30c8933e97f4f9fda47';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='aa5160aa130f0f0b4379fc62a0d5198c065815224e01318272864e56f260de34';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5fa704ef5864fad740294db29f7c0d7d6fdd76cbd3360939ec9a6be3a03989`  
		Last Modified: Wed, 08 Oct 2025 23:38:21 GMT  
		Size: 9.4 MB (9392778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7ba6f6eb539b03ac2bc0340f10734e81a4bdccb8204676198a082de9f8e98`  
		Last Modified: Wed, 08 Oct 2025 23:38:30 GMT  
		Size: 62.0 MB (61961736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eedabf43f24200a38721272981bbb1335e42d7177553ca14e3fc8829ede1cd`  
		Last Modified: Wed, 08 Oct 2025 23:38:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2815e65759c5c662c69ef7835af46000506e6562e5485dc2e31daca13a8dfb`  
		Last Modified: Wed, 08 Oct 2025 23:38:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:900148d5f1b235fb7f9303018cd41b2a8084776447585310d2d31bc65eee3528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **818.1 KB (818137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59d5370238644f111e2ddad1290793e3e9871941d6a96856e8083808b34a446`

```dockerfile
```

-	Layers:
	-	`sha256:b57a9d984273913898393490cf5b4c8a723b8971f3e7965347eafb6cdd6d4aa7`  
		Last Modified: Thu, 09 Oct 2025 00:17:35 GMT  
		Size: 799.0 KB (799017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84832cfaef06fccc998ad8132355f50583c6abbbd4dd4c585de8fc856b034bad`  
		Last Modified: Thu, 09 Oct 2025 00:17:36 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25_36-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:da9739e52f4b38435cf20ecbfd17cfee9efdc6704b56e183b7437bfad2386725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74276473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c3bb91309eaee50890847ab3dce686e037300085df3c70a66b05e216ca76fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e88496ca31d2e0a0cdeeba385ab4ea668bbb53a03018f30c8933e97f4f9fda47';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='aa5160aa130f0f0b4379fc62a0d5198c065815224e01318272864e56f260de34';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66052413beeacba9959cda7b15638340f4aaa74213f1ab6392849c98ef34c2d4`  
		Last Modified: Wed, 08 Oct 2025 21:49:06 GMT  
		Size: 9.4 MB (9412773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439a94f08d84f60b9b4701026ed3240cfcd918edf50f026be4e177b4165c688b`  
		Last Modified: Wed, 08 Oct 2025 21:49:28 GMT  
		Size: 60.9 MB (60868940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cdf19f3df290c2d6523c03ef06ef5b6718af2ae30fc69c0149717fa3bffab6`  
		Last Modified: Wed, 08 Oct 2025 21:49:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d38fffbecc3524e0d7ff53ec5c500b84924fd6e1322a57be96543c1e2f33d8`  
		Last Modified: Wed, 08 Oct 2025 21:49:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3eed80db1a59c39b2d7a2ef95935fa81c0cc46c3e0a5495c34349a90767d51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.7 KB (817658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffdea32c82f97d5ce6ece75fead4f1111ca5c3ea22d729b0af5157b0dc749a8`

```dockerfile
```

-	Layers:
	-	`sha256:ee6be2e057bdb25be337b8a61982e07a8b3e91931ba2806916260dd91d4116e8`  
		Last Modified: Thu, 09 Oct 2025 00:17:39 GMT  
		Size: 798.4 KB (798428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d818bafee18a7ada84dedfd6f5250a0f938a4410c55964800bea2e4628f9cec`  
		Last Modified: Thu, 09 Oct 2025 00:17:40 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
