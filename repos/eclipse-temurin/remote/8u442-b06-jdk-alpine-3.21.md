## `eclipse-temurin:8u442-b06-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:a83e2617731ac494343c5e463802b54a4311982c907840a2dedfa49a48856021
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u442-b06-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:aae0174f1dd01c5cafb0ca1f213c8ab70cb027d2dca10264a7bb5136ebed42dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72408948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d692d8df6bafd236fabbc89cf2717490113967729282f99ddc729c445d581`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9fcb96380b25c1d1caec65b7606c387716a7ae51caf359f5f3ff0dcca40f231f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e356728e49475bafa1991667011d8953c9bb74a078c4ab79b0cd1c4b4ca0e196`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 16.1 MB (16135293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc81bc153f6ddd85a531c37ec09fe39f74b62ea7f66f53c4be90272d66d7b75`  
		Last Modified: Fri, 31 Jan 2025 01:29:55 GMT  
		Size: 52.6 MB (52629506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fb220a47244d9af8ed0172e845bf6b939c026158c8ddee6f57a9f7186fda40`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83084373d9dc1bed9ddce2ebe84b276fe807daed6ecf0e93db1f464ea48ab3a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c71100ec76d1d00b611747ef005443abe17f0e4c4ca1d1e0b675358ce2eb979b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b24e60941439832ecfd1369de9219712a7d3137b49859bcc26bed4a2f27f10`

```dockerfile
```

-	Layers:
	-	`sha256:8aaef4971938c238b33fa6516f1afa400e6c731dbafcfb6cf4aacd74979a5b8e`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 1.1 MB (1096549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4088118ab0f6e4860da711511412c114558ab584de3ceb47f4f16cbb2745c8f6`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
