## `eclipse-temurin:8u432-b06-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:4fec424736b580d7a9779930782a5bc103aa1ff6a3320371ecf8cac9ab4bd67c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u432-b06-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:13f0ebc088f628f55642043a01f27d80849d61d730c57cb3dc25f46e203b78da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123476104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e76ea647a56a9a2c988f4fd6c3adfee1d96bae587556c5f9ddc059718ee5fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01eb70355033ab6dd8da26dc89c8cc17ab414daab89c3e8db799a76d8db8191`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 18.3 MB (18307357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67011bcdbe326e5d2228ed719b06657a451c130711dd51a2765340b845aead21`  
		Last Modified: Thu, 24 Oct 2024 00:56:32 GMT  
		Size: 101.5 MB (101542504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c003f0089d423ea3950139530879c979fe6b5566302c05bb0e275681d7374661`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a546658f7d29ae1a954fbb289a243325032aed159592ee0bd3a2b217f5a660e`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e70f1cab922505b319310a896d4dfeec5cb9cb3014ce7870c9320d2547c6fda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1107983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9d5550040c0014302d77b0cdd4eb63d9437614667afedf6520431e50e21931`

```dockerfile
```

-	Layers:
	-	`sha256:0d2193107577fab0bbea9b58a73ca1c93ff8b89c41519b1584692ec9665326b6`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 1.1 MB (1089458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bfd6c7be5e1108cfd1370c9b9bdce98feae0c05621bef1d16b8559c5dac54d`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 18.5 KB (18525 bytes)  
		MIME: application/vnd.in-toto+json
