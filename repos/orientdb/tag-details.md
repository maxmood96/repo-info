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
$ docker pull orientdb@sha256:9bd45ba79f1b733efb87df73b648708ec9952c210980a8140d259515cc6de62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:2f3025e3474a23be0c8d94f3e7b2f60b9d4ef718d9de4d2a55c7f45501c4b524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201083638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa34b024740e9457bdfa9ddefe9b23e36a60beb444cc0bc355acae010058267`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b3b08e64f1cf650cb1ed4ffe2c7a66afcb5eeadc7cec763bcd49fdcbb0b238`  
		Last Modified: Sat, 12 Oct 2024 00:55:04 GMT  
		Size: 53.1 MB (53081010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:cf184f1c51322ec950038d5d68f697916035b4f496fab3e1ae4bf0d9aabcb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94e98e1ded5fcdfb30f70a1a0f500d28c1b890fac70689d0a0b9db29fd95347`

```dockerfile
```

-	Layers:
	-	`sha256:4baae574c0cbf868d58ee71385201590371d35d6fd0c6775e02fb6062ee274da`  
		Last Modified: Sat, 12 Oct 2024 00:55:02 GMT  
		Size: 3.3 MB (3272531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4047cce12a0b6f12ebb3dd26dd05b59354293cc4f71894a5b83d19d2be640042`  
		Last Modified: Sat, 12 Oct 2024 00:55:01 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:230a2ca3ebd48519735730a7e8ebb47568affa6d20665f19f35004380d84d64d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:b4f843fa3ca9f297a796f0ee78a48574dacbe1c08a3022a6ccb95ed213712e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224090721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cec4f997fd859c2ae8171b480b18f490dc0218e66df5c5cb969290dd177c1b2`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036314c6ccfac61a7a4bf2f4b9ee7ea248df5252931b9939d4f92e1d51a82fbb`  
		Last Modified: Sat, 12 Oct 2024 00:55:54 GMT  
		Size: 76.1 MB (76086719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0dc06b91fff64abd7db578c0ef011548ac5b2d7d1f658ba2889357c56d77cc`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:c4c19e0faafd7c2dc8ed33de1d036b8a3afc0f6f6ce16d83e1c082950a3f6e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cc07de3c4e4c9834834f821d57625817b51a82106445402c401e1092cbbd46`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f79bf20df813105e30a2bf4ed3ca9cff128390cffaa19c849976c39b811f1`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 3.3 MB (3329883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481a1b5d487578bbfa147d9082426668377bd52498cb8da124f8b5bc4422438d`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 16.8 KB (16809 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:9bd45ba79f1b733efb87df73b648708ec9952c210980a8140d259515cc6de62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:2f3025e3474a23be0c8d94f3e7b2f60b9d4ef718d9de4d2a55c7f45501c4b524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201083638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa34b024740e9457bdfa9ddefe9b23e36a60beb444cc0bc355acae010058267`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b3b08e64f1cf650cb1ed4ffe2c7a66afcb5eeadc7cec763bcd49fdcbb0b238`  
		Last Modified: Sat, 12 Oct 2024 00:55:04 GMT  
		Size: 53.1 MB (53081010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:cf184f1c51322ec950038d5d68f697916035b4f496fab3e1ae4bf0d9aabcb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94e98e1ded5fcdfb30f70a1a0f500d28c1b890fac70689d0a0b9db29fd95347`

```dockerfile
```

-	Layers:
	-	`sha256:4baae574c0cbf868d58ee71385201590371d35d6fd0c6775e02fb6062ee274da`  
		Last Modified: Sat, 12 Oct 2024 00:55:02 GMT  
		Size: 3.3 MB (3272531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4047cce12a0b6f12ebb3dd26dd05b59354293cc4f71894a5b83d19d2be640042`  
		Last Modified: Sat, 12 Oct 2024 00:55:01 GMT  
		Size: 14.1 KB (14147 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:230a2ca3ebd48519735730a7e8ebb47568affa6d20665f19f35004380d84d64d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:b4f843fa3ca9f297a796f0ee78a48574dacbe1c08a3022a6ccb95ed213712e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224090721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cec4f997fd859c2ae8171b480b18f490dc0218e66df5c5cb969290dd177c1b2`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036314c6ccfac61a7a4bf2f4b9ee7ea248df5252931b9939d4f92e1d51a82fbb`  
		Last Modified: Sat, 12 Oct 2024 00:55:54 GMT  
		Size: 76.1 MB (76086719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0dc06b91fff64abd7db578c0ef011548ac5b2d7d1f658ba2889357c56d77cc`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:c4c19e0faafd7c2dc8ed33de1d036b8a3afc0f6f6ce16d83e1c082950a3f6e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cc07de3c4e4c9834834f821d57625817b51a82106445402c401e1092cbbd46`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f79bf20df813105e30a2bf4ed3ca9cff128390cffaa19c849976c39b811f1`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 3.3 MB (3329883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481a1b5d487578bbfa147d9082426668377bd52498cb8da124f8b5bc4422438d`  
		Last Modified: Sat, 12 Oct 2024 00:55:52 GMT  
		Size: 16.8 KB (16809 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:6091da93d2ecad9bf8dacab72370bc4d92cf48a9fa8cb946ab64f1e7772763ec
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
$ docker pull orientdb@sha256:e45a9a98c4ee1637dd244147be12b0206485ee37bd0ff1090eb6fa06167d5387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220926955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba925c7bc4bc9d9a5364108a58530cdea6149c66db39c1202d39b2f52d1a535`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c172f7fc73e8ae37579cab52d0cd897178277f38ff2dc662aa7a15e5e335974`  
		Last Modified: Sat, 12 Oct 2024 00:55:08 GMT  
		Size: 72.9 MB (72924327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:ea89b416c19ac9b9091824040b5845095ef4175126bc77ed07fa83625b79e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbc1ffa61ab5b8bdc2d29a0abbc976b54f0832b27e2a333574dbc6ab0b6140c`

```dockerfile
```

-	Layers:
	-	`sha256:d24dd6289a4bdc7fb1742a8bff97c803e8753fcf209af23c474c27800fbe68b8`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 3.3 MB (3280735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505d268d993ff587e6bc40bcc0e80a77d02361caf868ced3d90d1cd962e7f780`  
		Last Modified: Sat, 12 Oct 2024 00:55:05 GMT  
		Size: 14.4 KB (14448 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:a4bbdc954bc3a91e6a508a4fb5f080f8859cc41833e919e53def4356835c8ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213960270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c347e82b44fa895c3384f0e234338fdb91b029ee21790569a1da1a7d078f85e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b2fd590cc5463faa9cf3f386ec5d345a2af88a6e4c00448ff6aee88954d3f`  
		Last Modified: Wed, 16 Oct 2024 01:33:53 GMT  
		Size: 100.2 MB (100163689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbd58dd82fbc495f93b74f9abf31a2cc9e1f0d14815282deeca8e4271ee30e`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5546bea5a709c69f20b45c0ad81f1a63599e4fbc403b5d8b61566a55c781b58`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfcfd2128a7c6f488555155f9d2fc2519c0b6d0ee8c1298ab93fb8510ecaf4`  
		Last Modified: Wed, 16 Oct 2024 02:22:25 GMT  
		Size: 72.9 MB (72924326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d4d5367c69fb49f329466186abeda55c32f89e19e892c09e133203682b34400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71df19290a49e9573401b3fdefe9ad925634f1c50676a072376473077d1323b6`

```dockerfile
```

-	Layers:
	-	`sha256:7d508790695fb18d7dd7f860bdc8c84340195c738bf5e00a5286e7df0c8fac13`  
		Last Modified: Wed, 16 Oct 2024 02:22:22 GMT  
		Size: 3.3 MB (3284323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b98cf76440e20a9060885a16e5499ac1a0afd54555693420f49fb6f82b5a907`  
		Last Modified: Wed, 16 Oct 2024 02:22:21 GMT  
		Size: 14.5 KB (14523 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:412355cc46f19d13453d9647a5ed4ea9c208b05fc30c74cf16f48a9af7015d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219411705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209575f1ac8e2f3d08cbf8275a4e18fc61301324c33e89ea149b18914ba33ba0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9f64ebaa084b2b13bbc5bd85ed7b43a461b634d6d22af9378da852e3ede21`  
		Last Modified: Sat, 12 Oct 2024 00:13:34 GMT  
		Size: 102.7 MB (102732950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efec05e1504bea1a4a52f58160c39f2470db6d0e71a84a742eb8f0567391b6b`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661548f854312d8f470c7d6cd679caced687c9f5baa842bc80ccc8a5778065`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d0e0f41630a5ef72b600ece553c6e61628fc88abeb754fddbf398e056997e`  
		Last Modified: Sat, 12 Oct 2024 02:08:39 GMT  
		Size: 72.9 MB (72924303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:13c2cc70b277eb8cf31fb74370a8257b847846a2d8fd2089af5b8f5e0f431e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281cdbab5ce3ef04a690c206ea31de4449f067a94dcd7c301a9658d8bacabb6`

```dockerfile
```

-	Layers:
	-	`sha256:c5c86719b5e5b85380bb3d8e37a09c9a9cb66367bf5e4f01c3a2498c8b74589d`  
		Last Modified: Sat, 12 Oct 2024 02:08:38 GMT  
		Size: 3.3 MB (3281888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787bcf18682d49236caacd23ad3f4fffc510821b8716f7ea2cd2ca8d363228a5`  
		Last Modified: Sat, 12 Oct 2024 02:08:37 GMT  
		Size: 14.6 KB (14550 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:a6a4f0b2305bc1b5b0a39b2103b424a270c59cb1fcf617654f1f8bcbc5074606
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
$ docker pull orientdb@sha256:6299f66729572cf90c51dcd1e18868e77380bb1442445c4bb2d3e0552466bbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252855832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4e040834fb76f6b6f9814ff8b92cc3fa40b61b85ccad555f606773be23f84c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a80b03e1899b88d9b8b7846fd07e8daec22f95952d150f781fe3562e5ca27`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 104.9 MB (104851887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2887b7fd7c00342ed904d496847c4dc967844506e1f5e98aeba40bf6928c4d0c`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e76a449a6e9142f4467ef06e4c97ac84ad59a61f7fe566e684942f15b543c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3420462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0f6c8a4ee56cbba517ef6e2c3592ba8c169b66ccd88ca1d1fb4c661bb29d72`

```dockerfile
```

-	Layers:
	-	`sha256:2e49d35872b00d6446a5e9b772b65bf3e94caf552e4ac0455faf7f226a212840`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.4 MB (3403650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cab6fa7486751631cd730318f55789bad375f34f9d6c04c8d69606eb601e76`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 16.8 KB (16812 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:bed9e17e3568830c4819e598b2e167e6d059cdfea30687d30d52ea73aa59c0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546b1bbe17634920198405e78124443bb94380afe61919930ce548b66df3ec0f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b2fd590cc5463faa9cf3f386ec5d345a2af88a6e4c00448ff6aee88954d3f`  
		Last Modified: Wed, 16 Oct 2024 01:33:53 GMT  
		Size: 100.2 MB (100163689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbd58dd82fbc495f93b74f9abf31a2cc9e1f0d14815282deeca8e4271ee30e`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5546bea5a709c69f20b45c0ad81f1a63599e4fbc403b5d8b61566a55c781b58`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84369a8a40427ba1f093f87ae0567298cd86650a6e0aad1e3e027f9384b25a63`  
		Last Modified: Wed, 16 Oct 2024 02:23:27 GMT  
		Size: 104.9 MB (104851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513dca92e23723588c700742d166d7ca2fc70615f3e3727250bf41df37374419`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:dd5025babe55bf7161de2cdc6e05baa3c995c5cc188cd3dd7e4c18f0cf728ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecc9f3d4e0b25b1776ce08d6ab167eb942a6995ef8f5fb0ea742f61fa946115`

```dockerfile
```

-	Layers:
	-	`sha256:6448cbd713b03285f8f8aed54eeb1cc8436a8dc143e165f82cff90bc6e945291`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 3.4 MB (3407230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08f31a6b6797eb9f3f9739118ac4f78926544056c73809a107056ddf5881973`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:38e9a8df3560a484cda79bf90935d8e42906686b6ae3f5e0fbec34f1cec2d737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e612adefc3daf0eb57451a0ff4c0a31b0b481404b35ae4e5ed5e82acd833eeb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9f64ebaa084b2b13bbc5bd85ed7b43a461b634d6d22af9378da852e3ede21`  
		Last Modified: Sat, 12 Oct 2024 00:13:34 GMT  
		Size: 102.7 MB (102732950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efec05e1504bea1a4a52f58160c39f2470db6d0e71a84a742eb8f0567391b6b`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661548f854312d8f470c7d6cd679caced687c9f5baa842bc80ccc8a5778065`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62bfd6a9fb7f880ae576d8b39c74bd3ae8120024834974dcab6a5f8ccd9312`  
		Last Modified: Sat, 12 Oct 2024 02:09:21 GMT  
		Size: 104.9 MB (104851929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f6b2f203b1e75fc7b68d70587b9b34dc0fdd0ebaf0ac0be2f6fa33cfb71dfe`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:33974f738406012f38611bdebab8ab49c345583f4560b7318f976f172f8087ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3421692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5206d5dd6985723175c525ebdb6a42fc6f7336b636f863b86d6e5998071ca37`

```dockerfile
```

-	Layers:
	-	`sha256:5ecd597024e6e44ef06107461a6fd14b3d834c654e7edc100c9d2290e96e8463`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 3.4 MB (3404791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee93c368fe28ed5db7f2502b67b1ef9a14499858648d6736f3954af4e21302db`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 16.9 KB (16901 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.34`

```console
$ docker pull orientdb@sha256:6091da93d2ecad9bf8dacab72370bc4d92cf48a9fa8cb946ab64f1e7772763ec
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
$ docker pull orientdb@sha256:e45a9a98c4ee1637dd244147be12b0206485ee37bd0ff1090eb6fa06167d5387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220926955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba925c7bc4bc9d9a5364108a58530cdea6149c66db39c1202d39b2f52d1a535`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c172f7fc73e8ae37579cab52d0cd897178277f38ff2dc662aa7a15e5e335974`  
		Last Modified: Sat, 12 Oct 2024 00:55:08 GMT  
		Size: 72.9 MB (72924327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:ea89b416c19ac9b9091824040b5845095ef4175126bc77ed07fa83625b79e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbc1ffa61ab5b8bdc2d29a0abbc976b54f0832b27e2a333574dbc6ab0b6140c`

```dockerfile
```

-	Layers:
	-	`sha256:d24dd6289a4bdc7fb1742a8bff97c803e8753fcf209af23c474c27800fbe68b8`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 3.3 MB (3280735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505d268d993ff587e6bc40bcc0e80a77d02361caf868ced3d90d1cd962e7f780`  
		Last Modified: Sat, 12 Oct 2024 00:55:05 GMT  
		Size: 14.4 KB (14448 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:a4bbdc954bc3a91e6a508a4fb5f080f8859cc41833e919e53def4356835c8ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213960270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c347e82b44fa895c3384f0e234338fdb91b029ee21790569a1da1a7d078f85e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b2fd590cc5463faa9cf3f386ec5d345a2af88a6e4c00448ff6aee88954d3f`  
		Last Modified: Wed, 16 Oct 2024 01:33:53 GMT  
		Size: 100.2 MB (100163689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbd58dd82fbc495f93b74f9abf31a2cc9e1f0d14815282deeca8e4271ee30e`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5546bea5a709c69f20b45c0ad81f1a63599e4fbc403b5d8b61566a55c781b58`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfcfd2128a7c6f488555155f9d2fc2519c0b6d0ee8c1298ab93fb8510ecaf4`  
		Last Modified: Wed, 16 Oct 2024 02:22:25 GMT  
		Size: 72.9 MB (72924326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d4d5367c69fb49f329466186abeda55c32f89e19e892c09e133203682b34400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71df19290a49e9573401b3fdefe9ad925634f1c50676a072376473077d1323b6`

```dockerfile
```

-	Layers:
	-	`sha256:7d508790695fb18d7dd7f860bdc8c84340195c738bf5e00a5286e7df0c8fac13`  
		Last Modified: Wed, 16 Oct 2024 02:22:22 GMT  
		Size: 3.3 MB (3284323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b98cf76440e20a9060885a16e5499ac1a0afd54555693420f49fb6f82b5a907`  
		Last Modified: Wed, 16 Oct 2024 02:22:21 GMT  
		Size: 14.5 KB (14523 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:412355cc46f19d13453d9647a5ed4ea9c208b05fc30c74cf16f48a9af7015d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219411705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209575f1ac8e2f3d08cbf8275a4e18fc61301324c33e89ea149b18914ba33ba0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9f64ebaa084b2b13bbc5bd85ed7b43a461b634d6d22af9378da852e3ede21`  
		Last Modified: Sat, 12 Oct 2024 00:13:34 GMT  
		Size: 102.7 MB (102732950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efec05e1504bea1a4a52f58160c39f2470db6d0e71a84a742eb8f0567391b6b`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661548f854312d8f470c7d6cd679caced687c9f5baa842bc80ccc8a5778065`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d0e0f41630a5ef72b600ece553c6e61628fc88abeb754fddbf398e056997e`  
		Last Modified: Sat, 12 Oct 2024 02:08:39 GMT  
		Size: 72.9 MB (72924303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34` - unknown; unknown

```console
$ docker pull orientdb@sha256:13c2cc70b277eb8cf31fb74370a8257b847846a2d8fd2089af5b8f5e0f431e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281cdbab5ce3ef04a690c206ea31de4449f067a94dcd7c301a9658d8bacabb6`

```dockerfile
```

-	Layers:
	-	`sha256:c5c86719b5e5b85380bb3d8e37a09c9a9cb66367bf5e4f01c3a2498c8b74589d`  
		Last Modified: Sat, 12 Oct 2024 02:08:38 GMT  
		Size: 3.3 MB (3281888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787bcf18682d49236caacd23ad3f4fffc510821b8716f7ea2cd2ca8d363228a5`  
		Last Modified: Sat, 12 Oct 2024 02:08:37 GMT  
		Size: 14.6 KB (14550 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.34-tp3`

```console
$ docker pull orientdb@sha256:a6a4f0b2305bc1b5b0a39b2103b424a270c59cb1fcf617654f1f8bcbc5074606
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
$ docker pull orientdb@sha256:6299f66729572cf90c51dcd1e18868e77380bb1442445c4bb2d3e0552466bbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252855832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4e040834fb76f6b6f9814ff8b92cc3fa40b61b85ccad555f606773be23f84c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a80b03e1899b88d9b8b7846fd07e8daec22f95952d150f781fe3562e5ca27`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 104.9 MB (104851887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2887b7fd7c00342ed904d496847c4dc967844506e1f5e98aeba40bf6928c4d0c`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e76a449a6e9142f4467ef06e4c97ac84ad59a61f7fe566e684942f15b543c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3420462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0f6c8a4ee56cbba517ef6e2c3592ba8c169b66ccd88ca1d1fb4c661bb29d72`

```dockerfile
```

-	Layers:
	-	`sha256:2e49d35872b00d6446a5e9b772b65bf3e94caf552e4ac0455faf7f226a212840`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.4 MB (3403650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cab6fa7486751631cd730318f55789bad375f34f9d6c04c8d69606eb601e76`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 16.8 KB (16812 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:bed9e17e3568830c4819e598b2e167e6d059cdfea30687d30d52ea73aa59c0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245889164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546b1bbe17634920198405e78124443bb94380afe61919930ce548b66df3ec0f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b2fd590cc5463faa9cf3f386ec5d345a2af88a6e4c00448ff6aee88954d3f`  
		Last Modified: Wed, 16 Oct 2024 01:33:53 GMT  
		Size: 100.2 MB (100163689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbd58dd82fbc495f93b74f9abf31a2cc9e1f0d14815282deeca8e4271ee30e`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5546bea5a709c69f20b45c0ad81f1a63599e4fbc403b5d8b61566a55c781b58`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84369a8a40427ba1f093f87ae0567298cd86650a6e0aad1e3e027f9384b25a63`  
		Last Modified: Wed, 16 Oct 2024 02:23:27 GMT  
		Size: 104.9 MB (104851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513dca92e23723588c700742d166d7ca2fc70615f3e3727250bf41df37374419`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:dd5025babe55bf7161de2cdc6e05baa3c995c5cc188cd3dd7e4c18f0cf728ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecc9f3d4e0b25b1776ce08d6ab167eb942a6995ef8f5fb0ea742f61fa946115`

```dockerfile
```

-	Layers:
	-	`sha256:6448cbd713b03285f8f8aed54eeb1cc8436a8dc143e165f82cff90bc6e945291`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 3.4 MB (3407230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08f31a6b6797eb9f3f9739118ac4f78926544056c73809a107056ddf5881973`  
		Last Modified: Wed, 16 Oct 2024 02:23:19 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.34-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:38e9a8df3560a484cda79bf90935d8e42906686b6ae3f5e0fbec34f1cec2d737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e612adefc3daf0eb57451a0ff4c0a31b0b481404b35ae4e5ed5e82acd833eeb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9f64ebaa084b2b13bbc5bd85ed7b43a461b634d6d22af9378da852e3ede21`  
		Last Modified: Sat, 12 Oct 2024 00:13:34 GMT  
		Size: 102.7 MB (102732950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efec05e1504bea1a4a52f58160c39f2470db6d0e71a84a742eb8f0567391b6b`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661548f854312d8f470c7d6cd679caced687c9f5baa842bc80ccc8a5778065`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b62bfd6a9fb7f880ae576d8b39c74bd3ae8120024834974dcab6a5f8ccd9312`  
		Last Modified: Sat, 12 Oct 2024 02:09:21 GMT  
		Size: 104.9 MB (104851929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f6b2f203b1e75fc7b68d70587b9b34dc0fdd0ebaf0ac0be2f6fa33cfb71dfe`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.34-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:33974f738406012f38611bdebab8ab49c345583f4560b7318f976f172f8087ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3421692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5206d5dd6985723175c525ebdb6a42fc6f7336b636f863b86d6e5998071ca37`

```dockerfile
```

-	Layers:
	-	`sha256:5ecd597024e6e44ef06107461a6fd14b3d834c654e7edc100c9d2290e96e8463`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 3.4 MB (3404791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee93c368fe28ed5db7f2502b67b1ef9a14499858648d6736f3954af4e21302db`  
		Last Modified: Sat, 12 Oct 2024 02:09:18 GMT  
		Size: 16.9 KB (16901 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:6091da93d2ecad9bf8dacab72370bc4d92cf48a9fa8cb946ab64f1e7772763ec
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
$ docker pull orientdb@sha256:e45a9a98c4ee1637dd244147be12b0206485ee37bd0ff1090eb6fa06167d5387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220926955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba925c7bc4bc9d9a5364108a58530cdea6149c66db39c1202d39b2f52d1a535`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c172f7fc73e8ae37579cab52d0cd897178277f38ff2dc662aa7a15e5e335974`  
		Last Modified: Sat, 12 Oct 2024 00:55:08 GMT  
		Size: 72.9 MB (72924327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:ea89b416c19ac9b9091824040b5845095ef4175126bc77ed07fa83625b79e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbc1ffa61ab5b8bdc2d29a0abbc976b54f0832b27e2a333574dbc6ab0b6140c`

```dockerfile
```

-	Layers:
	-	`sha256:d24dd6289a4bdc7fb1742a8bff97c803e8753fcf209af23c474c27800fbe68b8`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 3.3 MB (3280735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505d268d993ff587e6bc40bcc0e80a77d02361caf868ced3d90d1cd962e7f780`  
		Last Modified: Sat, 12 Oct 2024 00:55:05 GMT  
		Size: 14.4 KB (14448 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:a4bbdc954bc3a91e6a508a4fb5f080f8859cc41833e919e53def4356835c8ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213960270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c347e82b44fa895c3384f0e234338fdb91b029ee21790569a1da1a7d078f85e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b2fd590cc5463faa9cf3f386ec5d345a2af88a6e4c00448ff6aee88954d3f`  
		Last Modified: Wed, 16 Oct 2024 01:33:53 GMT  
		Size: 100.2 MB (100163689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbd58dd82fbc495f93b74f9abf31a2cc9e1f0d14815282deeca8e4271ee30e`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5546bea5a709c69f20b45c0ad81f1a63599e4fbc403b5d8b61566a55c781b58`  
		Last Modified: Wed, 16 Oct 2024 01:33:44 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfcfd2128a7c6f488555155f9d2fc2519c0b6d0ee8c1298ab93fb8510ecaf4`  
		Last Modified: Wed, 16 Oct 2024 02:22:25 GMT  
		Size: 72.9 MB (72924326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d4d5367c69fb49f329466186abeda55c32f89e19e892c09e133203682b34400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71df19290a49e9573401b3fdefe9ad925634f1c50676a072376473077d1323b6`

```dockerfile
```

-	Layers:
	-	`sha256:7d508790695fb18d7dd7f860bdc8c84340195c738bf5e00a5286e7df0c8fac13`  
		Last Modified: Wed, 16 Oct 2024 02:22:22 GMT  
		Size: 3.3 MB (3284323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b98cf76440e20a9060885a16e5499ac1a0afd54555693420f49fb6f82b5a907`  
		Last Modified: Wed, 16 Oct 2024 02:22:21 GMT  
		Size: 14.5 KB (14523 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:412355cc46f19d13453d9647a5ed4ea9c208b05fc30c74cf16f48a9af7015d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219411705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209575f1ac8e2f3d08cbf8275a4e18fc61301324c33e89ea149b18914ba33ba0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 01 Oct 2024 13:53:41 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:53:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:53:41 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:53:41 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 01 Oct 2024 13:53:41 GMT
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
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9f64ebaa084b2b13bbc5bd85ed7b43a461b634d6d22af9378da852e3ede21`  
		Last Modified: Sat, 12 Oct 2024 00:13:34 GMT  
		Size: 102.7 MB (102732950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efec05e1504bea1a4a52f58160c39f2470db6d0e71a84a742eb8f0567391b6b`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661548f854312d8f470c7d6cd679caced687c9f5baa842bc80ccc8a5778065`  
		Last Modified: Sat, 12 Oct 2024 00:13:27 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d0e0f41630a5ef72b600ece553c6e61628fc88abeb754fddbf398e056997e`  
		Last Modified: Sat, 12 Oct 2024 02:08:39 GMT  
		Size: 72.9 MB (72924303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:13c2cc70b277eb8cf31fb74370a8257b847846a2d8fd2089af5b8f5e0f431e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281cdbab5ce3ef04a690c206ea31de4449f067a94dcd7c301a9658d8bacabb6`

```dockerfile
```

-	Layers:
	-	`sha256:c5c86719b5e5b85380bb3d8e37a09c9a9cb66367bf5e4f01c3a2498c8b74589d`  
		Last Modified: Sat, 12 Oct 2024 02:08:38 GMT  
		Size: 3.3 MB (3281888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787bcf18682d49236caacd23ad3f4fffc510821b8716f7ea2cd2ca8d363228a5`  
		Last Modified: Sat, 12 Oct 2024 02:08:37 GMT  
		Size: 14.6 KB (14550 bytes)  
		MIME: application/vnd.in-toto+json
