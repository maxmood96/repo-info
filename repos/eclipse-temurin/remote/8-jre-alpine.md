## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:0865d08cf588d2d11e5ec090e1cd42ede14f6db1dcacde17d37f558b60b081ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:743a6fb53df157fcb0840887aa3b5eebe0188528516eb2c3449924c171dc2511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61644322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f763a70940e3fae8d58faaa44e788e78c358d6842c9156aa1840a3ad7ef40d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4fb0636534b0cd4534a3cdcbbe7cf2e937523d6376d9cef00cc6cfd5d19537e8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf13c66f60c41a33897cd40178c48771098f169a6e4a55bc4ec6f06d81ec32a`  
		Last Modified: Fri, 14 Feb 2025 20:36:58 GMT  
		Size: 16.2 MB (16175658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26918a07338f2ee3756983c6dffb6360174b95bb8aa2af4cd76340f813d829`  
		Last Modified: Fri, 14 Feb 2025 20:36:53 GMT  
		Size: 41.8 MB (41824010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4801c8bf7bdd800257b220db042f32f0a3b31e26ec623d2d59159a2b6ccf0db1`  
		Last Modified: Fri, 14 Feb 2025 20:36:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336753188655c831a8112b1e1412ac1df4e8900223090e4677d78ae3927d70d`  
		Last Modified: Fri, 14 Feb 2025 20:36:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1d835efc17c6392c0262ee023313a33f500c8a623befca9fce94024792ac763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.2 KB (941179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a25bc5f03ff0e1312587d19c2a8a76c518e2ebe3726900fe66a9d9e6fe45f03`

```dockerfile
```

-	Layers:
	-	`sha256:a797a52a13dfae522d5d47a0dc50c0267b1242320f8e927291f3ad44bade8ddf`  
		Last Modified: Fri, 14 Feb 2025 22:16:24 GMT  
		Size: 922.3 KB (922277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de96965fdd90b4b60f1204170df7539ba1baaf17b070f7d91a44129693b8c64`  
		Last Modified: Fri, 14 Feb 2025 22:16:25 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.in-toto+json
