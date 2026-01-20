## `eclipse-temurin:8u472-b08-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:49468d326d5ee2781264201c1f7576d572e86574b5119833599d94d2df381a7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f95f0e606c423df2e209067c20e369a22d84fc3b88be2a86fc5d0a40e3fb4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61662367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46b92d8dda45ec82e08a9b6a78d1bad69c834fe831c91ca299fee545691558a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:03 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:57:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:57:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce56a8c3867406f1937de193b064d059af34be0a7419a809c30bba8cb15f263e`  
		Last Modified: Sat, 08 Nov 2025 17:57:16 GMT  
		Size: 16.2 MB (16174549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b72018aca0df60314194d61adc25b005efc926e671e9fb5a4f1b56c2c2ccbd`  
		Last Modified: Fri, 09 Jan 2026 13:26:34 GMT  
		Size: 41.8 MB (41842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022927c1be85512c6b122e5deaccc9347a3b6a4784313ff57ebc86ace488d015`  
		Last Modified: Fri, 09 Jan 2026 13:26:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cbe01d25889334223a859e1f5f43f9573b2ea5c021ed6cc95b0b6477d7b1d4`  
		Last Modified: Fri, 09 Jan 2026 13:26:30 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:af891747ba8876c5172ac5d8538771de11d179ff1e7446ae80b96eb90e627888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7f36fef97b7134a836d5f8bf47aa5889141ac0e0a34a85d03f849cd9fa4565`

```dockerfile
```

-	Layers:
	-	`sha256:43b124f6852e2cf2eb6f12676c7ca4e081dc0fd8ccfda0a222a727a16c884a5b`  
		Last Modified: Sat, 08 Nov 2025 17:57:15 GMT  
		Size: 926.8 KB (926847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e5fd93a302566fdb834af5d38f2a2319e300d3ab89994b671e39fb6ea1cd0cf`  
		Last Modified: Sat, 08 Nov 2025 17:57:15 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
