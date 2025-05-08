## `eclipse-temurin:8u452-b09-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:cf90d0de6e8202281c4a946865bcc920eea4fb13fc0a37023ec6d63c37c4e1c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u452-b09-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:578721c29ca04cae56ad3e5889b90ebea8d98a00a43f7ad228b78a98fad21c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72443067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08ad16d6c3d2d5fe2fa195fcb8d5d8ea2faf4e3134897bcac5e28150739ddf8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='be8abae7586c328ceb3252aefed9e51c29be91616968c0130b41e7e57c846f0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7141be485741d41116a845b669643de63ccceb87c3be707c0a7eaa7f5ccf8f0`  
		Last Modified: Thu, 08 May 2025 17:18:28 GMT  
		Size: 16.2 MB (16176532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22b184abfb23338db1ce2eec5f2b1c5299eec68ec533ba9f0c96eb50f94d86`  
		Last Modified: Thu, 08 May 2025 17:18:35 GMT  
		Size: 52.6 MB (52621858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3726fa4c4e4f7f6fac67f7e4a3b9f88a7697235d9144aea259a488250ea6a4`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267111b8758c00ce54358fe646f25d46e043fc0ee6173035ede38ede1c1aaddb`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u452-b09-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:241096ddccc038ae10d29f5bccb56b373834bb49cf8c32e3940136964174f0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cb5f84d818d18665b1dce57d44f6844ebe780b341ad6781fad930928803d48`

```dockerfile
```

-	Layers:
	-	`sha256:35c9bb4493ca46fb601164dcfb0833c8343cc49572d450aef584c9703482c789`  
		Last Modified: Mon, 28 Apr 2025 20:07:38 GMT  
		Size: 1.1 MB (1097177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37144094a48b3d449ce49908c1f40ccc2ad6d0db98ba4a47b22120f36d89bc4c`  
		Last Modified: Mon, 28 Apr 2025 20:07:38 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
