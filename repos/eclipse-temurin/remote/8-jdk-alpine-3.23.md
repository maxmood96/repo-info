## `eclipse-temurin:8-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:5df9e2a8f3aa3fb2881689f1c24c882412eb293a8cff7b4bf4a0e8822772e13d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1007b60e0e6f4da6d289f542e329576bda0ce7d028d6ae679f0cd9e770b31573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73339555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c9d5e6f9e0303f23d30b5072d6908f7e900f813623f37968b326d0d18b2069`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:11 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:11 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 19 Dec 2025 17:28:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 19 Dec 2025 17:28:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:28:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:28:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee8b0646f656de250ca1a6a8ef702342d5a8339a0b2832185a3f541607a5f5e`  
		Last Modified: Fri, 19 Dec 2025 17:28:40 GMT  
		Size: 16.8 MB (16839497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d460db6220d138b1e238d962b9eeeaa627b2398eda382665b0ffaf53c688e192`  
		Last Modified: Fri, 19 Dec 2025 17:28:46 GMT  
		Size: 52.6 MB (52637522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4ad705c93121e3d925861476e0cc180af6658e7a42cb4186327d3a845c5038`  
		Last Modified: Fri, 19 Dec 2025 17:28:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fcfc0339ce24e08232918a6f1e090588828f5dd401be7002ebb9a049370903`  
		Last Modified: Fri, 19 Dec 2025 17:28:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b014a9de437c56bc112e306d01b0982bc617a10871e5ea246f212cdf5ac80df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1126686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed66b9e41a270b2e079ac528666a170f349a9e5da2a9c5793677d9e114016b88`

```dockerfile
```

-	Layers:
	-	`sha256:18aa395326c8e688fe8f9ca7fb28cbfadab7d30545d39d44eaf3ac28ff717e41`  
		Last Modified: Fri, 19 Dec 2025 19:16:12 GMT  
		Size: 1.1 MB (1107975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd89978329aa6eef6e87a08f9c0735bf39b4dce6c80bd040060684936214c294`  
		Last Modified: Fri, 19 Dec 2025 17:28:27 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json
