## `eclipse-temurin:8-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:d5c99b63168df4b9b9b8b101d872d96284bcebf76eea774479cc00c85075cda2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2a3a709b4c31e79ce903806a9d3e173ae95fbe20d40bdc2ddb3a02bef255c75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72454987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb69edf4d5dd37922d2bbee0d58b13de0a971e1fc26ccb17ea9277ecdfb81ac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e518bf4d2dc069c03c1ee405432433fa41ad1d693b65c8ae3505a0cbfb96fef1`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 16.2 MB (16174554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da622b8abbe9f14b819248df83ca57fd9eb03bdfd47ced711b6f3a500cf46b18`  
		Last Modified: Wed, 08 Oct 2025 23:01:43 GMT  
		Size: 52.6 MB (52635431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80efde82a398c373a6dd178d6463aceb85ec43479b2cfdba7a1dbb3264ccf54b`  
		Last Modified: Wed, 08 Oct 2025 23:01:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422c395a04785ec7594c0d066c8c5f036590188e16d23ab4ec4198e02b9c4f00`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:730b8f0dea849c083253744a315ec021c0dcccfbb8e9de659121ad31edf7ec34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1119559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff21e32b41bd115a92e0ae73dea1e88d306701cf86e15c9afcc7bfb8a9aacf9`

```dockerfile
```

-	Layers:
	-	`sha256:b6a1d8d8055fb2071db8f621433deb0ad103364d17f01678de58f0c88174846f`  
		Last Modified: Thu, 09 Oct 2025 00:18:25 GMT  
		Size: 1.1 MB (1100805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a2e65a74e400f7e41070d1c4b83ac5262dfe4efab12fd7ad745a832d496031`  
		Last Modified: Thu, 09 Oct 2025 00:18:26 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
