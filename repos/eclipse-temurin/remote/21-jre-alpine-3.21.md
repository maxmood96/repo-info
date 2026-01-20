## `eclipse-temurin:21-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:7f1d6c1ec4b79f07dcad820c7952d526e7ae6ce96ef5b7df506a446c3c924818
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:17f382e2c628199a71d3f84b18de4a5adb3e644ee8675f48b17f60f252334131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72988581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabbf1ea476e2c8d37900379e97fb578555bc0ca0e0bfbafdbf49408242ed036`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:36 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6625eac0c56afe980468268c82e58541814b3f353faae75b36aa85b733b9f6`  
		Last Modified: Wed, 07 Jan 2026 19:32:02 GMT  
		Size: 16.2 MB (16174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a857bcc1a1505748a54fef25bb81f303468a26d3de127b6b0044b1ffde6275a`  
		Last Modified: Sat, 08 Nov 2025 17:59:51 GMT  
		Size: 53.2 MB (53169034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a75c308165465141d861c1b7f7ec799b18fc84d5d8b87396dc29c3aa4894ff`  
		Last Modified: Sat, 08 Nov 2025 17:59:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d1cf1d02f064d13d647e4816e26b17678a634769ec583b4eb29d5a68d415f7`  
		Last Modified: Wed, 07 Jan 2026 18:56:48 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cd4c25745f46600fdbc15c116e09dd4f7fed97bde364ca5e1c22a0d6b69faf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.0 KB (917015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca065e85c4b32aa6d23b389ad2baee91929e02d17ee5aa14bf9dbf6bb8e8177`

```dockerfile
```

-	Layers:
	-	`sha256:9071db4ff600f7c42c82907423be096d7d9b0fd294f464479446bd3f0a746e2f`  
		Last Modified: Mon, 12 Jan 2026 14:21:40 GMT  
		Size: 898.0 KB (897990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1654022c4c909e74c8bfd0e43c40972b604bfce396ed55986cbc51102bfa8669`  
		Last Modified: Mon, 12 Jan 2026 14:21:39 GMT  
		Size: 19.0 KB (19025 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:746df0d3043b1ac73fc8b67cca8dbb9e89c20abdd99082c594e7f25e16c0ecca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72358083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03a08fed48e62376ef63419b40940746f6149e920d1005c888edd0c6f67b08b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:58 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f2afbabc707ea40256e108c30aa092c8fc89e070654609e6d9f4f42bc128f`  
		Last Modified: Thu, 08 Jan 2026 11:04:19 GMT  
		Size: 16.1 MB (16136845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086326885038d57b26faf7c1daebb024a8f730e9d49f8284177cf9b4d4a8f5b0`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 52.2 MB (52226480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae04221b2e584a4e0a67d1d535900a5eb9c049d2a2051d0b66d4d2af68f77ac`  
		Last Modified: Wed, 07 Jan 2026 18:56:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ada9f9a574189d8e20095927344850458cfffc58029c0e6d5d292c6f568c419`  
		Last Modified: Wed, 07 Jan 2026 18:56:45 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5b3877bb260738bfff21d42553dc4523a24df5c852e4f69e4fdc3752e73847c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 KB (916539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0055452fde8dc279ce2df1d80f54ee4784bda7f40521db81c68b258b5442fc`

```dockerfile
```

-	Layers:
	-	`sha256:e220f9205123aac9e333f6a32cb095587aca4c764910d55f5e3d322935cb2d9a`  
		Last Modified: Sat, 08 Nov 2025 17:59:13 GMT  
		Size: 897.4 KB (897404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc1d714d7d78fb04a9939354b0792175015121f689ff15a44fc6df8e2d15a2a`  
		Last Modified: Sat, 08 Nov 2025 17:59:12 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json
