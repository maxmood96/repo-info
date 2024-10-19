<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.34`](#orientdb3234)
-	[`orientdb:3.2.34-tp3`](#orientdb3234-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:b82d771c184c96db9c59685d9aa5935281b27e2b691bb50736d14ffb66ceee5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:7d9397e044c9359171f73641cd419fd25fc8680cfca1cf3664b9fed859126be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200217252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb69838ee3c31e2cfa9edf0cd117cbfda7e3c2da2b413e83e8efe66c600a2d31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 15 Sep 2022 13:05:16 GMT
ARG RELEASE
# Thu, 15 Sep 2022 13:05:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 15 Sep 2022 13:05:16 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Sep 2022 13:05:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 15 Sep 2022 13:05:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 15 Sep 2022 13:05:16 GMT
WORKDIR /orientdb
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2424/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2480/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0129195fc42071fd03ba89c8d373c8eafc06279d6bc65ef52e18c93c7fd2dbe7`  
		Last Modified: Sat, 19 Oct 2024 02:56:56 GMT  
		Size: 53.1 MB (53081033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:a1cfa8978d0df6edf61237d1c914ae1be611ef4a648e1df930c583872436f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3308892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6537fcb6865db68d5e4b60f3f2ad7cc28ead9e40f0fa6f3efd89d0b8096057`

```dockerfile
```

-	Layers:
	-	`sha256:db43e8a1d00f25f18305baac95013372d614877fce99beeb85b64104aac204f1`  
		Last Modified: Sat, 19 Oct 2024 02:56:55 GMT  
		Size: 3.3 MB (3294676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717426a3f10b5d8532bdf60995a5d0d3184fb8f3923f42671f44f44a8cb6cf42`  
		Last Modified: Sat, 19 Oct 2024 02:56:55 GMT  
		Size: 14.2 KB (14216 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:3d0691a186c2fb77daa38d46853f5ed9e3c2f8feac7016b7cfa946565b5697df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:d98991bff282487caa9bb5651895b93a669a0e7452a75a5bb23de081fbb0bcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223224336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c01f8574ebca892deb085ea3ab237961d427c2efebb35b9199e6a495328c82b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 15 Sep 2022 13:05:16 GMT
ARG RELEASE
# Thu, 15 Sep 2022 13:05:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 15 Sep 2022 13:05:16 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Sep 2022 13:05:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 15 Sep 2022 13:05:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 15 Sep 2022 13:05:16 GMT
WORKDIR /orientdb
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2424/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2480/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[8182/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8e1090143c3cf6541e436ee00fe4b010a6433bb8fc61da7846bbe350ed4168`  
		Last Modified: Sat, 19 Oct 2024 02:57:14 GMT  
		Size: 76.1 MB (76086744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98e1b7def1c867d2c0f2f84c58d4d6aabf0baddc2dc5ecb20779fc966a4ea`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:24688b7a391408130125fe1b55ba4d23ac84801a6427edb6c1bafe0c3b6b7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ece4ac9b6fa97b361162106ad062518f7c569131f4a51c0b628b1936aa552e`

```dockerfile
```

-	Layers:
	-	`sha256:be0256115c00c7647da14fe8d6f06425bae4708b03aec098f2d34f22262c4df5`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 3.4 MB (3357218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77ce63e16ea6219408a57b296f7419a36b4c433da1fe34d96bfb59d9a7264fb`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 16.8 KB (16848 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:b82d771c184c96db9c59685d9aa5935281b27e2b691bb50736d14ffb66ceee5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:7d9397e044c9359171f73641cd419fd25fc8680cfca1cf3664b9fed859126be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200217252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb69838ee3c31e2cfa9edf0cd117cbfda7e3c2da2b413e83e8efe66c600a2d31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 15 Sep 2022 13:05:16 GMT
ARG RELEASE
# Thu, 15 Sep 2022 13:05:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 15 Sep 2022 13:05:16 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Sep 2022 13:05:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 15 Sep 2022 13:05:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 15 Sep 2022 13:05:16 GMT
WORKDIR /orientdb
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2424/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2480/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0129195fc42071fd03ba89c8d373c8eafc06279d6bc65ef52e18c93c7fd2dbe7`  
		Last Modified: Sat, 19 Oct 2024 02:56:56 GMT  
		Size: 53.1 MB (53081033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:a1cfa8978d0df6edf61237d1c914ae1be611ef4a648e1df930c583872436f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3308892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6537fcb6865db68d5e4b60f3f2ad7cc28ead9e40f0fa6f3efd89d0b8096057`

```dockerfile
```

-	Layers:
	-	`sha256:db43e8a1d00f25f18305baac95013372d614877fce99beeb85b64104aac204f1`  
		Last Modified: Sat, 19 Oct 2024 02:56:55 GMT  
		Size: 3.3 MB (3294676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717426a3f10b5d8532bdf60995a5d0d3184fb8f3923f42671f44f44a8cb6cf42`  
		Last Modified: Sat, 19 Oct 2024 02:56:55 GMT  
		Size: 14.2 KB (14216 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:3d0691a186c2fb77daa38d46853f5ed9e3c2f8feac7016b7cfa946565b5697df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:d98991bff282487caa9bb5651895b93a669a0e7452a75a5bb23de081fbb0bcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223224336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c01f8574ebca892deb085ea3ab237961d427c2efebb35b9199e6a495328c82b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 15 Sep 2022 13:05:16 GMT
ARG RELEASE
# Thu, 15 Sep 2022 13:05:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Sep 2022 13:05:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 15 Sep 2022 13:05:16 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Sep 2022 13:05:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 15 Sep 2022 13:05:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 15 Sep 2022 13:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 15 Sep 2022 13:05:16 GMT
WORKDIR /orientdb
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2424/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[2480/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
EXPOSE map[8182/tcp:{}]
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8e1090143c3cf6541e436ee00fe4b010a6433bb8fc61da7846bbe350ed4168`  
		Last Modified: Sat, 19 Oct 2024 02:57:14 GMT  
		Size: 76.1 MB (76086744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98e1b7def1c867d2c0f2f84c58d4d6aabf0baddc2dc5ecb20779fc966a4ea`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:24688b7a391408130125fe1b55ba4d23ac84801a6427edb6c1bafe0c3b6b7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ece4ac9b6fa97b361162106ad062518f7c569131f4a51c0b628b1936aa552e`

```dockerfile
```

-	Layers:
	-	`sha256:be0256115c00c7647da14fe8d6f06425bae4708b03aec098f2d34f22262c4df5`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 3.4 MB (3357218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77ce63e16ea6219408a57b296f7419a36b4c433da1fe34d96bfb59d9a7264fb`  
		Last Modified: Sat, 19 Oct 2024 02:57:13 GMT  
		Size: 16.8 KB (16848 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:c018bea1297655d82668a3e527247a54499ccd8f991bd63107ef0e9be238450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:36203788c94a1c323bae5381d38c4b134cad0cffd7f91de7e7e86ae852606da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220060547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfac5c2306cf7a7cd71d2a64558074f3a80c4cd85984345bcc29ea7cddcf9049`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292fd68a032b7ae16c31af75a59bd48b8692911df7f6fb4ef5befaef2ab25c2`  
		Last Modified: Sat, 19 Oct 2024 02:54:52 GMT  
		Size: 72.9 MB (72924328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:f82d32ce3b2efb7f8b314404c08412dc97a7d53dae841bf9bc7a38d8e83b19cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09792b014915fcf5eb9b0a07942adaf04831656f54824d57ceb02024618e69`

```dockerfile
```

-	Layers:
	-	`sha256:01e9f9da7633f8eee965fdf47d8c9bb1bb546a87e755ceddc47f5f46b63b8e9e`  
		Last Modified: Sat, 19 Oct 2024 02:54:50 GMT  
		Size: 3.3 MB (3303618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77685ec0194c4c42bc46a16b5e7141e369c2378ba7d0daba6953e769d2e00f4`  
		Last Modified: Sat, 19 Oct 2024 02:54:49 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:94b6815fe34ec5125871124b34212e23155e51a3d008f45a496f03c3bcfba583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212868235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a98911a2ad833d32b2304bebaeaaaeaddf7bd669df8bfb40cc31531218ac567`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2985aa13654dd1cf219d1650174d7f1e079faced490096c0ce7b5778b58a7a9d`  
		Last Modified: Sat, 19 Oct 2024 06:52:37 GMT  
		Size: 13.1 MB (13134217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02f87539f2467477a585c1a57a4b5ee24edb33ed640743175a3927841bdce8`  
		Last Modified: Sat, 19 Oct 2024 06:52:39 GMT  
		Size: 99.9 MB (99941321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c728da7ad31cc052ceab07c4b667234781f9e9b1d931c1b0f0fef206009cfc`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f6d3dca019027cacfe20cdcafebea7b6f49548a25940dafe4ab21e7c1d05`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ef5e7ccaf6fa3e22a57d4133e52034e0eebb39990ff91ed0aec6aa126c480`  
		Last Modified: Sat, 19 Oct 2024 09:38:55 GMT  
		Size: 72.9 MB (72924324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:781d29f9867fad17751e2e7484d4e30ad19e69cd75013caea04d9c631280b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efff4403c24aacbdfd2850cad0ac802d8267bb059f092f3c02f98e90cef04d7`

```dockerfile
```

-	Layers:
	-	`sha256:28a84aea9c8a1147775fc7df229b76c115480acb2341d072f86870a618226c2c`  
		Last Modified: Sat, 19 Oct 2024 09:38:52 GMT  
		Size: 3.3 MB (3307312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efaf0b73243245abcd69009bab7be64ea4719a8860b40a5f60a99660c13f0011`  
		Last Modified: Sat, 19 Oct 2024 09:38:50 GMT  
		Size: 14.6 KB (14594 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:900b023646a0189a0468269caf8862a32fac2488b9dfe2d97661d90883d3b8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218341740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce226f150a0ae658c4bc000b6c643c1295df84375ea1eb0a4dfa5c87c74811c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086fac5a6f132071668768424cfa681e0d46064f3b5b758bc8de7243abe745`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 102.7 MB (102733182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ef5a479c7afc017c3c7a22550f53bc13be002fe299c8b59ff21ebc4bd86a`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a89397a504e8c0a20400d197991e8b9827fe8263ac037154a0c6ed55fed7f5`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c20249df6e24e6630d77a290b60913a0d29a3f21950a15378d0328964a7f91`  
		Last Modified: Sat, 19 Oct 2024 09:02:10 GMT  
		Size: 72.9 MB (72924321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:436efcef610ccaf3a7d76ee405cca0c8eb471080b512c64b881ebafac6cf36b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1b4976d867c47fc1ae7359d990a673e23d9f3802a5de9e9783a0a67d63b2a`

```dockerfile
```

-	Layers:
	-	`sha256:033e454db17a0d4dc9c7bc8cd81c452bc21450f4d5402a1be222b0fb38a30f08`  
		Last Modified: Sat, 19 Oct 2024 09:02:08 GMT  
		Size: 3.3 MB (3304771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826741f899193ccbbfe0ca253bef09332a3d8a952561b249d744046db8b6d10`  
		Last Modified: Sat, 19 Oct 2024 09:02:07 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:ca05d4c11c21cc53dc68d8a9edc06899bbcaf77996ae881674a83c2332906744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:b2273d5fd1a213760e68435bedf8d1285a4dd5d0006d21f99976903f9e868f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251989434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209c9ee1653e2edd37c9f8d87579378c780779ae209d4df4510a63c1d242802b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd133e0608d07b8da586c1f5ee59428444e9a37893a72bae2cfda2239b9eb6`  
		Last Modified: Sat, 19 Oct 2024 02:54:49 GMT  
		Size: 104.9 MB (104851893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641633a4aeaf4c4490b6b76e18fe094b3268d37ace7c034c52a604a9805b7be1`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:1947ed189cdf763fc0c24f6ae8d6fc90ded63df5349be85fc5cf65fd26d4dddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e93719fdae5c31afeb2eb34d70e5ba3a2c4496ea6c87626bd7ef29fc91a4b`

```dockerfile
```

-	Layers:
	-	`sha256:775346f1020cbc074eca4043901f900aba257bcef8b7413fdd4afd9be013fde0`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 3.4 MB (3437663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30193d1409e16e274f4269ba146596fbdf643f8ec7a452a4b319b661f57ad8a3`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 16.9 KB (16851 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:cccc221da56f786added117dbbc91dce239d9f5c3ae8986eccefec8260b30d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244797159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cf9a12da554e1de835f3a2aceeaa547ac887b180dce7bdf68a9eb8ed006b31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2985aa13654dd1cf219d1650174d7f1e079faced490096c0ce7b5778b58a7a9d`  
		Last Modified: Sat, 19 Oct 2024 06:52:37 GMT  
		Size: 13.1 MB (13134217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02f87539f2467477a585c1a57a4b5ee24edb33ed640743175a3927841bdce8`  
		Last Modified: Sat, 19 Oct 2024 06:52:39 GMT  
		Size: 99.9 MB (99941321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c728da7ad31cc052ceab07c4b667234781f9e9b1d931c1b0f0fef206009cfc`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f6d3dca019027cacfe20cdcafebea7b6f49548a25940dafe4ab21e7c1d05`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86fa1eb2163f19848209bb246a9e41bb3fecc08b7651129f520136b481bd37c`  
		Last Modified: Sat, 19 Oct 2024 09:40:40 GMT  
		Size: 104.9 MB (104851927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524fadad4f058d691b71966bca16f6a40ef5f70dc95b2e2684384399df0eae78`  
		Last Modified: Sat, 19 Oct 2024 09:40:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0132aac6ec9241b4b9f0bb22865a38267ad1cfe1d807323b1dbde2fc1b265493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd238748a0416aa4a6a0e41c856e3d7f22bab73a870129c351d9b1c50d16147`

```dockerfile
```

-	Layers:
	-	`sha256:f1c986e5e3c2c0b142f290f5d64c6a8ecb0b8886e163d16f201ed48b47d70088`  
		Last Modified: Sat, 19 Oct 2024 09:40:37 GMT  
		Size: 3.4 MB (3441349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcb94ebb88e24846784960f3d53852f083499c1167899dcb1a5b79e410bee26`  
		Last Modified: Sat, 19 Oct 2024 09:40:36 GMT  
		Size: 16.9 KB (16919 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:f1c38a3086ba5c8a8c4e83b8af63960f1dcf4b3ab4abc51f88b90bf7f41c5bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250270621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddffb46a4de6759015b4460452e5bdd618aac14ebd50853a47afdad06323c926`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086fac5a6f132071668768424cfa681e0d46064f3b5b758bc8de7243abe745`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 102.7 MB (102733182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ef5a479c7afc017c3c7a22550f53bc13be002fe299c8b59ff21ebc4bd86a`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a89397a504e8c0a20400d197991e8b9827fe8263ac037154a0c6ed55fed7f5`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90746004d2e96288247b767122ad5b0de10cadb96e5fdef38b2cbb60f40b7806`  
		Last Modified: Sat, 19 Oct 2024 09:03:20 GMT  
		Size: 104.9 MB (104851883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79cb1d770a2f68a63f209b8e3386980e54b6865dc34d485bfb0115e0015ac5`  
		Last Modified: Sat, 19 Oct 2024 09:03:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:a789afac838f79e305037c777fd4d32ad47f404e18ed3be84819b14321f7f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3455750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fcfa5b49ada9056eb0fac69991ba58a3d6120dee387517845890a0fb2ee27`

```dockerfile
```

-	Layers:
	-	`sha256:5577c033e43d853bc7b707b1f3f31863411a584c13860a9081408cdece68d1e8`  
		Last Modified: Sat, 19 Oct 2024 09:03:18 GMT  
		Size: 3.4 MB (3438804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15834a37c27d37b64913f6a5535de4afe646d96505d404bddc1043b555cacb32`  
		Last Modified: Sat, 19 Oct 2024 09:03:17 GMT  
		Size: 16.9 KB (16946 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.34`

```console
$ docker pull orientdb@sha256:c018bea1297655d82668a3e527247a54499ccd8f991bd63107ef0e9be238450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.34` - linux; amd64

```console
$ docker pull orientdb@sha256:36203788c94a1c323bae5381d38c4b134cad0cffd7f91de7e7e86ae852606da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220060547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfac5c2306cf7a7cd71d2a64558074f3a80c4cd85984345bcc29ea7cddcf9049`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292fd68a032b7ae16c31af75a59bd48b8692911df7f6fb4ef5befaef2ab25c2`  
		Last Modified: Sat, 19 Oct 2024 02:54:52 GMT  
		Size: 72.9 MB (72924328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:f82d32ce3b2efb7f8b314404c08412dc97a7d53dae841bf9bc7a38d8e83b19cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09792b014915fcf5eb9b0a07942adaf04831656f54824d57ceb02024618e69`

```dockerfile
```

-	Layers:
	-	`sha256:01e9f9da7633f8eee965fdf47d8c9bb1bb546a87e755ceddc47f5f46b63b8e9e`  
		Last Modified: Sat, 19 Oct 2024 02:54:50 GMT  
		Size: 3.3 MB (3303618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77685ec0194c4c42bc46a16b5e7141e369c2378ba7d0daba6953e769d2e00f4`  
		Last Modified: Sat, 19 Oct 2024 02:54:49 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:94b6815fe34ec5125871124b34212e23155e51a3d008f45a496f03c3bcfba583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212868235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a98911a2ad833d32b2304bebaeaaaeaddf7bd669df8bfb40cc31531218ac567`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2985aa13654dd1cf219d1650174d7f1e079faced490096c0ce7b5778b58a7a9d`  
		Last Modified: Sat, 19 Oct 2024 06:52:37 GMT  
		Size: 13.1 MB (13134217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02f87539f2467477a585c1a57a4b5ee24edb33ed640743175a3927841bdce8`  
		Last Modified: Sat, 19 Oct 2024 06:52:39 GMT  
		Size: 99.9 MB (99941321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c728da7ad31cc052ceab07c4b667234781f9e9b1d931c1b0f0fef206009cfc`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f6d3dca019027cacfe20cdcafebea7b6f49548a25940dafe4ab21e7c1d05`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ef5e7ccaf6fa3e22a57d4133e52034e0eebb39990ff91ed0aec6aa126c480`  
		Last Modified: Sat, 19 Oct 2024 09:38:55 GMT  
		Size: 72.9 MB (72924324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:781d29f9867fad17751e2e7484d4e30ad19e69cd75013caea04d9c631280b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efff4403c24aacbdfd2850cad0ac802d8267bb059f092f3c02f98e90cef04d7`

```dockerfile
```

-	Layers:
	-	`sha256:28a84aea9c8a1147775fc7df229b76c115480acb2341d072f86870a618226c2c`  
		Last Modified: Sat, 19 Oct 2024 09:38:52 GMT  
		Size: 3.3 MB (3307312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efaf0b73243245abcd69009bab7be64ea4719a8860b40a5f60a99660c13f0011`  
		Last Modified: Sat, 19 Oct 2024 09:38:50 GMT  
		Size: 14.6 KB (14594 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:900b023646a0189a0468269caf8862a32fac2488b9dfe2d97661d90883d3b8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218341740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce226f150a0ae658c4bc000b6c643c1295df84375ea1eb0a4dfa5c87c74811c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086fac5a6f132071668768424cfa681e0d46064f3b5b758bc8de7243abe745`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 102.7 MB (102733182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ef5a479c7afc017c3c7a22550f53bc13be002fe299c8b59ff21ebc4bd86a`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a89397a504e8c0a20400d197991e8b9827fe8263ac037154a0c6ed55fed7f5`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c20249df6e24e6630d77a290b60913a0d29a3f21950a15378d0328964a7f91`  
		Last Modified: Sat, 19 Oct 2024 09:02:10 GMT  
		Size: 72.9 MB (72924321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:436efcef610ccaf3a7d76ee405cca0c8eb471080b512c64b881ebafac6cf36b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1b4976d867c47fc1ae7359d990a673e23d9f3802a5de9e9783a0a67d63b2a`

```dockerfile
```

-	Layers:
	-	`sha256:033e454db17a0d4dc9c7bc8cd81c452bc21450f4d5402a1be222b0fb38a30f08`  
		Last Modified: Sat, 19 Oct 2024 09:02:08 GMT  
		Size: 3.3 MB (3304771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826741f899193ccbbfe0ca253bef09332a3d8a952561b249d744046db8b6d10`  
		Last Modified: Sat, 19 Oct 2024 09:02:07 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.34-tp3`

```console
$ docker pull orientdb@sha256:ca05d4c11c21cc53dc68d8a9edc06899bbcaf77996ae881674a83c2332906744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.34-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:b2273d5fd1a213760e68435bedf8d1285a4dd5d0006d21f99976903f9e868f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251989434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209c9ee1653e2edd37c9f8d87579378c780779ae209d4df4510a63c1d242802b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd133e0608d07b8da586c1f5ee59428444e9a37893a72bae2cfda2239b9eb6`  
		Last Modified: Sat, 19 Oct 2024 02:54:49 GMT  
		Size: 104.9 MB (104851893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641633a4aeaf4c4490b6b76e18fe094b3268d37ace7c034c52a604a9805b7be1`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:1947ed189cdf763fc0c24f6ae8d6fc90ded63df5349be85fc5cf65fd26d4dddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e93719fdae5c31afeb2eb34d70e5ba3a2c4496ea6c87626bd7ef29fc91a4b`

```dockerfile
```

-	Layers:
	-	`sha256:775346f1020cbc074eca4043901f900aba257bcef8b7413fdd4afd9be013fde0`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 3.4 MB (3437663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30193d1409e16e274f4269ba146596fbdf643f8ec7a452a4b319b661f57ad8a3`  
		Last Modified: Sat, 19 Oct 2024 02:54:48 GMT  
		Size: 16.9 KB (16851 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:cccc221da56f786added117dbbc91dce239d9f5c3ae8986eccefec8260b30d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244797159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cf9a12da554e1de835f3a2aceeaa547ac887b180dce7bdf68a9eb8ed006b31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2985aa13654dd1cf219d1650174d7f1e079faced490096c0ce7b5778b58a7a9d`  
		Last Modified: Sat, 19 Oct 2024 06:52:37 GMT  
		Size: 13.1 MB (13134217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02f87539f2467477a585c1a57a4b5ee24edb33ed640743175a3927841bdce8`  
		Last Modified: Sat, 19 Oct 2024 06:52:39 GMT  
		Size: 99.9 MB (99941321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c728da7ad31cc052ceab07c4b667234781f9e9b1d931c1b0f0fef206009cfc`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f6d3dca019027cacfe20cdcafebea7b6f49548a25940dafe4ab21e7c1d05`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86fa1eb2163f19848209bb246a9e41bb3fecc08b7651129f520136b481bd37c`  
		Last Modified: Sat, 19 Oct 2024 09:40:40 GMT  
		Size: 104.9 MB (104851927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524fadad4f058d691b71966bca16f6a40ef5f70dc95b2e2684384399df0eae78`  
		Last Modified: Sat, 19 Oct 2024 09:40:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0132aac6ec9241b4b9f0bb22865a38267ad1cfe1d807323b1dbde2fc1b265493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd238748a0416aa4a6a0e41c856e3d7f22bab73a870129c351d9b1c50d16147`

```dockerfile
```

-	Layers:
	-	`sha256:f1c986e5e3c2c0b142f290f5d64c6a8ecb0b8886e163d16f201ed48b47d70088`  
		Last Modified: Sat, 19 Oct 2024 09:40:37 GMT  
		Size: 3.4 MB (3441349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcb94ebb88e24846784960f3d53852f083499c1167899dcb1a5b79e410bee26`  
		Last Modified: Sat, 19 Oct 2024 09:40:36 GMT  
		Size: 16.9 KB (16919 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:f1c38a3086ba5c8a8c4e83b8af63960f1dcf4b3ab4abc51f88b90bf7f41c5bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250270621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddffb46a4de6759015b4460452e5bdd618aac14ebd50853a47afdad06323c926`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=95b2b7c6656555ea64bb034f6ee9d3fb
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad9ca5f37176843614a5373361734dab22efbaad
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.34/orientdb-tp3-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086fac5a6f132071668768424cfa681e0d46064f3b5b758bc8de7243abe745`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 102.7 MB (102733182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ef5a479c7afc017c3c7a22550f53bc13be002fe299c8b59ff21ebc4bd86a`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a89397a504e8c0a20400d197991e8b9827fe8263ac037154a0c6ed55fed7f5`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90746004d2e96288247b767122ad5b0de10cadb96e5fdef38b2cbb60f40b7806`  
		Last Modified: Sat, 19 Oct 2024 09:03:20 GMT  
		Size: 104.9 MB (104851883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79cb1d770a2f68a63f209b8e3386980e54b6865dc34d485bfb0115e0015ac5`  
		Last Modified: Sat, 19 Oct 2024 09:03:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:a789afac838f79e305037c777fd4d32ad47f404e18ed3be84819b14321f7f97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3455750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fcfa5b49ada9056eb0fac69991ba58a3d6120dee387517845890a0fb2ee27`

```dockerfile
```

-	Layers:
	-	`sha256:5577c033e43d853bc7b707b1f3f31863411a584c13860a9081408cdece68d1e8`  
		Last Modified: Sat, 19 Oct 2024 09:03:18 GMT  
		Size: 3.4 MB (3438804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15834a37c27d37b64913f6a5535de4afe646d96505d404bddc1043b555cacb32`  
		Last Modified: Sat, 19 Oct 2024 09:03:17 GMT  
		Size: 16.9 KB (16946 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:c018bea1297655d82668a3e527247a54499ccd8f991bd63107ef0e9be238450e
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
$ docker pull orientdb@sha256:36203788c94a1c323bae5381d38c4b134cad0cffd7f91de7e7e86ae852606da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220060547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfac5c2306cf7a7cd71d2a64558074f3a80c4cd85984345bcc29ea7cddcf9049`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b515f4a925e6bfb8280322b864818398a7de753dacf663827372fb7ac67003`  
		Last Modified: Sat, 19 Oct 2024 02:06:32 GMT  
		Size: 13.8 MB (13767635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ab7ec6310524f4e79b401b70e11c34f4d6fbdcde4474dc096d491c21c3123`  
		Last Modified: Sat, 19 Oct 2024 02:06:33 GMT  
		Size: 103.6 MB (103615897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b76f9ed28d911ee651bc6c2159010096f5e60db6041619c407f3589cda62d9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa296ae3a48857171a0b67f74b3e376415c3de671e3aac0383dd0237375184c9`  
		Last Modified: Sat, 19 Oct 2024 02:06:31 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292fd68a032b7ae16c31af75a59bd48b8692911df7f6fb4ef5befaef2ab25c2`  
		Last Modified: Sat, 19 Oct 2024 02:54:52 GMT  
		Size: 72.9 MB (72924328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:f82d32ce3b2efb7f8b314404c08412dc97a7d53dae841bf9bc7a38d8e83b19cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3318135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09792b014915fcf5eb9b0a07942adaf04831656f54824d57ceb02024618e69`

```dockerfile
```

-	Layers:
	-	`sha256:01e9f9da7633f8eee965fdf47d8c9bb1bb546a87e755ceddc47f5f46b63b8e9e`  
		Last Modified: Sat, 19 Oct 2024 02:54:50 GMT  
		Size: 3.3 MB (3303618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77685ec0194c4c42bc46a16b5e7141e369c2378ba7d0daba6953e769d2e00f4`  
		Last Modified: Sat, 19 Oct 2024 02:54:49 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:94b6815fe34ec5125871124b34212e23155e51a3d008f45a496f03c3bcfba583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212868235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a98911a2ad833d32b2304bebaeaaaeaddf7bd669df8bfb40cc31531218ac567`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2985aa13654dd1cf219d1650174d7f1e079faced490096c0ce7b5778b58a7a9d`  
		Last Modified: Sat, 19 Oct 2024 06:52:37 GMT  
		Size: 13.1 MB (13134217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02f87539f2467477a585c1a57a4b5ee24edb33ed640743175a3927841bdce8`  
		Last Modified: Sat, 19 Oct 2024 06:52:39 GMT  
		Size: 99.9 MB (99941321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c728da7ad31cc052ceab07c4b667234781f9e9b1d931c1b0f0fef206009cfc`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f6d3dca019027cacfe20cdcafebea7b6f49548a25940dafe4ab21e7c1d05`  
		Last Modified: Sat, 19 Oct 2024 06:52:36 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ef5e7ccaf6fa3e22a57d4133e52034e0eebb39990ff91ed0aec6aa126c480`  
		Last Modified: Sat, 19 Oct 2024 09:38:55 GMT  
		Size: 72.9 MB (72924324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:781d29f9867fad17751e2e7484d4e30ad19e69cd75013caea04d9c631280b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efff4403c24aacbdfd2850cad0ac802d8267bb059f092f3c02f98e90cef04d7`

```dockerfile
```

-	Layers:
	-	`sha256:28a84aea9c8a1147775fc7df229b76c115480acb2341d072f86870a618226c2c`  
		Last Modified: Sat, 19 Oct 2024 09:38:52 GMT  
		Size: 3.3 MB (3307312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efaf0b73243245abcd69009bab7be64ea4719a8860b40a5f60a99660c13f0011`  
		Last Modified: Sat, 19 Oct 2024 09:38:50 GMT  
		Size: 14.6 KB (14594 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:900b023646a0189a0468269caf8862a32fac2488b9dfe2d97661d90883d3b8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218341740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce226f150a0ae658c4bc000b6c643c1295df84375ea1eb0a4dfa5c87c74811c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:53:41 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Oct 2024 13:53:41 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_VERSION=3.2.34
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_MD5=27f3645f2160c8dbded573a195c522ef
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=bc3e3f33361a5e31e45bd08f77fc0d8d6d29ffd8
# Tue, 01 Oct 2024 13:53:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.34/orientdb-community-3.2.34.tar.gz
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 01 Oct 2024 13:53:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:53:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Oct 2024 13:53:41 GMT
WORKDIR /orientdb
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 01 Oct 2024 13:53:41 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086fac5a6f132071668768424cfa681e0d46064f3b5b758bc8de7243abe745`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 102.7 MB (102733182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261ef5a479c7afc017c3c7a22550f53bc13be002fe299c8b59ff21ebc4bd86a`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a89397a504e8c0a20400d197991e8b9827fe8263ac037154a0c6ed55fed7f5`  
		Last Modified: Sat, 19 Oct 2024 05:28:15 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c20249df6e24e6630d77a290b60913a0d29a3f21950a15378d0328964a7f91`  
		Last Modified: Sat, 19 Oct 2024 09:02:10 GMT  
		Size: 72.9 MB (72924321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:436efcef610ccaf3a7d76ee405cca0c8eb471080b512c64b881ebafac6cf36b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1b4976d867c47fc1ae7359d990a673e23d9f3802a5de9e9783a0a67d63b2a`

```dockerfile
```

-	Layers:
	-	`sha256:033e454db17a0d4dc9c7bc8cd81c452bc21450f4d5402a1be222b0fb38a30f08`  
		Last Modified: Sat, 19 Oct 2024 09:02:08 GMT  
		Size: 3.3 MB (3304771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826741f899193ccbbfe0ca253bef09332a3d8a952561b249d744046db8b6d10`  
		Last Modified: Sat, 19 Oct 2024 09:02:07 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json
