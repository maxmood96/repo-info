## `eclipse-temurin:8u482-b08-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:e53313abdffd7bd3d863280783bd9c877f0527e4c57ba5d7f83c79ee0100481c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c9495ebcad97b7528d151325f8943a7414d4dfdea07d02821f7708468f590ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62383977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714da9665658b26d30799f5f1e2e69eb725c6f48940829faf0dd46d5aaa4a1e7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:23:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 17 Apr 2026 00:23:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 17 Apr 2026 00:23:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:23:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f8bda847859193cd2362f05bcc05cc8a5700b6073c2d57cd933b51dbb9aeb0`  
		Last Modified: Fri, 17 Apr 2026 00:23:59 GMT  
		Size: 16.3 MB (16316831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40b1825d4136d66ab499816a8326c01794a7a464547057456b143b2b788bf2a`  
		Last Modified: Fri, 17 Apr 2026 00:24:00 GMT  
		Size: 42.3 MB (42256549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882dd8cc41e6895326b39d0f2d6fd6080c2dfc0a7f1a8e22aa958d2f630df7ec`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e7b7a22632319fff6d1a78f2d9af0aeeb76e17ffe30e6fe7c04a36bc0c6731`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:84654f38a206f87fb7950760547e12299f92efa4a1a4d47d4b2b59aa6bb2bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.5 KB (946533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187791904ccf141ad7ee41161cf742987ff65e1ce4f35d7e05b05743b924f7a2`

```dockerfile
```

-	Layers:
	-	`sha256:5712b0bd97dbf14838bdde9f335d75e8c37a45759bfc8e9a8793dc610d7fb5d9`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 928.3 KB (928346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed3a7e0738d50dea0605193e907a56791465fc28181a4adbbb86cde7bd6d035`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
