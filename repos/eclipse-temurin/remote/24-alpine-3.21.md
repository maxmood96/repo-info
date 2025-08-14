## `eclipse-temurin:24-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:1cbf7e660e1280b98ec07de260640b6e9e4d1e711b3ca423c8871758a399fc42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5bcaa55f6d8acdcea860bea9377282c946937de6ab4311b4d7c172174f9f652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114715637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c827a31c0214d9a513e310be233fdd051ace9bc3edd53a7255b81c6400159e81`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d96d7832c798daaafa1df8ffb8ae648082c763cc48b9002dab53d342be24c7`  
		Last Modified: Mon, 04 Aug 2025 21:39:30 GMT  
		Size: 20.9 MB (20942713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9519f753bef633ad881df2f47900d160e10ec43ef806e4571aa19794a363b5`  
		Last Modified: Mon, 04 Aug 2025 21:39:33 GMT  
		Size: 90.1 MB (90132943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c880a00af0a233567e2f61ea2d88e1dda161a1a96d633f0424e53932ff7ed437`  
		Last Modified: Mon, 04 Aug 2025 19:57:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98824a67d305d19102a22819b5e28bbfc7861bd13514a3c6fef67889ec77e`  
		Last Modified: Mon, 04 Aug 2025 19:57:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4d7601b09e2da02cfaaa52a3a87b911dbadefb6622fd7faa84fe81c3c0e70d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1069715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae994a7a0694691ddf7df2c92b636bf317588002a6fdb9196a8361c8fcbc6e53`

```dockerfile
```

-	Layers:
	-	`sha256:d6983e4a8a29436ef03dc8dfce004a3e9907c2ea9bbc4b06cfadb777061be51f`  
		Last Modified: Mon, 04 Aug 2025 21:24:38 GMT  
		Size: 1.0 MB (1049253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e00268dd02ae5cebd94d3aa37a2a2a9dea4c35f3648e8bcb68fb8198f00031`  
		Last Modified: Mon, 04 Aug 2025 21:24:38 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e18b9d9e950ac2a1b14fd6284db78a9dc60e15c74b4fd2fa6023dcae961f964f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114092619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1832cfbf7acaa65d1e6ccc7c3ef422bff16d81998a90df894e52e00ae31f9abf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4921d16d47a336ad3c37c50ee608abc168d7bd9b1ace231696f3bab3de28839e`  
		Last Modified: Mon, 04 Aug 2025 19:31:17 GMT  
		Size: 21.0 MB (20986434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ee6ce9b91f08d3d4a97989797a36d0d43f4880dd6caaed6ee99519df727c88`  
		Last Modified: Mon, 04 Aug 2025 19:39:24 GMT  
		Size: 89.1 MB (89116838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25e3d6a0fb0bc8aebaace813e78c013a92ef409b50e8b03ea90443903a80b34`  
		Last Modified: Mon, 04 Aug 2025 19:39:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e850ecd4b823f9e657f5a4930d51d8b0a785ac9a839ab4f64fa5514faef5af`  
		Last Modified: Mon, 04 Aug 2025 19:39:13 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7efcda9d9fa4460a358fccf150f9f3013725085bee2bb09b2e8a84b1b89895e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1219836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2cc2ccc9f180847deacf4b69d525e5bee6c27f419bd75350f89d54ea02a239`

```dockerfile
```

-	Layers:
	-	`sha256:7c3f40a17145fcd23bfea02725b39735fb6cecec06e17662fbad0634cab34555`  
		Last Modified: Mon, 04 Aug 2025 21:24:42 GMT  
		Size: 1.2 MB (1199252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f236c1aeb466dc15397ce7bc67446ab016d669afd190ac8d2cf9db8ae4209434`  
		Last Modified: Mon, 04 Aug 2025 21:24:43 GMT  
		Size: 20.6 KB (20584 bytes)  
		MIME: application/vnd.in-toto+json
