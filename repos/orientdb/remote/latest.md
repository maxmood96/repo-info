## `orientdb:latest`

```console
$ docker pull orientdb@sha256:38c6968dcc04e2c35d85495026bd751e6a9e9d60bdbeee2607103477564c1295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:058e19fc4168ca9b0f1f2d29bc92f13b3dacb0c9bc13448a3c61f346b70909ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223939521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315dfbcb6b9627b6058123ee7d48c0ee3ce68c32903bd1695997e08fe61e7a74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f4ace5897523a1a5f235b03291ebbca78294e7d42b4f1425abd38b17701303`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 17.0 MB (16966378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6e2fd4158ef247a4fe5c04d362fd5595c2dc33f06cf9ba2bb74c89568085e5`  
		Last Modified: Tue, 03 Dec 2024 02:30:22 GMT  
		Size: 103.6 MB (103632853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc6481c0f3d295d0d446995ffc41a6315dfcf19f5a7ddae1815ef95e4b9ef6b`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1559309569d4ae3c3e5925400c9677ba1e4fba6ec1256bb50e56450568393`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032df3ee1ce2e2cb1453331bed6d30335b812ffa20fb58bec27bb7233cd3c234`  
		Last Modified: Wed, 15 Jan 2025 17:50:30 GMT  
		Size: 656.9 KB (656867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d26d8aefd6c53dd291f35b71acb2eaeb8a0696ffd9d5d5dcb7df4838aedd6`  
		Last Modified: Wed, 15 Jan 2025 17:50:32 GMT  
		Size: 72.9 MB (72928986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:467e240d1cf8385ed9a8bb152a3c179eb9b29c3af65d4305e17d1b2f6c475f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d02cda268f2d51e4cb9dbd442c1082df9378cfaf5d2a96e905db4a99d23a24`

```dockerfile
```

-	Layers:
	-	`sha256:8ecfbe44b0076844383a951acd851bf035eb60f91478a98c33bfdd8c62b66ed3`  
		Last Modified: Wed, 15 Jan 2025 17:50:30 GMT  
		Size: 3.4 MB (3411790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a7dcb65f5f65a09cfe5a886c2639b453ff78da5cc1223c397837b8d410edb4`  
		Last Modified: Wed, 15 Jan 2025 17:50:29 GMT  
		Size: 14.5 KB (14530 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:8f1217771d4bfdb581e02c8f08622e70391a924c1be596c6dd4a5602e6d658d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215705616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7e0afe36d2ad31c18006f6864c8211a6cea0223ced68fab6993ba6afff925f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749c836e2b9e894569dd92b2497fc11034a22539b0b8549179b226bb62007916`  
		Last Modified: Tue, 03 Dec 2024 07:45:26 GMT  
		Size: 99.0 MB (99021657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07ef20c8a3fbef21d889c70780aeda5595558be9646c177d214c1c0e66fee13`  
		Last Modified: Tue, 03 Dec 2024 07:45:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3112e573848c0cdff0c817a6feb8c1faeaec3a5b460078df0d550c17d827c03`  
		Last Modified: Tue, 03 Dec 2024 07:45:23 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe31ed040f60affdbdc54c7683783b391e490f2fe824eb3220d363bd7541650`  
		Last Modified: Wed, 15 Jan 2025 17:44:46 GMT  
		Size: 582.9 KB (582916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0652961f965021b60f5e653d62b2c8ea02ca5be2acddcb4888995c4086d0e29`  
		Last Modified: Wed, 15 Jan 2025 17:44:48 GMT  
		Size: 72.9 MB (72929030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:fa668c94d9c6d0f5aa1152520b3452b23909a164128462e2b9e3b97f76cea37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ab132b12939dd7b0f5f666f878c216913951f561bdf3ce4dcde57197bc9dc2`

```dockerfile
```

-	Layers:
	-	`sha256:391e60b385042c841d0a91073bee92826ce85b3a89fa4b378bceb58d3d73b83f`  
		Last Modified: Wed, 15 Jan 2025 17:44:46 GMT  
		Size: 3.4 MB (3415474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aece81335207a9c588d8f28fab88c9e61d47a91d3f15563c0f6f09cad7c88516`  
		Last Modified: Wed, 15 Jan 2025 17:44:45 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:35f55e09a4e7c652f1f571e45621162403aa0fcc841dd8b12e6897f822f3f77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222203871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e55926d93c882f660908ac37b8114b9eedf6383b1c9dd565fb5a095d5bd4a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d6d39497cde5edbefcc48f9d73d53c8b5408b69b8cc70ceb265af74eba9e2`  
		Last Modified: Tue, 03 Dec 2024 05:48:36 GMT  
		Size: 17.0 MB (16981577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef877a9ea24e5ac140294ab96845b9feea9ab6611afb676e26edcdfb9ecb601`  
		Last Modified: Tue, 03 Dec 2024 05:48:38 GMT  
		Size: 102.7 MB (102747260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b80d9f36529a5228235515248d17bcfb8e5a13aaabd97794093c19e0820304`  
		Last Modified: Tue, 03 Dec 2024 05:48:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb4a92aa8e990ff80906eabc2b1380d1320f1f070f55f589d8c21589b3b83d5`  
		Last Modified: Tue, 03 Dec 2024 05:48:35 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bb6692bc7c76507d88bf6ebbfc7c4307be5bd13a89e52b19b0dc849c1febd`  
		Last Modified: Wed, 15 Jan 2025 17:52:23 GMT  
		Size: 650.9 KB (650900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40241f042e038f91490bf5de72e0c20f2125785c2bd9ef3f287bbdc157f68ef`  
		Last Modified: Wed, 15 Jan 2025 17:52:25 GMT  
		Size: 72.9 MB (72928994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:49147a8f529701877fae4803b074c70f8b3613ef15b83bad8882bd817ec8440f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3427583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f59d73c4bf4fc223f07e1882f03cae840c9647fbf5cbd5653203d89d19475f7`

```dockerfile
```

-	Layers:
	-	`sha256:a80ee7d63c654b3c91624bd4f873aba78656255a020321cd4e5c441ce27a55b6`  
		Last Modified: Wed, 15 Jan 2025 17:52:23 GMT  
		Size: 3.4 MB (3412947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb7c912690e97e23ad4c860074e9d38caeb1e6bbb3d91cda8a3930dff458a88`  
		Last Modified: Wed, 15 Jan 2025 17:52:23 GMT  
		Size: 14.6 KB (14636 bytes)  
		MIME: application/vnd.in-toto+json
