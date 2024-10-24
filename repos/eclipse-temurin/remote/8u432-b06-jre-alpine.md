## `eclipse-temurin:8u432-b06-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:98a125daa0a30f3fd411287aca6b4ab5dcdaa92dc1df6ada63e04cdf9407888f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u432-b06-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:059673da8df6415c5fc83cc0863211cbfff41f916e9bac1cc40600483ff98cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63752410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7713c3d3de27d5a88236e38e8ce1c8a527c0d6bab270e4567c84d44d724b40a`
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:6b44aac08e486bd7570e2707a2b2be64763695a251fb43e6c5258fd800c550b4`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 18.3 MB (18307489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f75f98ebadbbb254ddd6535f206a6b965ae67279830001028a35aae0ed6960e`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 41.8 MB (41818707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e79129544ca49f38f069c73b502081b6c6215128618b9a99a3d8aff91b328a`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a7b53c655069bedea61de2c5c4b0012d404a33386836348a056266a5b86097`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dc647dd3c2ce0eb0da433e5f8136979203fe4ab360c58ce312808e93cd2ef498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.7 KB (932719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672258f9f6ecdc55fa74ca26a347ae481777e73184cdab5256d4b7488a8be9ec`

```dockerfile
```

-	Layers:
	-	`sha256:af99aeb859b4356677cac571f757e1f9c782861bfcfcdb87c82eac4f3f255189`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 914.7 KB (914661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013fdab8574992da9247ad8d50ec6cdb0df3b378f3040aad860ec5db1da36fe8`  
		Last Modified: Thu, 24 Oct 2024 00:56:26 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
