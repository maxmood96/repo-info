## `eclipse-temurin:17-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:9c0fb77dcdb1edc4f3cd2f086f51e5a8447f8c1bb37d3ccef6c13b5398a3b22f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:99cda25b49e057b4668f189feb255fc5277a035183a2c90f0725013e1e2fd72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168146943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1e70ede920c88b78d43d753d80497c41a2d243b876c4f0c2c4d2d129864c6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bbf8607021762a2c0532a8c80d4f29f987c7307e8ff9c8271e94c079c44f22`  
		Last Modified: Wed, 08 Oct 2025 23:32:26 GMT  
		Size: 20.7 MB (20668210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb4845cfb386c2025e9e6126acb47a43cd6da133c1df4d18f17068d2c3f0dc0`  
		Last Modified: Thu, 09 Oct 2025 00:41:50 GMT  
		Size: 143.8 MB (143849267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c47c3fa1a6ccf54135026e652e509acbcb0b8362416c5ffc8c02df9844eb56`  
		Last Modified: Wed, 08 Oct 2025 23:32:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452f822649893acaa973518a9b637c0aa111e439d241fccd2841ccb6715d15ab`  
		Last Modified: Wed, 08 Oct 2025 23:32:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:266f01b124dea63c3be07cac5fa012b992ad1fe52b9ae19fb799282a0593c1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425772d850bf18bccb1bc081e15b784fd2f27d1283b19468de897c324bf18b96`

```dockerfile
```

-	Layers:
	-	`sha256:7cae1d8d55b1aa408ecb7764b77717db69df1e7b66b57e97ac9137b94ce753c1`  
		Last Modified: Thu, 09 Oct 2025 00:13:48 GMT  
		Size: 1.1 MB (1069543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4162c0e73eeca6372d9c5f13dd7be07d8173b63b4293abb1c4eb87b90d5991b4`  
		Last Modified: Thu, 09 Oct 2025 00:13:49 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
