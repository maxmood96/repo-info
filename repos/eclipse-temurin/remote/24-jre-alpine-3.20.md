## `eclipse-temurin:24-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:5ed7fefb8f8bb8561fd325786cadeca9aa25ebd66e94f9dac73fa936365f8faf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5304332dffa8179342f17f184846e67cce3e0955cface2d6565a805caa152cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80672357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f00749d7b04c5f9f8629a4c14e6d10ea5c90a52882603eba7447fc759082cda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0bc8181c7e85d55bba652503db62e60846439f279271d583b740ac70f9f5ae87';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='0f738719d0483d6fe7f08a1371d1c696d68dcfe39f073b4241673f35ffc8d655';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e5c2ea4b1708e262c6bd8c4e3d2e8634ab9d722cad8022f64510292a48eab7`  
		Last Modified: Tue, 25 Mar 2025 21:57:51 GMT  
		Size: 16.0 MB (16025331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209ee7ab98d2a9ecf62dcaec29386176224c57fd081c20c4ab12845224a721c3`  
		Last Modified: Tue, 25 Mar 2025 21:57:54 GMT  
		Size: 61.0 MB (61017721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2d2c2cc6d501247861eafa51b8c1a5bbf0d41c47dff040bd4ea82f59b26d04`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1decf8c3bcdc34136b97face555bf08dd7954f7938599f95e48381994a0a6a`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c85e8adf497e1cb13deb10fb91bf963e4b12b8af38769543a95f4f1e3210d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **912.4 KB (912405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac469c9e563dec0d30ed52061926a751ceb643211edf686becdb24dc0ec74ddb`

```dockerfile
```

-	Layers:
	-	`sha256:ff4006b575d6f24919ec037578f8f05a1cff581fc8e510c31eacf6107ce88152`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 893.4 KB (893394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cabf704e1b7159fee3a0c8fb48f9542b85ba1f9f28a928e47673eca9c9cb917d`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 19.0 KB (19011 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:352065dc833a837f9ca837d886f6e0b22432f49814eb8ec29dfb809183e0c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80289314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331d8e9718b82f42283f561e54ab0a9aad107428bbac474a50e7d240c8a8423c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='0bc8181c7e85d55bba652503db62e60846439f279271d583b740ac70f9f5ae87';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='0f738719d0483d6fe7f08a1371d1c696d68dcfe39f073b4241673f35ffc8d655';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82da281b56f197099e73d78f75a362bf89ef49056d32325c202981f9826865`  
		Last Modified: Tue, 25 Mar 2025 22:05:13 GMT  
		Size: 16.2 MB (16190753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fd778f0f41a4946bc2c05b6de3a58f678e1b93c47bd72b9d86778277800f01`  
		Last Modified: Tue, 25 Mar 2025 22:05:14 GMT  
		Size: 60.0 MB (60004990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9493cea0632e2e630e4334245c55c807d468b0da2d5ad8df51153960f0a195a8`  
		Last Modified: Tue, 25 Mar 2025 22:05:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e3a7de2624bcb0e146a7788500c9c7d7f54d563df0e3023ef75c9363f6e008`  
		Last Modified: Tue, 25 Mar 2025 22:05:12 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:540b092018a67e5f60017ce8f0a230694424903711cf9bd37a4d0b2f3856bb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.9 KB (911927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a01c302cd2b04619b6edf26d9b3fd06aad821a96d7218cddd84a77d0aea6a7`

```dockerfile
```

-	Layers:
	-	`sha256:982c444d08865b4b0ac3d2fda8aa8ff702b570d03b4da78f3c053a88400250bc`  
		Last Modified: Tue, 25 Mar 2025 22:05:12 GMT  
		Size: 892.8 KB (892805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc08a311f2313007b71485073f3c3a5622f280fc6a186e48d572609c4262a73`  
		Last Modified: Tue, 25 Mar 2025 22:05:12 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json
