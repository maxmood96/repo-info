## `eclipse-temurin:8u462-b08-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:4308793dd75270508f344e2f8ed160f1906f86e15c34853fdea331674e992d44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3fe118804109b60d6416b0fde6e7ebcd8b04816735668151962fac72e210b63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72437997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5fc8ce6e078e30135a4f791b54d92848b5f4e9c30bb62d2a3639644303fbec`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:6783bac38599214da1a397bd44bff07603d33ab5e424bf530aef419d51eb3b06`  
		Last Modified: Mon, 04 Aug 2025 19:11:01 GMT  
		Size: 16.2 MB (16162633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96475f84a9b714761a5e5c8ad458afd8e49387b873357b6ce7535bd89e8032`  
		Last Modified: Mon, 04 Aug 2025 19:11:07 GMT  
		Size: 52.6 MB (52635362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec3d96b91e4e9b7e856fe23b9e9c7a2c808ce171f908f8965024159caab669`  
		Last Modified: Mon, 04 Aug 2025 19:10:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f204ccabee0d752cac12a3aa1ffaa0435c06f364a224cca0bc5ec6c5ff788c23`  
		Last Modified: Mon, 04 Aug 2025 19:10:57 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1f13b3f2e9043ae77dca6642dd67a9b5f34c2e13074997b1d4511f3eee7fd8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454f262688a7b431a32760e9b4ab111464ffe8e5c1be333cdb309fea8fb7a9f`

```dockerfile
```

-	Layers:
	-	`sha256:c487231eb6f33f9e0a86e3a94cf07dc24b5796c6c76a27f7514b3278ae64e51e`  
		Last Modified: Mon, 04 Aug 2025 21:27:52 GMT  
		Size: 1.1 MB (1098192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b76d81b3d752f1372606475b944c5d6af4ada42024171882fedb133096e94a`  
		Last Modified: Mon, 04 Aug 2025 21:27:53 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
