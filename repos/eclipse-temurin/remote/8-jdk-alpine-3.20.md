## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:7c3e54a537d42f52e4c91c29a7fce042d3ea6d78d08e457365344e1b2ac09fc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:41acc5eeae37dbe6019b893579af17b66f4e07696f61ccef59a305ad1e510eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72277287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d5a57d4997b33aba118d8d83016feacd60be0b2e711b86920cce87e8e58262`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47901869702831fea4a14a7952fc33608e6246679610f9fa54f6de06db46eeb5`  
		Last Modified: Mon, 28 Apr 2025 20:07:40 GMT  
		Size: 16.0 MB (16026112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f56dddad7703b65ea78624ad99c9f7dcd759e484437e3b9b2ddd53d5892849e`  
		Last Modified: Mon, 28 Apr 2025 20:07:40 GMT  
		Size: 52.6 MB (52621847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c18520b525a6240fd7e5c8fddccec5e012bdca60dbb341584157225039e25a3`  
		Last Modified: Thu, 08 May 2025 17:17:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627ebced9b5bd4951800df929f24789bef33709f856bd7f8b1738d88ad15ca26`  
		Last Modified: Mon, 28 Apr 2025 20:07:40 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d88f672e94f288b10ed15db6e03ca4f8ca2ddf855d340175070e9fb57ba16108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de1a68888d5a71c1da0ca658a52292080e3a35baf119b101434483c75c90c45`

```dockerfile
```

-	Layers:
	-	`sha256:612c692794ebba862f1313a8f958186d3fde47e8e3ba54f12d8275137dfec89a`  
		Last Modified: Mon, 28 Apr 2025 20:07:40 GMT  
		Size: 1.1 MB (1089288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd2cfda7a2af11b7b19159c818ea78c0a986868cf171b3af1bcfd2580ba6287`  
		Last Modified: Mon, 28 Apr 2025 20:07:40 GMT  
		Size: 18.8 KB (18753 bytes)  
		MIME: application/vnd.in-toto+json
