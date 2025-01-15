## `eclipse-temurin:8u432-b06-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:6af5651ab87b8cac585e45f7887a2bfdcf42ca6f1cf63fb32f7d51c496963951
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u432-b06-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:87ee49746af07c9c6b5aabb63c25d294feb83769941fd2deadc0f50f3ffdd3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61469715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b2bd7144497955eaa3824736caaa3e6940e97ab86774fb43c9d2e7446eb404`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d1fccd1898ea4bb145d009cd29080b91ccaf30179d18da02360e29b1136bd7`  
		Last Modified: Tue, 14 Jan 2025 20:54:33 GMT  
		Size: 16.0 MB (16022324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd116e3328fb199865e459caecc1d80cf5c9d9be850fea2f0b2db32b5c5edd69`  
		Last Modified: Tue, 14 Jan 2025 21:06:28 GMT  
		Size: 41.8 MB (41818722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbd3739bbb55be440a15c3472aedee8bb625b8d87639545952759deb0d3ad1`  
		Last Modified: Tue, 14 Jan 2025 21:05:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8f39bcefc58333ef8d2982d6c772d437202f0ed61eee6cdeb584b75f877372`  
		Last Modified: Wed, 08 Jan 2025 18:14:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5582b9a0651ab71d712ffd23fbc0f082c9ef167dbee97205cbdd79c82659c39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.9 KB (932939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb3e1d4fead735cca90190f11c897c8fe789ad85a112d66c80287787182ec4b`

```dockerfile
```

-	Layers:
	-	`sha256:1b42ef58e2583f320506cac121c4ea815aa5b7029bee99827d0222d5cdc61bf5`  
		Last Modified: Wed, 08 Jan 2025 18:14:15 GMT  
		Size: 914.7 KB (914688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3d6a2c13ccfe63c56e3905429f1cbaf5fb047f0def5002fda74ebab8d37ebd`  
		Last Modified: Wed, 08 Jan 2025 18:14:15 GMT  
		Size: 18.3 KB (18251 bytes)  
		MIME: application/vnd.in-toto+json
