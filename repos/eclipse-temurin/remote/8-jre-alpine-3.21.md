## `eclipse-temurin:8-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:46108c412aa21af8b7cc5a3844a24ad04718d12f277022e8d9de8cc5366951b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e2e214d626e42204d9e0aeb57258327edcd4758579cd48de22c1d29a7c795227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61603280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8e2f9f83f54ac8e16df37821134f9d6c7c8b88c04a9cff1c46efdd2fe552e7`
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4fb0636534b0cd4534a3cdcbbe7cf2e937523d6376d9cef00cc6cfd5d19537e8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294ff539aba2e0569828f0684354d9f30a7a2c324a5ed2ed06f29adad4d2d594`  
		Last Modified: Tue, 04 Feb 2025 00:00:12 GMT  
		Size: 16.1 MB (16135245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8162ea6aa2a012ddb94617af7670d4f3825d5b9c7c19bbeef10986034fcc0159`  
		Last Modified: Tue, 04 Feb 2025 00:00:14 GMT  
		Size: 41.8 MB (41823911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e8f353e144af132c24e7890d44f4a3fabffb56a5788be91c4f9a11e23183ef`  
		Last Modified: Mon, 03 Feb 2025 20:53:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a928bc2847bd3936e603316f6eadd3642ab881bcc38b310a07a11d7c5fbfe3f`  
		Last Modified: Tue, 04 Feb 2025 07:08:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c1552fd7152213238b4e8a8fd61542a2546050c9dae194808daf01d4007552a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.2 KB (941172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa1a768b77b65a8a35e1174a59bf77ca4eaf2c06a5759611e8a7616e7803fd`

```dockerfile
```

-	Layers:
	-	`sha256:6859442210e78519d53939d789a520043a364e404c534b218bce9ca6c9e23a1e`  
		Last Modified: Thu, 13 Feb 2025 16:45:05 GMT  
		Size: 922.3 KB (922271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb6b701aeaad765687c4b6c82141733e97224ddd89b77c183e352e4af2b1a81b`  
		Last Modified: Thu, 13 Feb 2025 16:45:08 GMT  
		Size: 18.9 KB (18901 bytes)  
		MIME: application/vnd.in-toto+json
