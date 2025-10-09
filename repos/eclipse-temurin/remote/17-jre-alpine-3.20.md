## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:339674eb0bd485ac2671fcebba61400312f16b79007a6184f7650769ee66d872
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d54b618b3b8bb60ff6df19341fb5624ad059f72cbffc92ff742f71f3027cf503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae160df9ce0b1920707685460f7f79aeb2eeac1e27dd25086138fd3061007dab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='88424be8b71d7c801c39866cf19d3b7c49b1c499cdccfa292e103c7cba08c21b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a66ec770ae6ea417d052732498fefd45ad1d3c2822fb99941c9c4c5e720957`  
		Last Modified: Wed, 08 Oct 2025 23:02:04 GMT  
		Size: 16.0 MB (16023364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a240d68dd6d2f47e5b8e58071020753ae72d1bde4c6e278b5cbf96683758b2`  
		Last Modified: Wed, 08 Oct 2025 23:34:07 GMT  
		Size: 46.7 MB (46664541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab52f199ba689f2a5a17915c59adffd042fd5a047eb8f658c794ed72972bc6d`  
		Last Modified: Wed, 08 Oct 2025 23:34:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6f53c550b0f867b5fd9b52fc64893cfacd9f7577f8844a8628c8b2d822f3d9`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:96cb834e32bb4eb332896dc375e951395d8da95072d3ac54afe8ad11e4853ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.5 KB (906496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0b817909b354fb1d0f6f968074cf70c2535743ad507552e3164c03bdaced8b`

```dockerfile
```

-	Layers:
	-	`sha256:bde50804cec3fb104c125ec9d9d3f96e9c47bd25b12b8f168877ac257617e6f0`  
		Last Modified: Thu, 09 Oct 2025 00:14:20 GMT  
		Size: 888.2 KB (888239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070b7bd4b33e90c48fe35229cb77b4b38fc910fcb1eab4eac387ffee44c132c2`  
		Last Modified: Thu, 09 Oct 2025 00:14:21 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
