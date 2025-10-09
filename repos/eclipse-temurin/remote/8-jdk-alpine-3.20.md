## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:75a94ef9653384a55a1ddc8b665fcb3c94f8177b4dbbcc02fbc792556ddd7006
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cac7c59b5d0acb69468e478a84ea3426cff188d75be2bb8849c2c4807825c3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72288325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911935cb7ca557ff6d26739565bbb91ed73c5278e8bb83c06309a1596a71510d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee812c61135edc8d84ac1eb1e31c69593b8edc5a20b7ee1c05376bf10f496389`  
		Last Modified: Wed, 08 Oct 2025 23:01:33 GMT  
		Size: 16.0 MB (16023412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defd63a4848ee3e5655b4e1c99d4f1c51a2bd5be1526dd457f175062193904d2`  
		Last Modified: Wed, 08 Oct 2025 23:01:37 GMT  
		Size: 52.6 MB (52635424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faceed04915053d250e616b448512e4203e34bfd157994cafb729cd4a8dec0b`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ab9b0dedf3a70ccf6bf9d762b440976f619b32524528cf7a310a3a6aeca9d`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3a433b756ab1ffea523aec6fc50e9ae4e45bf472ba1556377b08d413747dd4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc83384e0ddb810d56b66f7c1a5fdbdc1537a77fc63bb2a26b11c28116331dd0`

```dockerfile
```

-	Layers:
	-	`sha256:83b987a0bf4fb4fa2981a351738d54693eee8fc91a25402c5965eed9c2acf34e`  
		Last Modified: Thu, 09 Oct 2025 00:18:19 GMT  
		Size: 1.1 MB (1093554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823f9f19ac44b03ebb5dec7ac8237d1d0726ff88746187d140ca2c271d344f80`  
		Last Modified: Thu, 09 Oct 2025 00:18:20 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
