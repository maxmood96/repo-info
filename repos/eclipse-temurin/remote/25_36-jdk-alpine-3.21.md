## `eclipse-temurin:25_36-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:55cb381e0575555b6969c917ac06b9b1a495edf1a546b8a8a7298fa4f8157ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25_36-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ffd829f374f67bc46ea7f067c57ca33d847fee604b8bcb889972646155359fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109083132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1176dc20b9aa75cd993bf19f012b83830cb4f8d352bc191700929542256775c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba71ae14a29c7c26a79fd73c98ecf70ac8cb15d4721516f2fd38977d6502bf`  
		Last Modified: Wed, 08 Oct 2025 23:37:03 GMT  
		Size: 14.2 MB (14172013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c305b49cad6a6be9c2a9c7b2fa413d3353e4f71dd2fa236d51a366f1d30e348e`  
		Last Modified: Wed, 08 Oct 2025 23:37:07 GMT  
		Size: 91.3 MB (91266142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed902f16b62128ea17f3bcac667de8ea071948f37c3529251f0756a49647b4`  
		Last Modified: Wed, 08 Oct 2025 23:37:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086959ce2b5a051676c82acc8d641b4ed425f1ee5f0d11a7c3ff5409cd5eb0e6`  
		Last Modified: Wed, 08 Oct 2025 23:37:02 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6370a5dcc03951cce49b6366a91d1eef47caab300e1cef8f4b2b0808364ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.1 KB (967101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971ac6b1fd24808353aca78e85a098892629fcbfc6aa48f5f8e32987e9d281de`

```dockerfile
```

-	Layers:
	-	`sha256:a8da0ba522e109b832a490ef8067dd5b6cbcaa3c927f0bc0674e9bee4230be54`  
		Last Modified: Thu, 09 Oct 2025 00:17:04 GMT  
		Size: 946.6 KB (946583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea7cdb5201459ccda776a1275ba856b83e434100e3d8fa8fc4a92d0da51126d`  
		Last Modified: Thu, 09 Oct 2025 00:17:05 GMT  
		Size: 20.5 KB (20518 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25_36-jdk-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a45e1c771923d56c8c9c08f1002e93ba97100fcd16c1534c740a2d48c42108fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108434502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d6ae0b282a20ef352089277fedc78aaa01a99ad7e84e42525a990214f473ef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb4032d5bbf21d741500bd4c63447053405bddbe8ab3b3b1a87297783720f4`  
		Last Modified: Wed, 08 Oct 2025 21:49:05 GMT  
		Size: 14.3 MB (14269517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ab61261e598cafffb374e1235bdea122e771fc4a1c57ab39b443e0ffc0655a`  
		Last Modified: Wed, 08 Oct 2025 21:49:11 GMT  
		Size: 90.2 MB (90170222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eda98f6b56711fb48d2b3fe0fb7d56ef3fd8844c568943f3593db52f8603526`  
		Last Modified: Wed, 08 Oct 2025 21:49:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bba6497bae8a7414867121184a5e11fda8f34bef345ff2e8b2078c2d47b541`  
		Last Modified: Wed, 08 Oct 2025 21:49:05 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25_36-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1bea8e3c7012a44ac18ed3f1b67bb028a087193dce674255e25aa05b5c54c029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6baa171a9983fd23758b9480d4566471ec3813606eb6ed8a0e29376b478c6e5`

```dockerfile
```

-	Layers:
	-	`sha256:095fce3f9e711d89839dfb1a5b1a7c768c4f038362b5c677b51c60b4f92bc85c`  
		Last Modified: Thu, 09 Oct 2025 00:17:09 GMT  
		Size: 1.1 MB (1096582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386dddc5cd01aeff1abe7b794ae71d485ad2c86a64cc70f6c575f5c185820732`  
		Last Modified: Thu, 09 Oct 2025 00:17:10 GMT  
		Size: 20.6 KB (20640 bytes)  
		MIME: application/vnd.in-toto+json
