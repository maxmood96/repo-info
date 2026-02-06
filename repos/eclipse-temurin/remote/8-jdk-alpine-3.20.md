## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:f93db08db529199c411606961647f4870146ca81f8274b8681643550a04c1ef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:157620575effeb1cd9b87c71927528e634c4eff33c475d5f3a35d2752e3e0756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72769030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf70d840f25f0c0dce1fe3211869ea8c5234a0409b8ed22cb27fec6ad45132`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:08 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0f4cf8f93d23e12916770872ed7c1795626038cadd9aee6054aa77edc39a4`  
		Last Modified: Thu, 05 Feb 2026 22:13:27 GMT  
		Size: 16.1 MB (16081531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66938ef23f8092267e735aaf67b12d52fd64bd6d0a63d9bf61d9d042693b2b40`  
		Last Modified: Thu, 05 Feb 2026 22:13:28 GMT  
		Size: 53.1 MB (53057201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8285d6a8ab29cf9a716b7a5b51544cf56ec3858c013a63bb5db95515ed14337a`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135766a2cec7cfcf5fbb5ca055f6c96f6828b3fc8bb7373f44af082ca88a3f8`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ffd1abab59d67eadc07d2dddf6a6c16a383f80d3212a15adbe44a983e08dc544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f2b92d358532359b5e01d058bfdf13a64165b4f994b817fc97933b59d6d353`

```dockerfile
```

-	Layers:
	-	`sha256:ed22b145aaf23d1295e3162b37cb6780dfdf042c1710b81979265842e6b9b299`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 1.1 MB (1094960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d1f5d084065e2cdbe049834012b054357e79aba6645f42fff20590224e3174`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
