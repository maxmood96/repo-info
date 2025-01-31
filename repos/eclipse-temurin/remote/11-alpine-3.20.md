## `eclipse-temurin:11-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:3d9719e70fc60408d2451547bbb8e196ac16bd9b9d5cc48b3eaab6a377ba500a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0ae05bfdc3e08964b95d9665d1b822d6047efe1e256529721b4fe804efb9c03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160420572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e7079f5870046a17a5f4d40ebf12d2d81bd88e8c699de9428daec1599df6fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e1f667395cdb1e872bd7320e3eda96c0f0978e29e574e75f9cdf61160e8974a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56975df28a27d17c6f44425de685fff4c1a61c1ca04f59f6410d06f00073ba`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 16.0 MB (16022252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085adcc8b3c69f047ff2eed71d1779e242262e601939775a55dbb0c8be2679d1`  
		Last Modified: Fri, 31 Jan 2025 01:29:56 GMT  
		Size: 140.8 MB (140769652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b59cb256977bdb654aae92925f664c715a199b43c9d80698ae4dae423e2346a`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d74f039dfa8ed3fa41828f51a672903ce34ab2a06b878b02599bc936d70005f`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:506426282475bce72331354d662f8d2f912347dc761232a915a354463724c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d6ae66d971a0f309f1dc566f7601c9b15501a3fbf2ce0e00071d3ec96a1ced`

```dockerfile
```

-	Layers:
	-	`sha256:5611466db6eb1c3fe7d1b23c37bf5750287b8da28ce00c2379b5e3259811d66b`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 987.3 KB (987346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a1c89ee559b15fd67cb9e17e3cffdb89b6c5812586a8a872e1e426250c9268`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
