## `eclipse-temurin:17-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:5ea5933c99960896fe9362c7ea344c9d5ec8bafbbf9406fc8479afc024592aa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:026ac805287fdf43e667d0e33189751364ba4545a8a05a20255a59032d8a7b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (169957404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a334ca4baaf4bd20e8de908c3f7a6b97b3692cbda9c77229bcbc4bdb8f4aa4f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:55 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 22 Jun 2026 19:57:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf53c61ca0d565fa8e99caecb7f91b1e86aa7a7ec587848395a0529b97781aa3`  
		Last Modified: Mon, 22 Jun 2026 19:57:18 GMT  
		Size: 21.1 MB (21115717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65934b931948be295d9c545de3c9e9d0d32f6ae54cac2c85bf4369a4434748dd`  
		Last Modified: Mon, 22 Jun 2026 19:57:20 GMT  
		Size: 145.1 MB (145051681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954f1747c4e5c426ae38631e95b0494950eb78209f25ea413a0d591f5bfd8b0`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b77cdc7662fe699fa69859c1779bd00cbb4a4c357352a8fd626160a5e97e10`  
		Last Modified: Mon, 22 Jun 2026 19:57:17 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:99b2ae1e9311fab9d149973288824201807d67fe492d045925e7b740c59e96f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1106703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc849923c4fb74257312a0ce1c7a3c6acad5c66de04a5bbdc5463cfd2fc9549f`

```dockerfile
```

-	Layers:
	-	`sha256:2ac7565155f6881f908d5325207cd7f017fa49890fae84e39f97b67e658c056d`  
		Last Modified: Mon, 22 Jun 2026 19:57:17 GMT  
		Size: 1.1 MB (1087082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d258de65190c2aa25e3ca56f78e4921ad0012a1b403973dcb9abb5b1119d3ad4`  
		Last Modified: Mon, 22 Jun 2026 19:57:17 GMT  
		Size: 19.6 KB (19621 bytes)  
		MIME: application/vnd.in-toto+json
