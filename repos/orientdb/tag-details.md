<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.45`](#orientdb3245)
-	[`orientdb:3.2.45-tp3`](#orientdb3245-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:7962bc9228042673183a023d85ce6f6186b02a64c7419f1d6649abe322eb78d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:252a35c18b02c5616b357a6a959a07ff4a95bfbf720ae69c460a069722b0dcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154518119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170a6ef08656a26a0b9dcb3453b1ff483fd842abfbbeec503f7d88c7c1010d2d`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e7481913d85d33db6649254e5d8d75b71b3e916323a052c051530991070e77`  
		Last Modified: Fri, 10 Oct 2025 03:38:34 GMT  
		Size: 53.1 MB (53081016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:b489a4ec690b3b7aa077297ebd1a2c9afa452dd00e44aa11fbedcb65a0fbce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b4e689881ab001ada697ca9973f7e8aa60b875d3a508250cb12d951e362460`

```dockerfile
```

-	Layers:
	-	`sha256:d181d80a426241f5f56bf58c1d89e7def257d1db174e3e64c619d4e7d7e2f6f9`  
		Last Modified: Fri, 10 Oct 2025 03:40:27 GMT  
		Size: 3.6 MB (3571134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fcbbcf3129007373d26140e155f524dc18628b78c0d46afdcfe327f0ebdab55`  
		Last Modified: Fri, 10 Oct 2025 03:40:28 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:7e668fa94743772d6c9e7dd06375594ee71aa63d1f5638da9647e05b22ce5a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:0107e9b8579fb4b7657512776bdca9bd3da8ed737600ac26b9f00cc9bd6b7efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177525220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec803caa529337640d309fac1f7a153db10f788deef8d338c4ef90abba622813`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc90dedae6be64b685efa0ec5d45f9266e6347aa455e698f4345f7cb1abab6d`  
		Last Modified: Fri, 10 Oct 2025 03:36:07 GMT  
		Size: 76.1 MB (76086743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67414803c62def3aab31a95d66dbbc5a7479551ba123d340a4548077189787d4`  
		Last Modified: Fri, 10 Oct 2025 03:36:01 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:10d53a029a9d75c4d9c0cba13ee126abdc062d633de571023c74a3377830a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3651867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89880caa2d342338ec78cc757aa7901abd16d9efb905d15aae6eba90e4150747`

```dockerfile
```

-	Layers:
	-	`sha256:d4d551f16f3746f1e8214d65531a2bfca43cafee68f163d668670d978d03ca86`  
		Last Modified: Fri, 10 Oct 2025 03:40:22 GMT  
		Size: 3.6 MB (3635024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8140536bd669deb529d6479579363f7ea91dee9f2185fe53cfed1eeeabf98e`  
		Last Modified: Fri, 10 Oct 2025 03:40:23 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:7962bc9228042673183a023d85ce6f6186b02a64c7419f1d6649abe322eb78d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:252a35c18b02c5616b357a6a959a07ff4a95bfbf720ae69c460a069722b0dcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154518119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170a6ef08656a26a0b9dcb3453b1ff483fd842abfbbeec503f7d88c7c1010d2d`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e7481913d85d33db6649254e5d8d75b71b3e916323a052c051530991070e77`  
		Last Modified: Fri, 10 Oct 2025 03:38:34 GMT  
		Size: 53.1 MB (53081016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:b489a4ec690b3b7aa077297ebd1a2c9afa452dd00e44aa11fbedcb65a0fbce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b4e689881ab001ada697ca9973f7e8aa60b875d3a508250cb12d951e362460`

```dockerfile
```

-	Layers:
	-	`sha256:d181d80a426241f5f56bf58c1d89e7def257d1db174e3e64c619d4e7d7e2f6f9`  
		Last Modified: Fri, 10 Oct 2025 03:40:27 GMT  
		Size: 3.6 MB (3571134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fcbbcf3129007373d26140e155f524dc18628b78c0d46afdcfe327f0ebdab55`  
		Last Modified: Fri, 10 Oct 2025 03:40:28 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:7e668fa94743772d6c9e7dd06375594ee71aa63d1f5638da9647e05b22ce5a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:0107e9b8579fb4b7657512776bdca9bd3da8ed737600ac26b9f00cc9bd6b7efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177525220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec803caa529337640d309fac1f7a153db10f788deef8d338c4ef90abba622813`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 15 Sep 2022 13:05:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Sep 2022 13:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Sep 2022 13:05:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Sep 2022 13:05:16 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc90dedae6be64b685efa0ec5d45f9266e6347aa455e698f4345f7cb1abab6d`  
		Last Modified: Fri, 10 Oct 2025 03:36:07 GMT  
		Size: 76.1 MB (76086743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67414803c62def3aab31a95d66dbbc5a7479551ba123d340a4548077189787d4`  
		Last Modified: Fri, 10 Oct 2025 03:36:01 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:10d53a029a9d75c4d9c0cba13ee126abdc062d633de571023c74a3377830a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3651867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89880caa2d342338ec78cc757aa7901abd16d9efb905d15aae6eba90e4150747`

```dockerfile
```

-	Layers:
	-	`sha256:d4d551f16f3746f1e8214d65531a2bfca43cafee68f163d668670d978d03ca86`  
		Last Modified: Fri, 10 Oct 2025 03:40:22 GMT  
		Size: 3.6 MB (3635024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8140536bd669deb529d6479579363f7ea91dee9f2185fe53cfed1eeeabf98e`  
		Last Modified: Fri, 10 Oct 2025 03:40:23 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:496a67d2da979970d511baf993f33f58f38e115b5c62839cf7ba1b2eb442cdbf
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
$ docker pull orientdb@sha256:d5cc28c081d4a8e59740601e9100448cdb4fb1fe1be5eb2e6776f18444c5b7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174373722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc5110b1eacd7334cb7b607464efe82c9fd2bafbc0ece0183a04176100672c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb22e1d122291cb17079f053ddb24864a2006e6653ea36305d91c61e634f817a`  
		Last Modified: Tue, 21 Oct 2025 20:20:44 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:061152f6b9501468522d9d8cd9ecfaa45c418b16a94d19f7b97fe1cd9befab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7535cb57c9eef2dc01a6cbbc508a4c613692b1d20b024ba7d6aefb79cd4ae441`

```dockerfile
```

-	Layers:
	-	`sha256:8ef015a99466c6985c674ddba793e42b9eed372cc14c264f9b5a37bff21f22be`  
		Last Modified: Tue, 21 Oct 2025 21:40:24 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2813ca44b751cb7226c96ef155860b88ed40b4aac8a04a432d685fe313e67f`  
		Last Modified: Tue, 21 Oct 2025 21:40:25 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:eca95a7fed595547ad082c5894040e9c8392b3f1183715485bc16076dcea6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166221258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c8736f3e0e9eec6375a7cbb4b72000f5662915e67b9208c9c3b79034f840a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039aff4ed2f070744d1cc5de3e93d1b8aca6111aa88baed0dbabf449fd8ed82`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 16.3 MB (16306353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a62b4840402f4b9a14c81c72588ee335d9b1202ee66837319687e892ae6044`  
		Last Modified: Thu, 09 Oct 2025 21:09:29 GMT  
		Size: 50.1 MB (50124025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a2f85acd624f87d27ba20669e5cbcab9c41851e45aecc6219e2bed9a443e4`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1c90462b9666a458b1bd6d71315e0623d5908092159fb977fb1c231b58152`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81767bdd6036bd5fc3925e83ad9709e8d71eadaf49c4c29e535154beafa26e0`  
		Last Modified: Tue, 21 Oct 2025 19:44:32 GMT  
		Size: 72.9 MB (72936649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:afb75a8d2934ef70cbd1997e933ebc3f2d7524ba4b4dd1a7d77a18cd45e4b107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaa212e868d897cea2c998e467e7e13974291316af549f5a5b15952b30a5944`

```dockerfile
```

-	Layers:
	-	`sha256:71781aee674fc2b3b9983ef1dfc6b950b0e14b4e10d2d0827affbc8c29e6eb38`  
		Last Modified: Tue, 21 Oct 2025 21:40:29 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ef092e1dbe6e20cf863f92239dd84d336132d3731fc9d6dd0bf461591009e2`  
		Last Modified: Tue, 21 Oct 2025 21:40:30 GMT  
		Size: 14.6 KB (14599 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:7e7f0414fa7c6f40c481a34a8d7f25c505b6844355ca00a711ff9b87bdc43612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172629407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781ab61bc250a2943d3e1c3ac084b1366ebc57c78444809a6cc9a8af31f46b6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61460e446b1594b49b000fa9d979a8bb479d5c75b28b635adb060361c733c466`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb22bb19f4a059a4a7f7fd0e87a47272e573e5a91a185693e4cd19206f19071`  
		Last Modified: Thu, 09 Oct 2025 21:14:27 GMT  
		Size: 53.8 MB (53839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3c4751f3ef676c4404b6f13afaad783b78cb322a3eaf08b290e7d96f72c7e`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9b819ee799265be7861003b57e2dc46b1e29e37ce4fe34ffbcedb7839a216`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8c3086a8e248794e25a08c191d577911d014d6b7130c8a32dc0afb8a9e008f`  
		Last Modified: Tue, 21 Oct 2025 19:53:28 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:ae4ce3462726edd200ef0f77d46672b1798064fd9ef02ccd814d48ffa822afdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218e74e9c8233004518b6ff4225590839c81465d8da87acf0bfc2e62049b1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9f7aa56b128c54a9d7b36316c52a316e8fc3fecbd3c707d1f2d4aa470feb6`  
		Last Modified: Tue, 21 Oct 2025 21:40:35 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6141280c23935857fa7439fe23b00819a41080248d0d454321a55d5233bf9d3f`  
		Last Modified: Tue, 21 Oct 2025 21:40:36 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:d1068b933ff324c24c734c1ceee416067aa20a63e5ab06d54520f74787b05bee
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
$ docker pull orientdb@sha256:9c1ab88081d406d6bb2717c94bb9b28afa7e5ef67cad4e1fc68568332cb676ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206308893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156dce6b1937866187a9fae8ddcf0f925154f0668fd0894c37206bb8c9e65df4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9751ca1099c89a9bb8dfcc2d8de612db6667b5b1dcded2d733b93c677e214`  
		Last Modified: Tue, 21 Oct 2025 20:21:25 GMT  
		Size: 104.9 MB (104870417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb53a8900a983113a69b01c79150cee0441613addc6bed83602130a6e1ce0c8`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b16bdc3104c8274d4c2e4a2bbb4eec69e06596b655e022d593ecbb2147b8c6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446cd4f8d7837ef7d0238ad38d9fdb8566c236f0cab3420304cace8bacb699ad`

```dockerfile
```

-	Layers:
	-	`sha256:72ccc52be4059f26ec630427fbca6b662ec42f2cf190b8ac7a73d6b857c99e00`  
		Last Modified: Tue, 21 Oct 2025 21:40:35 GMT  
		Size: 3.7 MB (3715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a4e2d63a7301c97cfafd99ec191e6c317ef29657f455530f11c0e7237d343e3`  
		Last Modified: Tue, 21 Oct 2025 21:40:36 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:44da68092f8618815c7013819060b0f91ae36655f5c712b7be35482f907e1ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198156428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf342b4f457f6ac24f67a4cc8e989fd4f56f03727821c28e1c27ba768f7d1dc2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039aff4ed2f070744d1cc5de3e93d1b8aca6111aa88baed0dbabf449fd8ed82`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 16.3 MB (16306353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a62b4840402f4b9a14c81c72588ee335d9b1202ee66837319687e892ae6044`  
		Last Modified: Thu, 09 Oct 2025 21:09:29 GMT  
		Size: 50.1 MB (50124025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a2f85acd624f87d27ba20669e5cbcab9c41851e45aecc6219e2bed9a443e4`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1c90462b9666a458b1bd6d71315e0623d5908092159fb977fb1c231b58152`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77633d44065591ad3eb117bea07c1eaeba9fcdb39ac0ab34bcd7a5197aff31db`  
		Last Modified: Tue, 21 Oct 2025 19:44:36 GMT  
		Size: 104.9 MB (104870448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f997bfdb181d05bc09fbe41be6b7df58242033468e5925c10ed12eef97dccf79`  
		Last Modified: Tue, 21 Oct 2025 19:44:18 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:80b3fce6e43ee68c1fe17182aa601b7cd255da072732a21b307471efcf3d3762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf239ead1cfcc4c38acbb7a31f7cf1e8ccdb54c52738a7aa57df5becc4ef8cf`

```dockerfile
```

-	Layers:
	-	`sha256:f2aeef1ceb359884cd5aadb5af30bb3912cf04d06a0341e96063d95a9c0657ca`  
		Last Modified: Tue, 21 Oct 2025 21:40:40 GMT  
		Size: 3.7 MB (3719126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2c4b6471bb64301010c69cbb9a808c3107c575a6e0541c05365e8420f33d21`  
		Last Modified: Tue, 21 Oct 2025 21:40:41 GMT  
		Size: 16.9 KB (16923 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:292e57c08873814509e60b99155ecfd97deef7e79f093b8745177235c1567c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204564635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1061a6bfdf223cd07210f1033b3c12d1e986d9fa3638e1b3cde8888ede89219b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61460e446b1594b49b000fa9d979a8bb479d5c75b28b635adb060361c733c466`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb22bb19f4a059a4a7f7fd0e87a47272e573e5a91a185693e4cd19206f19071`  
		Last Modified: Thu, 09 Oct 2025 21:14:27 GMT  
		Size: 53.8 MB (53839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3c4751f3ef676c4404b6f13afaad783b78cb322a3eaf08b290e7d96f72c7e`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9b819ee799265be7861003b57e2dc46b1e29e37ce4fe34ffbcedb7839a216`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb79e45ebcf1789be5b7e7fbfcb1e5073033ea7f523a76a822ba4e82c17de1e`  
		Last Modified: Tue, 21 Oct 2025 19:53:54 GMT  
		Size: 104.9 MB (104870474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1394b98fd1f8f7f80a45ccef3653def9007d3c1868d5a9eebdc90d531bf3604f`  
		Last Modified: Tue, 21 Oct 2025 19:53:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0bc81b3418f968ef4b0120a422f73a8d13cd8fbc53de027c029113644392cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35b250715dec4864646c188ce8822ea09baaa3e09fb65ea91f46c1d847555ab`

```dockerfile
```

-	Layers:
	-	`sha256:6cd9d379188b2d84d9c93104e3945c5067ba77d3e9cbe201610503d157a90323`  
		Last Modified: Tue, 21 Oct 2025 21:40:45 GMT  
		Size: 3.7 MB (3716305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d73c2a71c4eb4feffa47b0c0cf0b3379c252e83a54ad5d6f12405722ebffa3`  
		Last Modified: Tue, 21 Oct 2025 21:40:46 GMT  
		Size: 16.9 KB (16941 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.45`

```console
$ docker pull orientdb@sha256:496a67d2da979970d511baf993f33f58f38e115b5c62839cf7ba1b2eb442cdbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.45` - linux; amd64

```console
$ docker pull orientdb@sha256:d5cc28c081d4a8e59740601e9100448cdb4fb1fe1be5eb2e6776f18444c5b7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174373722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc5110b1eacd7334cb7b607464efe82c9fd2bafbc0ece0183a04176100672c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb22e1d122291cb17079f053ddb24864a2006e6653ea36305d91c61e634f817a`  
		Last Modified: Tue, 21 Oct 2025 20:20:44 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:061152f6b9501468522d9d8cd9ecfaa45c418b16a94d19f7b97fe1cd9befab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7535cb57c9eef2dc01a6cbbc508a4c613692b1d20b024ba7d6aefb79cd4ae441`

```dockerfile
```

-	Layers:
	-	`sha256:8ef015a99466c6985c674ddba793e42b9eed372cc14c264f9b5a37bff21f22be`  
		Last Modified: Tue, 21 Oct 2025 21:40:24 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2813ca44b751cb7226c96ef155860b88ed40b4aac8a04a432d685fe313e67f`  
		Last Modified: Tue, 21 Oct 2025 21:40:25 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:eca95a7fed595547ad082c5894040e9c8392b3f1183715485bc16076dcea6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166221258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c8736f3e0e9eec6375a7cbb4b72000f5662915e67b9208c9c3b79034f840a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039aff4ed2f070744d1cc5de3e93d1b8aca6111aa88baed0dbabf449fd8ed82`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 16.3 MB (16306353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a62b4840402f4b9a14c81c72588ee335d9b1202ee66837319687e892ae6044`  
		Last Modified: Thu, 09 Oct 2025 21:09:29 GMT  
		Size: 50.1 MB (50124025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a2f85acd624f87d27ba20669e5cbcab9c41851e45aecc6219e2bed9a443e4`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1c90462b9666a458b1bd6d71315e0623d5908092159fb977fb1c231b58152`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81767bdd6036bd5fc3925e83ad9709e8d71eadaf49c4c29e535154beafa26e0`  
		Last Modified: Tue, 21 Oct 2025 19:44:32 GMT  
		Size: 72.9 MB (72936649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:afb75a8d2934ef70cbd1997e933ebc3f2d7524ba4b4dd1a7d77a18cd45e4b107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaa212e868d897cea2c998e467e7e13974291316af549f5a5b15952b30a5944`

```dockerfile
```

-	Layers:
	-	`sha256:71781aee674fc2b3b9983ef1dfc6b950b0e14b4e10d2d0827affbc8c29e6eb38`  
		Last Modified: Tue, 21 Oct 2025 21:40:29 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ef092e1dbe6e20cf863f92239dd84d336132d3731fc9d6dd0bf461591009e2`  
		Last Modified: Tue, 21 Oct 2025 21:40:30 GMT  
		Size: 14.6 KB (14599 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:7e7f0414fa7c6f40c481a34a8d7f25c505b6844355ca00a711ff9b87bdc43612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172629407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781ab61bc250a2943d3e1c3ac084b1366ebc57c78444809a6cc9a8af31f46b6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61460e446b1594b49b000fa9d979a8bb479d5c75b28b635adb060361c733c466`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb22bb19f4a059a4a7f7fd0e87a47272e573e5a91a185693e4cd19206f19071`  
		Last Modified: Thu, 09 Oct 2025 21:14:27 GMT  
		Size: 53.8 MB (53839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3c4751f3ef676c4404b6f13afaad783b78cb322a3eaf08b290e7d96f72c7e`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9b819ee799265be7861003b57e2dc46b1e29e37ce4fe34ffbcedb7839a216`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8c3086a8e248794e25a08c191d577911d014d6b7130c8a32dc0afb8a9e008f`  
		Last Modified: Tue, 21 Oct 2025 19:53:28 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:ae4ce3462726edd200ef0f77d46672b1798064fd9ef02ccd814d48ffa822afdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218e74e9c8233004518b6ff4225590839c81465d8da87acf0bfc2e62049b1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9f7aa56b128c54a9d7b36316c52a316e8fc3fecbd3c707d1f2d4aa470feb6`  
		Last Modified: Tue, 21 Oct 2025 21:40:35 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6141280c23935857fa7439fe23b00819a41080248d0d454321a55d5233bf9d3f`  
		Last Modified: Tue, 21 Oct 2025 21:40:36 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.45-tp3`

```console
$ docker pull orientdb@sha256:d1068b933ff324c24c734c1ceee416067aa20a63e5ab06d54520f74787b05bee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.45-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:9c1ab88081d406d6bb2717c94bb9b28afa7e5ef67cad4e1fc68568332cb676ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206308893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156dce6b1937866187a9fae8ddcf0f925154f0668fd0894c37206bb8c9e65df4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9751ca1099c89a9bb8dfcc2d8de612db6667b5b1dcded2d733b93c677e214`  
		Last Modified: Tue, 21 Oct 2025 20:21:25 GMT  
		Size: 104.9 MB (104870417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb53a8900a983113a69b01c79150cee0441613addc6bed83602130a6e1ce0c8`  
		Last Modified: Tue, 21 Oct 2025 20:21:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b16bdc3104c8274d4c2e4a2bbb4eec69e06596b655e022d593ecbb2147b8c6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446cd4f8d7837ef7d0238ad38d9fdb8566c236f0cab3420304cace8bacb699ad`

```dockerfile
```

-	Layers:
	-	`sha256:72ccc52be4059f26ec630427fbca6b662ec42f2cf190b8ac7a73d6b857c99e00`  
		Last Modified: Tue, 21 Oct 2025 21:40:35 GMT  
		Size: 3.7 MB (3715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a4e2d63a7301c97cfafd99ec191e6c317ef29657f455530f11c0e7237d343e3`  
		Last Modified: Tue, 21 Oct 2025 21:40:36 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:44da68092f8618815c7013819060b0f91ae36655f5c712b7be35482f907e1ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198156428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf342b4f457f6ac24f67a4cc8e989fd4f56f03727821c28e1c27ba768f7d1dc2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039aff4ed2f070744d1cc5de3e93d1b8aca6111aa88baed0dbabf449fd8ed82`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 16.3 MB (16306353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a62b4840402f4b9a14c81c72588ee335d9b1202ee66837319687e892ae6044`  
		Last Modified: Thu, 09 Oct 2025 21:09:29 GMT  
		Size: 50.1 MB (50124025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a2f85acd624f87d27ba20669e5cbcab9c41851e45aecc6219e2bed9a443e4`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1c90462b9666a458b1bd6d71315e0623d5908092159fb977fb1c231b58152`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77633d44065591ad3eb117bea07c1eaeba9fcdb39ac0ab34bcd7a5197aff31db`  
		Last Modified: Tue, 21 Oct 2025 19:44:36 GMT  
		Size: 104.9 MB (104870448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f997bfdb181d05bc09fbe41be6b7df58242033468e5925c10ed12eef97dccf79`  
		Last Modified: Tue, 21 Oct 2025 19:44:18 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:80b3fce6e43ee68c1fe17182aa601b7cd255da072732a21b307471efcf3d3762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf239ead1cfcc4c38acbb7a31f7cf1e8ccdb54c52738a7aa57df5becc4ef8cf`

```dockerfile
```

-	Layers:
	-	`sha256:f2aeef1ceb359884cd5aadb5af30bb3912cf04d06a0341e96063d95a9c0657ca`  
		Last Modified: Tue, 21 Oct 2025 21:40:40 GMT  
		Size: 3.7 MB (3719126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2c4b6471bb64301010c69cbb9a808c3107c575a6e0541c05365e8420f33d21`  
		Last Modified: Tue, 21 Oct 2025 21:40:41 GMT  
		Size: 16.9 KB (16923 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:292e57c08873814509e60b99155ecfd97deef7e79f093b8745177235c1567c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204564635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1061a6bfdf223cd07210f1033b3c12d1e986d9fa3638e1b3cde8888ede89219b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61460e446b1594b49b000fa9d979a8bb479d5c75b28b635adb060361c733c466`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb22bb19f4a059a4a7f7fd0e87a47272e573e5a91a185693e4cd19206f19071`  
		Last Modified: Thu, 09 Oct 2025 21:14:27 GMT  
		Size: 53.8 MB (53839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3c4751f3ef676c4404b6f13afaad783b78cb322a3eaf08b290e7d96f72c7e`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9b819ee799265be7861003b57e2dc46b1e29e37ce4fe34ffbcedb7839a216`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb79e45ebcf1789be5b7e7fbfcb1e5073033ea7f523a76a822ba4e82c17de1e`  
		Last Modified: Tue, 21 Oct 2025 19:53:54 GMT  
		Size: 104.9 MB (104870474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1394b98fd1f8f7f80a45ccef3653def9007d3c1868d5a9eebdc90d531bf3604f`  
		Last Modified: Tue, 21 Oct 2025 19:53:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0bc81b3418f968ef4b0120a422f73a8d13cd8fbc53de027c029113644392cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35b250715dec4864646c188ce8822ea09baaa3e09fb65ea91f46c1d847555ab`

```dockerfile
```

-	Layers:
	-	`sha256:6cd9d379188b2d84d9c93104e3945c5067ba77d3e9cbe201610503d157a90323`  
		Last Modified: Tue, 21 Oct 2025 21:40:45 GMT  
		Size: 3.7 MB (3716305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d73c2a71c4eb4feffa47b0c0cf0b3379c252e83a54ad5d6f12405722ebffa3`  
		Last Modified: Tue, 21 Oct 2025 21:40:46 GMT  
		Size: 16.9 KB (16941 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:496a67d2da979970d511baf993f33f58f38e115b5c62839cf7ba1b2eb442cdbf
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
$ docker pull orientdb@sha256:d5cc28c081d4a8e59740601e9100448cdb4fb1fe1be5eb2e6776f18444c5b7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174373722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc5110b1eacd7334cb7b607464efe82c9fd2bafbc0ece0183a04176100672c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e91cbd4e78d9d306ff5f16ab0fb2c03a620508658d76b6ee6cf5b590183001`  
		Last Modified: Thu, 09 Oct 2025 21:14:01 GMT  
		Size: 17.0 MB (16971818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff219c2be2046300b285dba1fe6c269e97225129e6b2270c307dce2d0f05a99`  
		Last Modified: Thu, 09 Oct 2025 21:14:08 GMT  
		Size: 54.7 MB (54739641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a656fd7504979ebcab99066bc8d3a5ee06e74f190e09c93f4843cb21721f5c`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c054cf84e2b26e93c06c3cc3a079e32b837cc64f8ce4cf712d05f9c7c849cf`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb22e1d122291cb17079f053ddb24864a2006e6653ea36305d91c61e634f817a`  
		Last Modified: Tue, 21 Oct 2025 20:20:44 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:061152f6b9501468522d9d8cd9ecfaa45c418b16a94d19f7b97fe1cd9befab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7535cb57c9eef2dc01a6cbbc508a4c613692b1d20b024ba7d6aefb79cd4ae441`

```dockerfile
```

-	Layers:
	-	`sha256:8ef015a99466c6985c674ddba793e42b9eed372cc14c264f9b5a37bff21f22be`  
		Last Modified: Tue, 21 Oct 2025 21:40:24 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2813ca44b751cb7226c96ef155860b88ed40b4aac8a04a432d685fe313e67f`  
		Last Modified: Tue, 21 Oct 2025 21:40:25 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:eca95a7fed595547ad082c5894040e9c8392b3f1183715485bc16076dcea6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166221258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c8736f3e0e9eec6375a7cbb4b72000f5662915e67b9208c9c3b79034f840a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039aff4ed2f070744d1cc5de3e93d1b8aca6111aa88baed0dbabf449fd8ed82`  
		Last Modified: Thu, 09 Oct 2025 21:09:27 GMT  
		Size: 16.3 MB (16306353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a62b4840402f4b9a14c81c72588ee335d9b1202ee66837319687e892ae6044`  
		Last Modified: Thu, 09 Oct 2025 21:09:29 GMT  
		Size: 50.1 MB (50124025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a2f85acd624f87d27ba20669e5cbcab9c41851e45aecc6219e2bed9a443e4`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1c90462b9666a458b1bd6d71315e0623d5908092159fb977fb1c231b58152`  
		Last Modified: Thu, 09 Oct 2025 21:09:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81767bdd6036bd5fc3925e83ad9709e8d71eadaf49c4c29e535154beafa26e0`  
		Last Modified: Tue, 21 Oct 2025 19:44:32 GMT  
		Size: 72.9 MB (72936649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:afb75a8d2934ef70cbd1997e933ebc3f2d7524ba4b4dd1a7d77a18cd45e4b107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaa212e868d897cea2c998e467e7e13974291316af549f5a5b15952b30a5944`

```dockerfile
```

-	Layers:
	-	`sha256:71781aee674fc2b3b9983ef1dfc6b950b0e14b4e10d2d0827affbc8c29e6eb38`  
		Last Modified: Tue, 21 Oct 2025 21:40:29 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ef092e1dbe6e20cf863f92239dd84d336132d3731fc9d6dd0bf461591009e2`  
		Last Modified: Tue, 21 Oct 2025 21:40:30 GMT  
		Size: 14.6 KB (14599 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:7e7f0414fa7c6f40c481a34a8d7f25c505b6844355ca00a711ff9b87bdc43612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172629407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781ab61bc250a2943d3e1c3ac084b1366ebc57c78444809a6cc9a8af31f46b6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Oct 2025 11:27:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 21 Oct 2025 11:27:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Tue, 21 Oct 2025 11:27:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 21 Oct 2025 11:27:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 11:27:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 21 Oct 2025 11:27:30 GMT
WORKDIR /orientdb
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 21 Oct 2025 11:27:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61460e446b1594b49b000fa9d979a8bb479d5c75b28b635adb060361c733c466`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb22bb19f4a059a4a7f7fd0e87a47272e573e5a91a185693e4cd19206f19071`  
		Last Modified: Thu, 09 Oct 2025 21:14:27 GMT  
		Size: 53.8 MB (53839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3c4751f3ef676c4404b6f13afaad783b78cb322a3eaf08b290e7d96f72c7e`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9b819ee799265be7861003b57e2dc46b1e29e37ce4fe34ffbcedb7839a216`  
		Last Modified: Thu, 09 Oct 2025 21:14:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8c3086a8e248794e25a08c191d577911d014d6b7130c8a32dc0afb8a9e008f`  
		Last Modified: Tue, 21 Oct 2025 19:53:28 GMT  
		Size: 72.9 MB (72936619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:ae4ce3462726edd200ef0f77d46672b1798064fd9ef02ccd814d48ffa822afdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218e74e9c8233004518b6ff4225590839c81465d8da87acf0bfc2e62049b1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9f7aa56b128c54a9d7b36316c52a316e8fc3fecbd3c707d1f2d4aa470feb6`  
		Last Modified: Tue, 21 Oct 2025 21:40:35 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6141280c23935857fa7439fe23b00819a41080248d0d454321a55d5233bf9d3f`  
		Last Modified: Tue, 21 Oct 2025 21:40:36 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json
