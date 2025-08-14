## `eclipse-temurin:8u462-b08-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:5505321ea7b9f19687d2f136a483c3829e37d52c3f6757eb3278125c54af4483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6bba4413d15224145db3cb0b4bf46922f1433277de41d63c184391f87ce9ed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72717656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b7a0584a58a25e3b0a04ea9263c3afdc886ab17ba6daba91a22a395cd473e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203d7f2ad91296c29189d9e5c0619b490cb71fe963cad10b53ec84f88ca971d`  
		Last Modified: Mon, 04 Aug 2025 19:10:43 GMT  
		Size: 16.3 MB (16280141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b884ab8379b7e3f3639c2a35bac4787823a7d7bbcb15fec9531a4e72f8043f69`  
		Last Modified: Mon, 04 Aug 2025 19:10:52 GMT  
		Size: 52.6 MB (52635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d301459c24bef03fac78826eaca6eef9060db4208be33da132df14690b45d88`  
		Last Modified: Mon, 04 Aug 2025 19:10:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa4fd338b932d98deda035704b29a8991d4ce5a7b04a7e3eaac2fe5e23925f1`  
		Last Modified: Mon, 04 Aug 2025 19:10:41 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cfe70839eaacc41b7fd21c286d257dea391fce5f5c9e7b0273946192b847e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1120487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9152d91defca2eab80a63d6bdaea6203f43fcf447c09d0526fc6ff3dde6af010`

```dockerfile
```

-	Layers:
	-	`sha256:dca034b42644b301c32b26863072f26b58570b7c98f572aa09b4163f1d3b282c`  
		Last Modified: Mon, 04 Aug 2025 21:27:45 GMT  
		Size: 1.1 MB (1100741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8436b1eb054c2bec811af0ee938a47993aad8d126339487d5585625120f01a`  
		Last Modified: Mon, 04 Aug 2025 21:27:45 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
