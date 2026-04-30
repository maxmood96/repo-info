## `eclipse-temurin:11-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:1ec72ac90fe9b41a333a3df14ef61ad9fa17c836aec82be84b6a86f2b082d70f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c7f52075ea2f71c4fc289d2ef6218878131d6e0d4aaaf58215b34bdb87b16c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63831084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846ba7039e27e8ed682b875f829bac48839b1c87f706ba86b1ecee4ccbc61cf5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:45:24 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4a1ba44d0b28523ff5b73a5015f3bcc6b9d36f3ac313ffb87762946af7f642ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f956486b41c144416d21770b22cdd47083f24e62f9092955399fe13cdc2ea2`  
		Last Modified: Wed, 29 Apr 2026 22:45:38 GMT  
		Size: 16.3 MB (16316741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f605308cd9e49adc98392321da5f407a6a3df185f78645086e82acc2b2d24a4e`  
		Last Modified: Wed, 29 Apr 2026 22:45:39 GMT  
		Size: 43.7 MB (43703747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb21d5a47d9f5eeabe3ac4ce501c8cae16fa1d81770664fb7327b08b36fc1cf`  
		Last Modified: Wed, 29 Apr 2026 22:45:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b07ce7c340b7a76915e633b17fb651d7bef336ba14b609407cf126908aec577`  
		Last Modified: Wed, 29 Apr 2026 22:45:37 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a00daa131a1893b5b84c54b85a3fc9af7f48f0c9a187d0cdf3c950c01059faf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.3 KB (928333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44acdbc3e8711962d06c5db0aba676c317082bbc33836f6a1d91f485416457`

```dockerfile
```

-	Layers:
	-	`sha256:8d96dd8ce62d199448a97a27015c0cec12785731e87177651e4fdba08f724311`  
		Last Modified: Wed, 29 Apr 2026 22:45:37 GMT  
		Size: 910.1 KB (910109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0a9c37ce146f7e59f79a4487339b5287913879e9d4d11eeb132a5a3b629a45`  
		Last Modified: Wed, 29 Apr 2026 22:45:37 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
