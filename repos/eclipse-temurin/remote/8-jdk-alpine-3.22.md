## `eclipse-temurin:8-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:a2e11e7268a4e15a9a885a55c769dd3f56df927f8ec37fe9b22c225cc781138e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1981c13f3d1c252ede2336257d965c0424147060d2d76cf27251063025a099f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73228438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a969130d4c2c24e770b4c226f164d67f0895356e0d66a09b82f9b66103ded`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:25:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:01 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:25:01 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8529b55d79868cb31c931d3fdf76b873959204c1465cb20ef02c557fbd2d0314`  
		Last Modified: Tue, 12 May 2026 21:25:18 GMT  
		Size: 16.3 MB (16337480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7746302ee43a1043cd10214a771181b7399551845237edffd22064afc6c467f5`  
		Last Modified: Tue, 12 May 2026 21:25:19 GMT  
		Size: 53.1 MB (53080161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e2bb1cbfe608bdd125d64303502e49458ec2bae32c0c4c428d038e7c6fff22`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329eb8b1f09948ec0391ee5f0823a80350c28c58ef33c07a58f525de8645cdf`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:079365461768e935e17ea902cffb90a446a0c68ac134a7db9cc8bfed4a956fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1121019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35ce9afe53f49a0877392e135f670be681a3d87fa85331017cbc6d98e068866`

```dockerfile
```

-	Layers:
	-	`sha256:d37475f95a8df4dccbd5ef5b6fee5ee65a8109457f556a2a8c16a7a567bb1e20`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 1.1 MB (1102308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97bf81807658c8f1ff13767b1e61d302152af8e9d54b42eeea105f6ba2af583`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
