## `eclipse-temurin:8u472-b08-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:d5a08fce8cc0bd81591a0793ede78cbc2167c3fbdd0b45743022cbe126b94916
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c10101f6b597cfeb8265cb7969f32ba9704afb52d28a2967f72c4dfca69633b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62544821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6991a97e60392308cf98863f58ca5e95fcee6550fa60ad66e6386fef719426ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:53 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 19 Dec 2025 17:28:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 19 Dec 2025 17:28:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:28:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:28:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd339c1f2a49a0d087a1906b976a8cb90780165f243db41c6ab009b23aaf828`  
		Last Modified: Fri, 19 Dec 2025 17:29:16 GMT  
		Size: 16.8 MB (16839444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9d73ef0197d88c41002e64c6bbd4561a3e0ae2667496e0dd98c0ea2cb7d376`  
		Last Modified: Fri, 19 Dec 2025 17:29:30 GMT  
		Size: 41.8 MB (41842867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626a08c6455b22d54930017b1d5d87dfbc223969857b0b1299b65dfc3a987b0`  
		Last Modified: Fri, 19 Dec 2025 17:29:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807fb4feea2e7a6f3fa5c310287309bb16d2173ca5dd3e053744cbc26265735`  
		Last Modified: Fri, 19 Dec 2025 17:29:15 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4379b1948b5c71711cff71989a9e51b8e6a290bb86976d6f9d980ecef26116a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.2 KB (952204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4abd571cf26f17ad80573d676d475809de09b850b1685ece27b8c9f750664e9`

```dockerfile
```

-	Layers:
	-	`sha256:44a71e952d0c817f1b5089a93c0116affc983868b60c85d180510092a45af4a2`  
		Last Modified: Fri, 19 Dec 2025 19:16:24 GMT  
		Size: 934.0 KB (934017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f3107ece4f9c915bb8146ff657e3b2620ea48f25d9b40c3f49a55de710c62a`  
		Last Modified: Fri, 19 Dec 2025 19:16:24 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
