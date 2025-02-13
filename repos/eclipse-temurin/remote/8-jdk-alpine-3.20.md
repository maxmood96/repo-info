## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:fcec5531d50c4c6cb9a80313be245569df842067d8d495918bf66dff2a8f9eb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f74e81bbf26e7b90c090f729b9893421669fbc5d4aae7d97f356843cfc5a23ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72280591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401389c6a9a1c8d3e64e46f70ba2f9e4f4775655cb848540d69a50f80b57e4fe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9fcb96380b25c1d1caec65b7606c387716a7ae51caf359f5f3ff0dcca40f231f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af472d1a5a0cb24ab51e4442b5bafaca69b10f8acd4df86d8324b0bbf2db1df`  
		Last Modified: Mon, 10 Feb 2025 15:53:50 GMT  
		Size: 16.0 MB (16022411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcac2d62290c30b404dd4493dc497010979cc7c5dc1b29636fc4872bc44c3a4`  
		Last Modified: Mon, 10 Feb 2025 15:53:59 GMT  
		Size: 52.6 MB (52629490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a19eb24160c27520dc6f61158e896431c5d7d99025373f64ad441061068a68e`  
		Last Modified: Mon, 10 Feb 2025 15:53:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d733c716947a83c5bc715514afb7e7795756486a1c76dcb66cadc192c9634c`  
		Last Modified: Fri, 31 Jan 2025 01:29:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fc194868646c0f76f798f733d652fac0088a4fdc99f8313fba2e4f7a671fdf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1107420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beac61f3536a4c0889df74ed72fce44d78280921e79a304d749f14b8e5be6f34`

```dockerfile
```

-	Layers:
	-	`sha256:0652adb4f045e2034cc42c56c5c47c4570fa1a211fc1a6969be2927ba63983e1`  
		Last Modified: Fri, 31 Jan 2025 01:29:27 GMT  
		Size: 1.1 MB (1088666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd72d5ff72129e20659be98883c470c5b34454ce9b4347b14ff0a0c30651c73`  
		Last Modified: Fri, 31 Jan 2025 01:29:27 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
