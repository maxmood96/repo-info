## `eclipse-temurin:8u422-b05-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:3e802b5f1915aeb0f2ef7a01218ebcd30e8f8419ac4b80c7f379f39efc74e2b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u422-b05-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bf98a519790b24826168a130bdb6373da4230c47deec2f2af76c5be65aeecb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54838887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd8a65cacb9fac6b69f5d4ac32813d1ae5f41c03161c2dbb0938988caf19e66`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9a7a939638b9cdaa8e1a119b8f21bfdd4cb2390b8a47cc27ccf9effc90f4b437';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70889a85db12e2e03b1675a5dd3316837ea1e4c0178b15f72ea6110f143b7da9`  
		Last Modified: Sat, 19 Oct 2024 00:54:57 GMT  
		Size: 9.4 MB (9389053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80af6f369af482d2ac4915e71d4888a548c3d482d41a98ec1d0f65a2cf2ce3f`  
		Last Modified: Sat, 19 Oct 2024 00:54:57 GMT  
		Size: 41.8 MB (41823792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaccf8b5847648eda620ab0a530ed54bf12d638d64e1410aea4e4e3f9188a8c9`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0eefb8113c510ba382463cc23fb7599898f7824a38515c1c997d34dcb4909d`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u422-b05-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9faff992da32f1b55fd9936bb7c366ea3dcc33f678980ab741ce984af36c0205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.6 KB (828620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0582d64a88a877d9010a31a8dfaac961a41c73df90269a8cc06391b79d82d`

```dockerfile
```

-	Layers:
	-	`sha256:84533b59f82687ab94bcf550a3c0275ca032b4e5c5df5b8eb03273be4242d27a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 811.9 KB (811885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fff963500e434d2b2ec160bccd8c5e2077cfc9aa51655607528145c85b015ac`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 16.7 KB (16735 bytes)  
		MIME: application/vnd.in-toto+json
