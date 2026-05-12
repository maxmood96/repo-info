## `eclipse-temurin:8u492-b09-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:6ecc910f9ab3ff5a9ea332cbb7f8d1044407ae1d8e5c02a8b30301ea4c4d0ac6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u492-b09-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f68c26840795df7eb051870b02556334f31c03865bb915a58e6659fc29fdf1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62417469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99f064ef04ab2417476d51a291cd0cdf34a96828e9f0776a334bda18ee4b54e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='82b74dc9042ce6735624a1ca9585e6a43c44f0f6093a7f2088b0a622f304d62c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 21:26:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3286d2a7888d2fcc671a2f0ef8645cee5e1205ef9b8c23542017408cae6e14e`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 16.3 MB (16337362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4942539dc488cd5db022b888d33e145ecf62f7c34693a3042b5b633f718f89`  
		Last Modified: Tue, 12 May 2026 21:26:17 GMT  
		Size: 42.3 MB (42269329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305012812e9654bad510ae6f4f3063a8884b712d1e8bf9c158cd74b34b69baef`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae88fe1c554a4391e6b2012965f3b8302b34a11a349d1e11a2e7c298b923ff8`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u492-b09-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e55118a4b81ee64e96fe49a3a21c4c3c4c1f688be3522954a89382d71b2b9135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.5 KB (946533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe564c5acf8711aeffecb1f667ddd69c029a2bc3fbb4ec8ac1eb80480db59dd`

```dockerfile
```

-	Layers:
	-	`sha256:f69957a3bdb8e323e1900ade7a615094c350eb20099d816006d47c707730a90f`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 928.3 KB (928346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054391a2d0defe99db76efd23061edd02fbbdd9a7def3f48ac7fd30f85184181`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
