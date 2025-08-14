## `eclipse-temurin:11-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:3198e79bc3aefdc06c48f4c04e38316358de40982b1dc88830ded8372c1be4b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:59137b34e1ff53969c8fe7dc0087cf1c4172e57c2d58598dc5a481295d6692eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63229080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423d12cb120badd693c53bffcb9dc259779d1c41ec93acc7fc38147e7e6eaeb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b0092a3f753beb13221fab3a1ce713390809b4841b4a5eb407f9819d628c8856';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c05913ce60781d6f8e8c69deeccb867538dfda0a8331ed472113bda8807b1c6`  
		Last Modified: Mon, 04 Aug 2025 19:11:17 GMT  
		Size: 16.0 MB (16011663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e690080a0f536ceac9687266a0e3336573bf204699fdb103e9125ec3f71ef7e`  
		Last Modified: Mon, 04 Aug 2025 19:11:20 GMT  
		Size: 43.6 MB (43594533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5c126e99c877d06eceae7c329ad8403b089431ab60c55824d04a50cef9d52`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2a049ff11874534321c839b8b8fbc4bd76235de68d8c3bd592283785ceb1c`  
		Last Modified: Mon, 04 Aug 2025 19:11:15 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a9b0c3b6c9c2d9a4a320a16d55cfb3b69c14995a470be96b4f90c06b1cb8890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.4 KB (916372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffafa0cd45296469a02bb6b642a6349de5d29d2ca5f491406bafb2eabea9075`

```dockerfile
```

-	Layers:
	-	`sha256:f3161ccae9a0201db9ab8d52bed25afc75485087ad823466692b8a8db82dfb8c`  
		Last Modified: Mon, 04 Aug 2025 21:14:16 GMT  
		Size: 898.1 KB (898115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c405db3bb79b8aedd0033fe16ae99ff4d4900cd15c2951dd3f1efb5791cf3a`  
		Last Modified: Mon, 04 Aug 2025 21:14:17 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
