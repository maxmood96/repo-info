## `eclipse-temurin:17-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:fc9ce9540550d7d1524bb0fc0f00452132719d9b271dcb694c7f5af829f68248
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:82c130677c60dea9fa5626bfddce669a603c923860aeb25816a7ced8f2674c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67098441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ef018dc5286090bcecae4909dd6ba7e4dd658d36977326cd152cc3f2a31069`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:59:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:59:09 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='22d4d5579902d134dede626d0fdfb95891abc7578e13dea9cb23775498c4cf51';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 07 May 2026 23:59:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c7b3941eee5a2a884364f8c3df598f061769e6d8efa2011ea216f0b38c9518`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 16.2 MB (16219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fd1294917fa43846debb883be93142fe3350d1e5fd843b6b173b4cc93dc17`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 47.2 MB (47229289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e974076c6566a622b2fd44697a7cebf565ac36b531f4625ac94f2fa67036c8`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b9db8dfc621a62b67e8af736f7213e4cf8549b511f80fb36c1293a92f1f962`  
		Last Modified: Thu, 07 May 2026 23:59:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a01ec39d87744711b3a83cca59689f9e1ab16f6d374ab5482d29d23ac97539a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.9 KB (914922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591a8e72bf9fd042a36b2c213c4bbe713ce0f2327b1546ccac5b8a029d904b1`

```dockerfile
```

-	Layers:
	-	`sha256:79fa21bd2a378f4a49f34e99f9d71a7f2fe65b129c89bb3380b12341135eaa28`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 896.7 KB (896698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a73337d2bd6cd7efdd4434fd3512f70d3091604cd73e4029c9e13776cf28624`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
