## `eclipse-temurin:8-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:0c5b2fc6f29b75ea21a319b3961bdea7f1a8b20becbd399697d6eabfb249e5e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ed8e1b1fced474e3e48a0c6f3e4c8f656748eb55c358fbdd784c289f28e862a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce13c7058110aed3c415123c5108f6b4752169908845d80533657fa0195eb8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 22 Jun 2026 19:56:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563d88546d96f1d2f93220b50acd3c7357e55dd36553f5f2ea3136c665b588`  
		Last Modified: Mon, 22 Jun 2026 19:56:40 GMT  
		Size: 16.3 MB (16289486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71fd14a041729f3ffadf09b9a1777b46d31a8c1c9e64a3c3a19a5f52f2354c4`  
		Last Modified: Mon, 22 Jun 2026 19:56:41 GMT  
		Size: 53.1 MB (53080144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd8d8e4267ee1824e06f3c5ce77c6664fdd76700165bdcdf777149121a31e8`  
		Last Modified: Mon, 22 Jun 2026 19:56:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed500646f18358b06cb19576f093cc50c5bea7099fe7174ffc08783d9b4ad4b`  
		Last Modified: Mon, 22 Jun 2026 19:56:39 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a235c41c55664da3b1b15d21fe73820c3a701c7df9ce3109e3f35fb3b44c86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db8bcb15ac136ad4c4d1fb6514686ad18374f739b3ca136ba0864fe9df2e790`

```dockerfile
```

-	Layers:
	-	`sha256:55b8c30a87f750e524dffffa22883f1a76a78ad925e8a60013c4e552c854fefa`  
		Last Modified: Mon, 22 Jun 2026 19:56:39 GMT  
		Size: 1.1 MB (1085421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23444e39cb08a8ff70198765a50f900951de4b535e0d8ca6d234c2a40b86f4fa`  
		Last Modified: Mon, 22 Jun 2026 19:56:39 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
