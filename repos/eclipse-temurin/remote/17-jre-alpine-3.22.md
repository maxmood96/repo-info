## `eclipse-temurin:17-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:288261dc05866256873a1f8b5418ceba3461d91028cf358198d21037555657f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5c5b34c8e365e6e2f86e480b7f86e6cd5b7ddd183507ba7ba205893643bd1e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67200644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a10970ac59c222ba33160aaf217c2515e7c6a878439f4796b5d038f02833d5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:20:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3226a10cf4f7ef8f835148ce8737490f0cf63e38a1e3ba26cf1e05d9e28adf5c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bab3bdd95c102e05acad9ab52cf85c6bdc4899f0d6435f15cee045d4024b9d`  
		Last Modified: Thu, 05 Feb 2026 22:20:28 GMT  
		Size: 16.3 MB (16294152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eab94e1dc30ed9023eb29f4f66917eb24bf2604caf959789935f05bad5dedd`  
		Last Modified: Thu, 05 Feb 2026 22:20:29 GMT  
		Size: 47.1 MB (47099209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d7f4a95d7445d1b9f5346b199da293cb28cefe190e3caaa52694563d293229`  
		Last Modified: Thu, 05 Feb 2026 22:20:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a5230960fbe5573790c52b3ec7c702bd3f05c409a683240b5d4d2851cffba8`  
		Last Modified: Thu, 05 Feb 2026 22:20:27 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c541a24500577ea71b748031119c161248fa25dd1af26bff8f6040752b2a304e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 KB (916515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fff02ede158d15e2862abe0cad9a2d1cf3e365a557c327c8b0215487e06f88f`

```dockerfile
```

-	Layers:
	-	`sha256:281bed53b3b4fbacc649a9a989f0c35c5831a24ec45c39c521c52506c7482f20`  
		Last Modified: Thu, 05 Feb 2026 22:20:27 GMT  
		Size: 898.3 KB (898301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:969baf5d1e8dfb5340c3e531a7ff71366bdf2fc21c8650a3a9ff35b2ca40a3b6`  
		Last Modified: Thu, 05 Feb 2026 22:20:27 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
