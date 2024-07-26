<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.32`](#orientdb3232)
-	[`orientdb:3.2.32-tp3`](#orientdb3232-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:31f3d688777998f45c388a89d4ddfd97f265d9bfdb77a15416331ce52fb50eeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:2c985ebe45f4bd6d32cebd1e8b50a9cfd384c9d1bcd4b297df3991380d4e90ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201031096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734a179637d4df4b3d6b46fbb50b9d2ee109faa16db5b5591131ba55feba9a9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8020affb27b82091b865c7b5a4d78a0d7bcd25f336062909fcfe16351a790`  
		Last Modified: Thu, 25 Jul 2024 19:02:57 GMT  
		Size: 53.1 MB (53081034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:86c3cbd007fb84af83875a790ce789d00f6eb1c1992b96cc33090afab345f138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659830dc38a61bd1835e4a0452333f88ba34d1346c6522d69ec207046f305202`

```dockerfile
```

-	Layers:
	-	`sha256:e561e0c8ae48349b1e7702b2cd0b75110b61b0b6300bbfa8dc39b61253c180a9`  
		Last Modified: Thu, 25 Jul 2024 19:02:56 GMT  
		Size: 3.0 MB (3022186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aab0b42e8536ff090ec9f068dd0a6504273c557e9e72e87b8acc75aa246d895`  
		Last Modified: Thu, 25 Jul 2024 19:02:56 GMT  
		Size: 14.1 KB (14109 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:f20ee1cdbb9f6b550a7767ff6a89f6daa19ee91b083c89d45cd9686d1a2a2f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8c88c2b522dc45fe459b58e54bcd03b633dff84dc658b3922af2a307bf55b6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224038174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5dc5a48a40c18764633eb9f47624f1c6d1f71bd1b31b07f9a1ebe1dba5ed90`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b6e51e320d32d33d05335e57c10ca62125bb3be50933e067f923e0f761fdb`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 76.1 MB (76086739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e60ae5b4bbe440981089a9760d0573647fa041188e36a442d639b020a64091`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:db362ebd9a6cffe75efec483d42db3acf0b513d46a87aa186e1fc39f99961d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d3c33158da49f68841cef6148253a1772553c2004a171e715881eaffd51c0`

```dockerfile
```

-	Layers:
	-	`sha256:5046976ee6b2bcd4eab7322ffba7491900b6996cc81a2187af8740b358214e6f`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 3.1 MB (3079564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef581111ac915402a4cc8ce0d7abffcb46314015131af84f4e9b2d332ee70a09`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 16.8 KB (16771 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:31f3d688777998f45c388a89d4ddfd97f265d9bfdb77a15416331ce52fb50eeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:2c985ebe45f4bd6d32cebd1e8b50a9cfd384c9d1bcd4b297df3991380d4e90ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201031096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734a179637d4df4b3d6b46fbb50b9d2ee109faa16db5b5591131ba55feba9a9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8020affb27b82091b865c7b5a4d78a0d7bcd25f336062909fcfe16351a790`  
		Last Modified: Thu, 25 Jul 2024 19:02:57 GMT  
		Size: 53.1 MB (53081034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:86c3cbd007fb84af83875a790ce789d00f6eb1c1992b96cc33090afab345f138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659830dc38a61bd1835e4a0452333f88ba34d1346c6522d69ec207046f305202`

```dockerfile
```

-	Layers:
	-	`sha256:e561e0c8ae48349b1e7702b2cd0b75110b61b0b6300bbfa8dc39b61253c180a9`  
		Last Modified: Thu, 25 Jul 2024 19:02:56 GMT  
		Size: 3.0 MB (3022186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aab0b42e8536ff090ec9f068dd0a6504273c557e9e72e87b8acc75aa246d895`  
		Last Modified: Thu, 25 Jul 2024 19:02:56 GMT  
		Size: 14.1 KB (14109 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:f20ee1cdbb9f6b550a7767ff6a89f6daa19ee91b083c89d45cd9686d1a2a2f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8c88c2b522dc45fe459b58e54bcd03b633dff84dc658b3922af2a307bf55b6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224038174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5dc5a48a40c18764633eb9f47624f1c6d1f71bd1b31b07f9a1ebe1dba5ed90`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b6e51e320d32d33d05335e57c10ca62125bb3be50933e067f923e0f761fdb`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 76.1 MB (76086739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e60ae5b4bbe440981089a9760d0573647fa041188e36a442d639b020a64091`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:db362ebd9a6cffe75efec483d42db3acf0b513d46a87aa186e1fc39f99961d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2d3c33158da49f68841cef6148253a1772553c2004a171e715881eaffd51c0`

```dockerfile
```

-	Layers:
	-	`sha256:5046976ee6b2bcd4eab7322ffba7491900b6996cc81a2187af8740b358214e6f`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 3.1 MB (3079564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef581111ac915402a4cc8ce0d7abffcb46314015131af84f4e9b2d332ee70a09`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 16.8 KB (16771 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:b0e6f938277b72a9fd39df31128be59cff817800b0542664ed8391297955f1a3
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
$ docker pull orientdb@sha256:e578a96ac69e4cdd125a4f431109f5fe041b3ebc1217e8b1423549b3e17017a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220869605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a2b49a679953634a97a1bc6ad72cef7d70f8f86ac143240ecc78aae0ec65c3`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a36a15c5f4dc89dce16e46418a68e1663d134c5a9238cfcac27c71ad4c9f7`  
		Last Modified: Thu, 25 Jul 2024 19:02:55 GMT  
		Size: 72.9 MB (72919543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:5be66020315bbf463a68e19850c9025b18b4607bf11f95fe21bf66e7ebf71a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91320df608137a1a366ed399f21c5d6ff359db57cdbfd1e88b044226f37e1d65`

```dockerfile
```

-	Layers:
	-	`sha256:aa529b75046863b5a64327e6461b2290044e775d0faa905b688176a53f5d91e9`  
		Last Modified: Thu, 25 Jul 2024 19:02:54 GMT  
		Size: 3.0 MB (3030370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d2ccb6ba4d7409b7ad33da81d83f7c07c3a54ce98031a492ce5b23fa50c8a2`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 14.4 KB (14410 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:4fdfe3ac57141b639dda6e48fbf0fbcd0b180ff68a1c83be1dda3e4b060c19ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212967838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123018baadb769e5c02d3a5286af6b7be84db47b8d09459ccb773e21199a991`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e917ab077fb82a7ac04816b8f4c7ff257ad2addfb20b86167d131f7330d5f6d`  
		Last Modified: Thu, 25 Jul 2024 18:01:20 GMT  
		Size: 99.2 MB (99224382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18368ee9304be535671f7f29d6a2c8bc369ff65cfaa9ee55c3fbbaa8e242b5e6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0599d7ee9fe2aa3d1e8ac709318f05b9f86ee97623ada55d39775a2f26bfec6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580181c590af3761b3f586887bd7e2b9d2ef3cd7ca8ee603b6e7fa741871875`  
		Last Modified: Thu, 25 Jul 2024 19:30:14 GMT  
		Size: 72.9 MB (72919502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:805abb7c6cedbaf83cfade368b15f28762caa932936f3652c980dadd978038db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6972ab1abd827c69bd16d082f12c4f9d791a7f5e42f36a0dd661af291fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:b5a51e5c196a3122f238a721a78309525a249927920467f78aecb7469805e584`  
		Last Modified: Thu, 25 Jul 2024 19:30:11 GMT  
		Size: 3.0 MB (3033097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd70320a891c93191e2f218a4bb464a4e77fdd716c7d5cff92b6f902792d023`  
		Last Modified: Thu, 25 Jul 2024 19:30:10 GMT  
		Size: 14.5 KB (14482 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:e7a2763dd1475cf544505562d99014f1c24bde8f1580a4d1e870871ef619accd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219357922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d8f8bc977b16b4b54045d112682fa1a6466102ea8f934d9df2aa9bd7709ad9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8395e5b7d47f033f4bac691cf04bc6984eea3d1b9b23014a7241caf20e156c18`  
		Last Modified: Thu, 25 Jul 2024 17:43:30 GMT  
		Size: 102.7 MB (102732963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56095ce5d70fae57595a8a9a16654b4d43926dc67eb4c199442bf6958df30`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9384d39245c0213d2b4df1b44d0d3025e87bd37d8d9bab80ac54c8e5315bd2`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbd4e47817b740f60a325e3afcbec3b981ac3eb5d8fd30a169a99e425a4b1a9`  
		Last Modified: Thu, 25 Jul 2024 22:31:44 GMT  
		Size: 72.9 MB (72919478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:da5318f6df345cfedcdc2e19c2255682d23873ce273523a463101c8ef68d97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928a4d7716574b2d6d9a3bee09f143166310069b6f97703324354adb4667cec`

```dockerfile
```

-	Layers:
	-	`sha256:bf8278eaf8deb49af17a931ffe71032f5b1b9771452b303b34e1fd846b94f882`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 3.0 MB (3031443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b36878aeb80bc7e500e8ba55f35c95cb25502b6fbf3177e753e6ce25fff3bc`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 14.7 KB (14709 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:9365d9848bc9d40d25b646382a6382b8520d42f10fc314b98e07f51401aca28a
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
$ docker pull orientdb@sha256:f336663a5f9f689919e32534f9a53db479fa7ab94e9d6d617eff594d4e189454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252797228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdab22f512175c8c3d9e21149b220f560bb997fd1b2d6f3723b2e98becad3111`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159d215cf7678db7de5ce3ebcdc0d0582e8161e379f7c894bd863322a40c62fa`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 104.8 MB (104845846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad1890c15e96fc48b8ec496e46341ae58ef45927210c68ac61bfc5440e7eed`  
		Last Modified: Thu, 25 Jul 2024 19:02:59 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:9b5b39ca245d897d384c3a746b48613628a3266489afb2fc2d4b47b0cacd0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906851ed4fb6beaa3901f878dc36922a7cc058c9805a82270da86edfc1621bcb`

```dockerfile
```

-	Layers:
	-	`sha256:6b8441d781b68db02da51d3a85e9d7441d22a2b87975e27ab24c333b92f8f03d`  
		Last Modified: Thu, 25 Jul 2024 19:03:00 GMT  
		Size: 3.2 MB (3153246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d167b402ee88805529df79f14131fdb8ee6e01af4511462a03e27ecfdb4be0`  
		Last Modified: Thu, 25 Jul 2024 19:02:59 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:23e2047082e9e3f74db0d577eb84f263347158d70b2d4521fac9c22e2382edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244895501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5241f8a7955edcb71f43d87d9ec4ca73656591d2285af7c14e1ebed9dfcefd5d`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e917ab077fb82a7ac04816b8f4c7ff257ad2addfb20b86167d131f7330d5f6d`  
		Last Modified: Thu, 25 Jul 2024 18:01:20 GMT  
		Size: 99.2 MB (99224382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18368ee9304be535671f7f29d6a2c8bc369ff65cfaa9ee55c3fbbaa8e242b5e6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0599d7ee9fe2aa3d1e8ac709318f05b9f86ee97623ada55d39775a2f26bfec6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4a6df48c891ec7c678b1960ad558426beffbc06db1588d46e4201778c69f4`  
		Last Modified: Thu, 25 Jul 2024 19:31:12 GMT  
		Size: 104.8 MB (104845847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1656aec9f0ffe2ec709d7fdbd492b6078e03b06423ba62ce166697751381b4dc`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:853f1c00c330a2df9f61938b5d3bf7ddb9c36a45e3dae7680323e79179b6a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7846716778c965e2b126ef68bfc4dce2708ca6b7383f53e6a5b7d927e4d8d4`

```dockerfile
```

-	Layers:
	-	`sha256:e74f6b223339f4d6efc03f2a11e2f0315edb5ee37d88890a1c6c019b515ac49c`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 3.2 MB (3155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df1918876381b8055dd326298dea0a048a71abf3b676410ecfc4236d6928bd6`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 16.8 KB (16836 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:2a5c4653882d6064b7837cee86a5db316008869d71d55118989efd46c9d1bbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251285620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90673dcc36a7cab3e319dbc912be4faa2f88a839b59ac2a134ed8d9cfe834f8`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8395e5b7d47f033f4bac691cf04bc6984eea3d1b9b23014a7241caf20e156c18`  
		Last Modified: Thu, 25 Jul 2024 17:43:30 GMT  
		Size: 102.7 MB (102732963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56095ce5d70fae57595a8a9a16654b4d43926dc67eb4c199442bf6958df30`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9384d39245c0213d2b4df1b44d0d3025e87bd37d8d9bab80ac54c8e5315bd2`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c1b61d8c9cb5743921eecbcd52fef56cad4ed9edac339428bfc760c8a021c`  
		Last Modified: Thu, 25 Jul 2024 22:32:48 GMT  
		Size: 104.8 MB (104845856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b249d9ba5745e4bfd41c1694074010d4d495b5f9b17f80ba4624ddb9588781`  
		Last Modified: Thu, 25 Jul 2024 22:32:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:c714681682f538960e7084a98c7566403b0b1b1f8e650a41e85fa31d8994605c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcd11417420bda2d544311983b258db2b18b04a743c96c200c452914ba57836`

```dockerfile
```

-	Layers:
	-	`sha256:aac163de55a30496a76c7e23d7a5015e43586df28f19cadac6bc2321c4b51850`  
		Last Modified: Thu, 25 Jul 2024 22:32:46 GMT  
		Size: 3.2 MB (3154308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a3d618fad3f1621c1465b8eadf8679f205d2b6fa977a5d5410d088bc3dc1eb`  
		Last Modified: Thu, 25 Jul 2024 22:32:45 GMT  
		Size: 17.1 KB (17060 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.32`

```console
$ docker pull orientdb@sha256:b0e6f938277b72a9fd39df31128be59cff817800b0542664ed8391297955f1a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.32` - linux; amd64

```console
$ docker pull orientdb@sha256:e578a96ac69e4cdd125a4f431109f5fe041b3ebc1217e8b1423549b3e17017a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220869605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a2b49a679953634a97a1bc6ad72cef7d70f8f86ac143240ecc78aae0ec65c3`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a36a15c5f4dc89dce16e46418a68e1663d134c5a9238cfcac27c71ad4c9f7`  
		Last Modified: Thu, 25 Jul 2024 19:02:55 GMT  
		Size: 72.9 MB (72919543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32` - unknown; unknown

```console
$ docker pull orientdb@sha256:5be66020315bbf463a68e19850c9025b18b4607bf11f95fe21bf66e7ebf71a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91320df608137a1a366ed399f21c5d6ff359db57cdbfd1e88b044226f37e1d65`

```dockerfile
```

-	Layers:
	-	`sha256:aa529b75046863b5a64327e6461b2290044e775d0faa905b688176a53f5d91e9`  
		Last Modified: Thu, 25 Jul 2024 19:02:54 GMT  
		Size: 3.0 MB (3030370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d2ccb6ba4d7409b7ad33da81d83f7c07c3a54ce98031a492ce5b23fa50c8a2`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 14.4 KB (14410 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:4fdfe3ac57141b639dda6e48fbf0fbcd0b180ff68a1c83be1dda3e4b060c19ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212967838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123018baadb769e5c02d3a5286af6b7be84db47b8d09459ccb773e21199a991`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e917ab077fb82a7ac04816b8f4c7ff257ad2addfb20b86167d131f7330d5f6d`  
		Last Modified: Thu, 25 Jul 2024 18:01:20 GMT  
		Size: 99.2 MB (99224382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18368ee9304be535671f7f29d6a2c8bc369ff65cfaa9ee55c3fbbaa8e242b5e6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0599d7ee9fe2aa3d1e8ac709318f05b9f86ee97623ada55d39775a2f26bfec6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580181c590af3761b3f586887bd7e2b9d2ef3cd7ca8ee603b6e7fa741871875`  
		Last Modified: Thu, 25 Jul 2024 19:30:14 GMT  
		Size: 72.9 MB (72919502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32` - unknown; unknown

```console
$ docker pull orientdb@sha256:805abb7c6cedbaf83cfade368b15f28762caa932936f3652c980dadd978038db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6972ab1abd827c69bd16d082f12c4f9d791a7f5e42f36a0dd661af291fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:b5a51e5c196a3122f238a721a78309525a249927920467f78aecb7469805e584`  
		Last Modified: Thu, 25 Jul 2024 19:30:11 GMT  
		Size: 3.0 MB (3033097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd70320a891c93191e2f218a4bb464a4e77fdd716c7d5cff92b6f902792d023`  
		Last Modified: Thu, 25 Jul 2024 19:30:10 GMT  
		Size: 14.5 KB (14482 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:e7a2763dd1475cf544505562d99014f1c24bde8f1580a4d1e870871ef619accd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219357922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d8f8bc977b16b4b54045d112682fa1a6466102ea8f934d9df2aa9bd7709ad9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8395e5b7d47f033f4bac691cf04bc6984eea3d1b9b23014a7241caf20e156c18`  
		Last Modified: Thu, 25 Jul 2024 17:43:30 GMT  
		Size: 102.7 MB (102732963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56095ce5d70fae57595a8a9a16654b4d43926dc67eb4c199442bf6958df30`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9384d39245c0213d2b4df1b44d0d3025e87bd37d8d9bab80ac54c8e5315bd2`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbd4e47817b740f60a325e3afcbec3b981ac3eb5d8fd30a169a99e425a4b1a9`  
		Last Modified: Thu, 25 Jul 2024 22:31:44 GMT  
		Size: 72.9 MB (72919478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32` - unknown; unknown

```console
$ docker pull orientdb@sha256:da5318f6df345cfedcdc2e19c2255682d23873ce273523a463101c8ef68d97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928a4d7716574b2d6d9a3bee09f143166310069b6f97703324354adb4667cec`

```dockerfile
```

-	Layers:
	-	`sha256:bf8278eaf8deb49af17a931ffe71032f5b1b9771452b303b34e1fd846b94f882`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 3.0 MB (3031443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b36878aeb80bc7e500e8ba55f35c95cb25502b6fbf3177e753e6ce25fff3bc`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 14.7 KB (14709 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.32-tp3`

```console
$ docker pull orientdb@sha256:9365d9848bc9d40d25b646382a6382b8520d42f10fc314b98e07f51401aca28a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.32-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:f336663a5f9f689919e32534f9a53db479fa7ab94e9d6d617eff594d4e189454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252797228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdab22f512175c8c3d9e21149b220f560bb997fd1b2d6f3723b2e98becad3111`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159d215cf7678db7de5ce3ebcdc0d0582e8161e379f7c894bd863322a40c62fa`  
		Last Modified: Thu, 25 Jul 2024 19:03:01 GMT  
		Size: 104.8 MB (104845846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad1890c15e96fc48b8ec496e46341ae58ef45927210c68ac61bfc5440e7eed`  
		Last Modified: Thu, 25 Jul 2024 19:02:59 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:9b5b39ca245d897d384c3a746b48613628a3266489afb2fc2d4b47b0cacd0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906851ed4fb6beaa3901f878dc36922a7cc058c9805a82270da86edfc1621bcb`

```dockerfile
```

-	Layers:
	-	`sha256:6b8441d781b68db02da51d3a85e9d7441d22a2b87975e27ab24c333b92f8f03d`  
		Last Modified: Thu, 25 Jul 2024 19:03:00 GMT  
		Size: 3.2 MB (3153246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d167b402ee88805529df79f14131fdb8ee6e01af4511462a03e27ecfdb4be0`  
		Last Modified: Thu, 25 Jul 2024 19:02:59 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:23e2047082e9e3f74db0d577eb84f263347158d70b2d4521fac9c22e2382edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244895501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5241f8a7955edcb71f43d87d9ec4ca73656591d2285af7c14e1ebed9dfcefd5d`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e917ab077fb82a7ac04816b8f4c7ff257ad2addfb20b86167d131f7330d5f6d`  
		Last Modified: Thu, 25 Jul 2024 18:01:20 GMT  
		Size: 99.2 MB (99224382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18368ee9304be535671f7f29d6a2c8bc369ff65cfaa9ee55c3fbbaa8e242b5e6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0599d7ee9fe2aa3d1e8ac709318f05b9f86ee97623ada55d39775a2f26bfec6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4a6df48c891ec7c678b1960ad558426beffbc06db1588d46e4201778c69f4`  
		Last Modified: Thu, 25 Jul 2024 19:31:12 GMT  
		Size: 104.8 MB (104845847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1656aec9f0ffe2ec709d7fdbd492b6078e03b06423ba62ce166697751381b4dc`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:853f1c00c330a2df9f61938b5d3bf7ddb9c36a45e3dae7680323e79179b6a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7846716778c965e2b126ef68bfc4dce2708ca6b7383f53e6a5b7d927e4d8d4`

```dockerfile
```

-	Layers:
	-	`sha256:e74f6b223339f4d6efc03f2a11e2f0315edb5ee37d88890a1c6c019b515ac49c`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 3.2 MB (3155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df1918876381b8055dd326298dea0a048a71abf3b676410ecfc4236d6928bd6`  
		Last Modified: Thu, 25 Jul 2024 19:31:09 GMT  
		Size: 16.8 KB (16836 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:2a5c4653882d6064b7837cee86a5db316008869d71d55118989efd46c9d1bbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251285620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90673dcc36a7cab3e319dbc912be4faa2f88a839b59ac2a134ed8d9cfe834f8`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=fdce9f6942302aeaab2e9b6e660a9de5
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7c9c8a0374ce34f2b18e67b2599a192e69693f5a
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.32/orientdb-tp3-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8395e5b7d47f033f4bac691cf04bc6984eea3d1b9b23014a7241caf20e156c18`  
		Last Modified: Thu, 25 Jul 2024 17:43:30 GMT  
		Size: 102.7 MB (102732963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56095ce5d70fae57595a8a9a16654b4d43926dc67eb4c199442bf6958df30`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9384d39245c0213d2b4df1b44d0d3025e87bd37d8d9bab80ac54c8e5315bd2`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c1b61d8c9cb5743921eecbcd52fef56cad4ed9edac339428bfc760c8a021c`  
		Last Modified: Thu, 25 Jul 2024 22:32:48 GMT  
		Size: 104.8 MB (104845856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b249d9ba5745e4bfd41c1694074010d4d495b5f9b17f80ba4624ddb9588781`  
		Last Modified: Thu, 25 Jul 2024 22:32:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:c714681682f538960e7084a98c7566403b0b1b1f8e650a41e85fa31d8994605c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcd11417420bda2d544311983b258db2b18b04a743c96c200c452914ba57836`

```dockerfile
```

-	Layers:
	-	`sha256:aac163de55a30496a76c7e23d7a5015e43586df28f19cadac6bc2321c4b51850`  
		Last Modified: Thu, 25 Jul 2024 22:32:46 GMT  
		Size: 3.2 MB (3154308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a3d618fad3f1621c1465b8eadf8679f205d2b6fa977a5d5410d088bc3dc1eb`  
		Last Modified: Thu, 25 Jul 2024 22:32:45 GMT  
		Size: 17.1 KB (17060 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:b0e6f938277b72a9fd39df31128be59cff817800b0542664ed8391297955f1a3
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
$ docker pull orientdb@sha256:e578a96ac69e4cdd125a4f431109f5fe041b3ebc1217e8b1423549b3e17017a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220869605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a2b49a679953634a97a1bc6ad72cef7d70f8f86ac143240ecc78aae0ec65c3`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55d88f04bf6e53e31c50e8904474abf585146e213f83eb1b8aba53ad27570f`  
		Last Modified: Thu, 25 Jul 2024 17:26:28 GMT  
		Size: 103.6 MB (103615781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f388e28887d5f3234eeaadc2fdd280a1b22a1382f370654fa99346c3b71f54`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024263359e4a317547cbcd2570c107c54e4f1e415ce06f8b7746f95dbd6076a`  
		Last Modified: Thu, 25 Jul 2024 17:26:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a36a15c5f4dc89dce16e46418a68e1663d134c5a9238cfcac27c71ad4c9f7`  
		Last Modified: Thu, 25 Jul 2024 19:02:55 GMT  
		Size: 72.9 MB (72919543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:5be66020315bbf463a68e19850c9025b18b4607bf11f95fe21bf66e7ebf71a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91320df608137a1a366ed399f21c5d6ff359db57cdbfd1e88b044226f37e1d65`

```dockerfile
```

-	Layers:
	-	`sha256:aa529b75046863b5a64327e6461b2290044e775d0faa905b688176a53f5d91e9`  
		Last Modified: Thu, 25 Jul 2024 19:02:54 GMT  
		Size: 3.0 MB (3030370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d2ccb6ba4d7409b7ad33da81d83f7c07c3a54ce98031a492ce5b23fa50c8a2`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 14.4 KB (14410 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:4fdfe3ac57141b639dda6e48fbf0fbcd0b180ff68a1c83be1dda3e4b060c19ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212967838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123018baadb769e5c02d3a5286af6b7be84db47b8d09459ccb773e21199a991`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e917ab077fb82a7ac04816b8f4c7ff257ad2addfb20b86167d131f7330d5f6d`  
		Last Modified: Thu, 25 Jul 2024 18:01:20 GMT  
		Size: 99.2 MB (99224382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18368ee9304be535671f7f29d6a2c8bc369ff65cfaa9ee55c3fbbaa8e242b5e6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0599d7ee9fe2aa3d1e8ac709318f05b9f86ee97623ada55d39775a2f26bfec6`  
		Last Modified: Thu, 25 Jul 2024 18:01:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580181c590af3761b3f586887bd7e2b9d2ef3cd7ca8ee603b6e7fa741871875`  
		Last Modified: Thu, 25 Jul 2024 19:30:14 GMT  
		Size: 72.9 MB (72919502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:805abb7c6cedbaf83cfade368b15f28762caa932936f3652c980dadd978038db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb6972ab1abd827c69bd16d082f12c4f9d791a7f5e42f36a0dd661af291fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:b5a51e5c196a3122f238a721a78309525a249927920467f78aecb7469805e584`  
		Last Modified: Thu, 25 Jul 2024 19:30:11 GMT  
		Size: 3.0 MB (3033097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd70320a891c93191e2f218a4bb464a4e77fdd716c7d5cff92b6f902792d023`  
		Last Modified: Thu, 25 Jul 2024 19:30:10 GMT  
		Size: 14.5 KB (14482 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:e7a2763dd1475cf544505562d99014f1c24bde8f1580a4d1e870871ef619accd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219357922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d8f8bc977b16b4b54045d112682fa1a6466102ea8f934d9df2aa9bd7709ad9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 16 Jul 2024 16:57:57 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 16 Jul 2024 16:57:57 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_VERSION=3.2.32
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ee0355a42f7d9758719333dad0c5816c
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5693916d32d2b37f1d51e84345cfb9ba50a0a541
# Tue, 16 Jul 2024 16:57:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.32/orientdb-community-3.2.32.tar.gz
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jul 2024 16:57:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 16 Jul 2024 16:57:57 GMT
WORKDIR /orientdb
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 16 Jul 2024 16:57:57 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8395e5b7d47f033f4bac691cf04bc6984eea3d1b9b23014a7241caf20e156c18`  
		Last Modified: Thu, 25 Jul 2024 17:43:30 GMT  
		Size: 102.7 MB (102732963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f56095ce5d70fae57595a8a9a16654b4d43926dc67eb4c199442bf6958df30`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9384d39245c0213d2b4df1b44d0d3025e87bd37d8d9bab80ac54c8e5315bd2`  
		Last Modified: Thu, 25 Jul 2024 17:43:24 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbd4e47817b740f60a325e3afcbec3b981ac3eb5d8fd30a169a99e425a4b1a9`  
		Last Modified: Thu, 25 Jul 2024 22:31:44 GMT  
		Size: 72.9 MB (72919478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:da5318f6df345cfedcdc2e19c2255682d23873ce273523a463101c8ef68d97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928a4d7716574b2d6d9a3bee09f143166310069b6f97703324354adb4667cec`

```dockerfile
```

-	Layers:
	-	`sha256:bf8278eaf8deb49af17a931ffe71032f5b1b9771452b303b34e1fd846b94f882`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 3.0 MB (3031443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b36878aeb80bc7e500e8ba55f35c95cb25502b6fbf3177e753e6ce25fff3bc`  
		Last Modified: Thu, 25 Jul 2024 22:31:42 GMT  
		Size: 14.7 KB (14709 bytes)  
		MIME: application/vnd.in-toto+json
