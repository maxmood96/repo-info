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
$ docker pull orientdb@sha256:e4c4c5c8893302cccd0d69aa485e43e1d4928539523e3186f42d38ed5c95a20d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:daa2e94f979783ccdd1a8e8eaea98362d3144e0644e166d79ee88a1afc00567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201033278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604a576f0e32224c10e39f8baa108b8a455b174ce3607758c86d50f495134691`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5839926088fe0842112b9b2edbd6cb50745cc566b4e3be86088504bb856434e`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 53.1 MB (53081029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:7ab421751e2cbf270724299ea2cbefe0a15a13959b5b4a207e20c7632660978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ee60a8f414ab54d6efd59171b8be18020da3dc13796a6ef3ff1acc31fc4c0f`

```dockerfile
```

-	Layers:
	-	`sha256:71b557825eefe15a66d3bf0fc3de22d3b82bc688c66f29b6f030c37c3cf79292`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 3.0 MB (3022206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077a676ab2387b1363455888cd09c9e31ee06e32b38610eef98321b4e0880729`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 14.1 KB (14109 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:4d9ab1d7ecf6ae59b0ec03cf194a031b22bf9592e3bfc9ce3fb795be676c1b92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e843700884a042e3fea8c4c0d8872fb0b219161eec9e7bde44a4057d735f9512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224040368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5158111f8420d42af563066e50b008c38cfa115c2bce161b4daabdac321e5731`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc06c8d992f20cd0bf5df80d855aa3bfa6fd50196e8e1f97c1ab65a76972a6`  
		Last Modified: Sat, 17 Aug 2024 02:01:52 GMT  
		Size: 76.1 MB (76086741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230c1edbbf3fe39d0357432c91500ef7ce17d826e560202989ef2af12eba447`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:4bf05b20c54f0446b1b4e98e9e51b7c933c2cd54e809979826f7775c34f0b84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dade4d6788c0eb4c27213abd6b7a7dfa2802d1a102c791e4b40f4750a56d0e76`

```dockerfile
```

-	Layers:
	-	`sha256:d9d2118886b5f1b5030e1d96b6be454412881100cfbc4182684b866f5a08c4a8`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 3.1 MB (3079580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c3754b57318802ee75f535e37a98831c60a7832fcc2174a99805b1b76aca67`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 16.8 KB (16771 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:e4c4c5c8893302cccd0d69aa485e43e1d4928539523e3186f42d38ed5c95a20d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:daa2e94f979783ccdd1a8e8eaea98362d3144e0644e166d79ee88a1afc00567d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201033278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604a576f0e32224c10e39f8baa108b8a455b174ce3607758c86d50f495134691`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5839926088fe0842112b9b2edbd6cb50745cc566b4e3be86088504bb856434e`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 53.1 MB (53081029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:7ab421751e2cbf270724299ea2cbefe0a15a13959b5b4a207e20c7632660978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ee60a8f414ab54d6efd59171b8be18020da3dc13796a6ef3ff1acc31fc4c0f`

```dockerfile
```

-	Layers:
	-	`sha256:71b557825eefe15a66d3bf0fc3de22d3b82bc688c66f29b6f030c37c3cf79292`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 3.0 MB (3022206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077a676ab2387b1363455888cd09c9e31ee06e32b38610eef98321b4e0880729`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 14.1 KB (14109 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:4d9ab1d7ecf6ae59b0ec03cf194a031b22bf9592e3bfc9ce3fb795be676c1b92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e843700884a042e3fea8c4c0d8872fb0b219161eec9e7bde44a4057d735f9512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224040368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5158111f8420d42af563066e50b008c38cfa115c2bce161b4daabdac321e5731`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc06c8d992f20cd0bf5df80d855aa3bfa6fd50196e8e1f97c1ab65a76972a6`  
		Last Modified: Sat, 17 Aug 2024 02:01:52 GMT  
		Size: 76.1 MB (76086741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230c1edbbf3fe39d0357432c91500ef7ce17d826e560202989ef2af12eba447`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:4bf05b20c54f0446b1b4e98e9e51b7c933c2cd54e809979826f7775c34f0b84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dade4d6788c0eb4c27213abd6b7a7dfa2802d1a102c791e4b40f4750a56d0e76`

```dockerfile
```

-	Layers:
	-	`sha256:d9d2118886b5f1b5030e1d96b6be454412881100cfbc4182684b866f5a08c4a8`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 3.1 MB (3079580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c3754b57318802ee75f535e37a98831c60a7832fcc2174a99805b1b76aca67`  
		Last Modified: Sat, 17 Aug 2024 02:01:51 GMT  
		Size: 16.8 KB (16771 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:766d73ebbf4298f0b8e61434e241057a82fb4a31e12dedb4a071a9a145977cad
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
$ docker pull orientdb@sha256:5e439f790b51e0fe9485311bf1828fcfc1d57d529ffe8cc60f8bee0dd7280d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220871799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ee20170516ffd639ca7f286191ef76b84ccd5ccf192b549fc7f517fa24f8c`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6fe340fba038f85a1e3179d1d537df405dce2c4fa7ff7aa04f0b8b5b70f421`  
		Last Modified: Sat, 17 Aug 2024 02:05:33 GMT  
		Size: 72.9 MB (72919550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:0419714afae70242f59f19cd5706a60652e47ca3205c46c8c9259fa57704449c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2d1b210c03422ca1c3b4a6e783ba6f08cda04b2ca78df5e8265212443e0a56`

```dockerfile
```

-	Layers:
	-	`sha256:fbc361bd25d7d32c97ed323c59734f8932c21eeb53cbb83b85f6a76cb97f2460`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245953049e7fb7ad8f5057a1061b57d50f72627205c7cc862ddfb710245e112a`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c46f3483fbe1b8b857a537773e8aeab4b1326d565095a31ea67031181b418664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212968124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd311fa790f44b3a57f2af67e14ea0aa43adda42c63775e2d3186a92ae55097`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3862c536cdfb0bdc3b90686d4e0a3c3a5ae3912fce84544ed883d16af24466e`  
		Last Modified: Sat, 17 Aug 2024 04:32:55 GMT  
		Size: 72.9 MB (72919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:6752ffa5a914ee42eae1208c85eb8a7ae96e9d1d9aeefd0c0f40f936dc5fe46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3439d7f0b22dbd9c709cf70ed37547763ce8b6aee1900e4c8fe5a5d72a2ce6c`

```dockerfile
```

-	Layers:
	-	`sha256:36fda9220fb86585173b08786e05baa9104b7f44f9938134d4aa19fca44bf1da`  
		Last Modified: Sat, 17 Aug 2024 04:32:53 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ecbc57376dbd42cd4ffd1a49f15f89e17cfcbd0bc15731f73ea8b22f0dd225`  
		Last Modified: Sat, 17 Aug 2024 04:32:52 GMT  
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
$ docker pull orientdb@sha256:205940823af3bdafdb92269b6684236c473ce4e10364c4ee2bba34d8b15ecacf
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
$ docker pull orientdb@sha256:30aef6d3c339166575cccd243f2705a0216fd58dd0b5993e043faaa5d86dfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252799413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efde5c557d760c9bdaed27e86898094214be639c297fa16e58769009567324`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a9086632f7c724a3e8b82618028527657e1fa59761d1d1e994a799de782a3e`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 104.8 MB (104845844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35606fc0d90dd261572ef06a09092c51e2fc8763a17930a42f13b381211c8f2`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d67b44d658c7b3c728f325167884873697bdead150f7b1d2c6b8106776072f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2eb1bc44f69f1f48300d0a17f99fba385bccb923649b952ee72cc4dc96cbae`

```dockerfile
```

-	Layers:
	-	`sha256:e42086bd87fe0a6d28dfe18e9655ba3c81bc05bec389631ce01c30cf7dd7383c`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 3.2 MB (3153351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8cd8ebd3591a5773ead1ed3de8c986c08b517c195812c15eb6adb74a230a380`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:6631d3e8c18b116081b2c9023ce530e9de05bc90486a638e9e20fbd7d230c6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244895766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a85a86ddc57081aaa6e6147abf8fc9ccbba2c5e056594f70e0d686d2559f8ff`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943500ac4cb694ba61333a5dac17e0b3a3ebc6cd8a21e04d74c5111d581a6a0d`  
		Last Modified: Sat, 17 Aug 2024 04:33:51 GMT  
		Size: 104.8 MB (104845876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03135270490426a7126cfd4d5ba003e2de306f41904c3351814d9a97ca2da239`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:567e1597df058ff939afb70d6e9b6d8c64a903d78469ce8f8792f0b9915421be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc67a3e73ddb48f21240ffff1038dafcffd8d7ac923264fbc57db55b66f06e2e`

```dockerfile
```

-	Layers:
	-	`sha256:3e690a2f65dade06707dca2233e5509bed67ebcb786bcbc4e6bb6b19c0582f1c`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
		Size: 3.2 MB (3156054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32576ff67c2cb323e663381a231c3772b80281253a98613efe09f9a43d07b91b`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
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
$ docker pull orientdb@sha256:766d73ebbf4298f0b8e61434e241057a82fb4a31e12dedb4a071a9a145977cad
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
$ docker pull orientdb@sha256:5e439f790b51e0fe9485311bf1828fcfc1d57d529ffe8cc60f8bee0dd7280d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220871799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ee20170516ffd639ca7f286191ef76b84ccd5ccf192b549fc7f517fa24f8c`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6fe340fba038f85a1e3179d1d537df405dce2c4fa7ff7aa04f0b8b5b70f421`  
		Last Modified: Sat, 17 Aug 2024 02:05:33 GMT  
		Size: 72.9 MB (72919550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32` - unknown; unknown

```console
$ docker pull orientdb@sha256:0419714afae70242f59f19cd5706a60652e47ca3205c46c8c9259fa57704449c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2d1b210c03422ca1c3b4a6e783ba6f08cda04b2ca78df5e8265212443e0a56`

```dockerfile
```

-	Layers:
	-	`sha256:fbc361bd25d7d32c97ed323c59734f8932c21eeb53cbb83b85f6a76cb97f2460`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245953049e7fb7ad8f5057a1061b57d50f72627205c7cc862ddfb710245e112a`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c46f3483fbe1b8b857a537773e8aeab4b1326d565095a31ea67031181b418664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212968124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd311fa790f44b3a57f2af67e14ea0aa43adda42c63775e2d3186a92ae55097`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3862c536cdfb0bdc3b90686d4e0a3c3a5ae3912fce84544ed883d16af24466e`  
		Last Modified: Sat, 17 Aug 2024 04:32:55 GMT  
		Size: 72.9 MB (72919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32` - unknown; unknown

```console
$ docker pull orientdb@sha256:6752ffa5a914ee42eae1208c85eb8a7ae96e9d1d9aeefd0c0f40f936dc5fe46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3439d7f0b22dbd9c709cf70ed37547763ce8b6aee1900e4c8fe5a5d72a2ce6c`

```dockerfile
```

-	Layers:
	-	`sha256:36fda9220fb86585173b08786e05baa9104b7f44f9938134d4aa19fca44bf1da`  
		Last Modified: Sat, 17 Aug 2024 04:32:53 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ecbc57376dbd42cd4ffd1a49f15f89e17cfcbd0bc15731f73ea8b22f0dd225`  
		Last Modified: Sat, 17 Aug 2024 04:32:52 GMT  
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
$ docker pull orientdb@sha256:205940823af3bdafdb92269b6684236c473ce4e10364c4ee2bba34d8b15ecacf
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
$ docker pull orientdb@sha256:30aef6d3c339166575cccd243f2705a0216fd58dd0b5993e043faaa5d86dfbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252799413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1efde5c557d760c9bdaed27e86898094214be639c297fa16e58769009567324`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a9086632f7c724a3e8b82618028527657e1fa59761d1d1e994a799de782a3e`  
		Last Modified: Sat, 17 Aug 2024 02:01:57 GMT  
		Size: 104.8 MB (104845844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35606fc0d90dd261572ef06a09092c51e2fc8763a17930a42f13b381211c8f2`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d67b44d658c7b3c728f325167884873697bdead150f7b1d2c6b8106776072f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2eb1bc44f69f1f48300d0a17f99fba385bccb923649b952ee72cc4dc96cbae`

```dockerfile
```

-	Layers:
	-	`sha256:e42086bd87fe0a6d28dfe18e9655ba3c81bc05bec389631ce01c30cf7dd7383c`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 3.2 MB (3153351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8cd8ebd3591a5773ead1ed3de8c986c08b517c195812c15eb6adb74a230a380`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.32-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:6631d3e8c18b116081b2c9023ce530e9de05bc90486a638e9e20fbd7d230c6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244895766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a85a86ddc57081aaa6e6147abf8fc9ccbba2c5e056594f70e0d686d2559f8ff`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943500ac4cb694ba61333a5dac17e0b3a3ebc6cd8a21e04d74c5111d581a6a0d`  
		Last Modified: Sat, 17 Aug 2024 04:33:51 GMT  
		Size: 104.8 MB (104845876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03135270490426a7126cfd4d5ba003e2de306f41904c3351814d9a97ca2da239`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.32-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:567e1597df058ff939afb70d6e9b6d8c64a903d78469ce8f8792f0b9915421be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc67a3e73ddb48f21240ffff1038dafcffd8d7ac923264fbc57db55b66f06e2e`

```dockerfile
```

-	Layers:
	-	`sha256:3e690a2f65dade06707dca2233e5509bed67ebcb786bcbc4e6bb6b19c0582f1c`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
		Size: 3.2 MB (3156054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32576ff67c2cb323e663381a231c3772b80281253a98613efe09f9a43d07b91b`  
		Last Modified: Sat, 17 Aug 2024 04:33:48 GMT  
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
$ docker pull orientdb@sha256:766d73ebbf4298f0b8e61434e241057a82fb4a31e12dedb4a071a9a145977cad
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
$ docker pull orientdb@sha256:5e439f790b51e0fe9485311bf1828fcfc1d57d529ffe8cc60f8bee0dd7280d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220871799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ee20170516ffd639ca7f286191ef76b84ccd5ccf192b549fc7f517fa24f8c`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6fe340fba038f85a1e3179d1d537df405dce2c4fa7ff7aa04f0b8b5b70f421`  
		Last Modified: Sat, 17 Aug 2024 02:05:33 GMT  
		Size: 72.9 MB (72919550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:0419714afae70242f59f19cd5706a60652e47ca3205c46c8c9259fa57704449c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2d1b210c03422ca1c3b4a6e783ba6f08cda04b2ca78df5e8265212443e0a56`

```dockerfile
```

-	Layers:
	-	`sha256:fbc361bd25d7d32c97ed323c59734f8932c21eeb53cbb83b85f6a76cb97f2460`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245953049e7fb7ad8f5057a1061b57d50f72627205c7cc862ddfb710245e112a`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c46f3483fbe1b8b857a537773e8aeab4b1326d565095a31ea67031181b418664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212968124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd311fa790f44b3a57f2af67e14ea0aa43adda42c63775e2d3186a92ae55097`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 16 Jul 2024 16:57:57 GMT
ARG RELEASE
# Tue, 16 Jul 2024 16:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Jul 2024 16:57:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Jul 2024 16:57:57 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Tue, 16 Jul 2024 16:57:57 GMT
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
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3862c536cdfb0bdc3b90686d4e0a3c3a5ae3912fce84544ed883d16af24466e`  
		Last Modified: Sat, 17 Aug 2024 04:32:55 GMT  
		Size: 72.9 MB (72919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:6752ffa5a914ee42eae1208c85eb8a7ae96e9d1d9aeefd0c0f40f936dc5fe46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3439d7f0b22dbd9c709cf70ed37547763ce8b6aee1900e4c8fe5a5d72a2ce6c`

```dockerfile
```

-	Layers:
	-	`sha256:36fda9220fb86585173b08786e05baa9104b7f44f9938134d4aa19fca44bf1da`  
		Last Modified: Sat, 17 Aug 2024 04:32:53 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ecbc57376dbd42cd4ffd1a49f15f89e17cfcbd0bc15731f73ea8b22f0dd225`  
		Last Modified: Sat, 17 Aug 2024 04:32:52 GMT  
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
