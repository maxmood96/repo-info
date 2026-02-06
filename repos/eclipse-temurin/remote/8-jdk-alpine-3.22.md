## `eclipse-temurin:8-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:e952122463c6838b8b0d17eb7ebcc33820c1759123cf2eec2a424f63334edb91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:68811c1f950017bca89e6f801cca70d305321c8c98764a5058eb43a4498832f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73158659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468f994fbe9a14d56f4fd46c9e4b79515c874a9bb4fcbe4e8db5b447649aa3c9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1834a48a3505266cb3bc79db26f5ee911ce1e0fdccfb7f4652897577584b3f3f`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 16.3 MB (16294159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139044d6516fd53cf499322d945d57a044ef7026e60b967592f3698aac69e1f6`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 53.1 MB (53057192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ec9d3b4a0ae2f48cbd3f356a2342c62ba56808906410a919e563894ca3963`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bad8cc220b50d28fb9e65cb667328c33ff094f331a6d1d3268c808e20efbb`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:730fe160d525b11a4dcb9e1b4b4989b37a7676628676708a79861de81f913547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1121704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63526a29cb7750f78d32cfe42a43dd5724aace4dfccc8f00c4536564c53e11e`

```dockerfile
```

-	Layers:
	-	`sha256:bcf47061d0bdefd08184e672995e7968029d99cc657f402d5312e8bae250d8e0`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 1.1 MB (1102993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e20f71905ab389b8a9936148945bede36504853d4e186a9f86bae283519c134`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
