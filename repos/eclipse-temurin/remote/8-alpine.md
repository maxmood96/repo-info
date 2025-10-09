## `eclipse-temurin:8-alpine`

```console
$ docker pull eclipse-temurin@sha256:acabb086ed67f6d09fe4302cad17136c353fb7343b81af94c2aa8aaccd3fc09e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3edd153d0b6288f1a1c3053db9d9c8e2760278659d6d6c1fa21b1d63e015276c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72729961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8ddcd42d85a51f9807750c605ff35a2f8d48be4884b0d255b30c9fbc1c7f90`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9e5a155a7ff06c0190ea62107ab1a927e87f603ebbf7a293a0f96aa156ee7`  
		Last Modified: Wed, 08 Oct 2025 23:01:38 GMT  
		Size: 16.3 MB (16289659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93265a0ff65ce60a966752d25af81c37784a583b19f7d06efc02dbe0e78378da`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 52.6 MB (52635416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bf4f6cfaadc211f87c2de87c1251cb65e3da0c8d13918165069ce606153159`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1db43729eb563fea67456a3da0efc23000862940ff05797f125d3eadf8db99`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c62394515d4eee2fb051367dec4e08dc78798431fd0197b053365760cd64f1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1123100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6e787c843735f316def970f8bccec5e75d1f401228ac373e19a7294b4df5a5`

```dockerfile
```

-	Layers:
	-	`sha256:2f1416f682fe57a6e5a9a4d8da0dd802503ca2ace75a8cd3a1ceb4c4085f15d6`  
		Last Modified: Thu, 09 Oct 2025 00:18:14 GMT  
		Size: 1.1 MB (1103354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5272469a946bb8db508fa82dec9eb89b53241c6ceba5bd6b315255d274a9c03`  
		Last Modified: Thu, 09 Oct 2025 00:18:15 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
