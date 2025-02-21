## `eclipse-temurin:8-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:75b5547bacf966f165fa2ac8c310465d6bf668e65319b29baef299d5c5c4ba9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d906fff0d39582a823e5fa8f2f6db7712c3470d6dfe1371382fbd25445319c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72282169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f678c804183f0d96dc9e25b5d58324ed2322dd293110456de9d13e114715286`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d64600076e50cb2e4a28fa6b7e5c1d7931f47815fcc383cfb9559a3d418c81`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 16.0 MB (16023345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4795fdab62fa8bca78c2a3123c50e07b6160917d89de945351c750731455903d`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 52.6 MB (52629492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddf69d9377bb0fe458cb20c1f54a7e379e3ed9367769a4345e3ab0999c39404`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888dfd93cf5c460882af017eff457e6fe0049cb8c29d2c6f4706fcfab84a46b1`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2b812172430937320734c062421a9fc2ff47c043a8fb1ab9609d87a75d962573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1107420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efd907f2dcd4d90c831f3ee657aca54281947d53c52b019f6f628c2f4e4efa1`

```dockerfile
```

-	Layers:
	-	`sha256:253da15cc6951d57b977c243707222912e651dedd90703e3bfb85660914066bf`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 1.1 MB (1088666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbff6fd74e91345cce0470ef2e851b0b5c004a9b64c10181b013079ef31b3b1`  
		Last Modified: Fri, 14 Feb 2025 19:25:01 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
