## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:f4173cdb39610d01820a254fae9be75d340914450e9662e03c72aff96e299b3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:54aad6a0d0faf65a7cf2dcd2dd9a750a243628f27e69c4c87fbbf080279ccaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123476275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f65dc15d738b245c629cce353842bb9c3cbe4ff05795615d8b210d3603dec74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c838c9d71fbfa07585d45b8debfc5b680d9c8787ba580e1cd4e57c8a2d59e9f`  
		Last Modified: Tue, 12 Nov 2024 02:38:35 GMT  
		Size: 18.3 MB (18307453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a88318cbb807e0023c7ca8136f7b07514eb50f094bdba21159f3218f2d48c`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 101.5 MB (101542486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6ed989cd330cf39adf75bb5b9c82cd4c0fafbbf4244ae1e70127d75c88a09`  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbc39eb27a46a707a33836de54b2b0542935fe61e33dcfa239431e794172e4`  
		Last Modified: Tue, 12 Nov 2024 02:38:34 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:47e0e09754b361ffd3a227a9dd4e2e51aaef3cce946de7d5acfc8cb281444f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89210b21ee69c30e3caea543cbd89d13b4e540a9250862780f99e232a4739b4d`

```dockerfile
```

-	Layers:
	-	`sha256:f1acdc09ce36e59086843628c4a0b7770dfe83d23a5f8ec720a3e9a346cb0ef8`  
		Last Modified: Tue, 12 Nov 2024 02:38:35 GMT  
		Size: 1.1 MB (1089459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1621cef5cab81410c792d7f7132058ed36451b4334bf63451bbc9e8eb89bacda`  
		Last Modified: Tue, 12 Nov 2024 02:38:34 GMT  
		Size: 18.7 KB (18719 bytes)  
		MIME: application/vnd.in-toto+json
