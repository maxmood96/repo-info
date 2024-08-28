<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.33`](#orientdb3233)
-	[`orientdb:3.2.33-tp3`](#orientdb3233-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:488169d3bc3ad2b4924b92d21eb7a6720556f7b661e8d1f06537c26f92edc7d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:f2e005f55dde53b1e270cd33651e430f449a0a2f2ba99d3f77ba23e7af8f27ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201677232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f1f0b3fe3fb889ae4a9b31188e4254c7e248418c248280c20bc3a28e51e8fb`
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a454f72269d025ad6f4817241e9be1d9fbfa6dc87737ff92645b43810a20ada0`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 643.7 KB (643738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a35c3328ef87f1d155f3d38ad25f01471677e7ed7c27f856c2c5a79a385dd8`  
		Last Modified: Fri, 23 Aug 2024 20:03:07 GMT  
		Size: 53.1 MB (53081013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:4cdc5097bf23793a6202b02512f282c91883f1704cfbb3fbcabd70d798ad1a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8797fae00ed087aa3e1dd12bc6bb52f524b4a46f9c4146565ee0e213e109a58e`

```dockerfile
```

-	Layers:
	-	`sha256:cc586bbd26e62f6758f7fb605103484a57266b43b90bca36d73c06794da471b6`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 3.0 MB (3022202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825a8f059c82153725376def2f9f7b77d90ac1947599543996036477e01b716e`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:b7df44d9d4e4003cb45034670bbace55beccc61ada245de56ade8af2248949a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e0612f45fe774a564e3b9b5a3b90b58ae70de1f360b12255a71f9585054b546c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224684293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc5fd5e581921cf52588f9ce7835410100cba4d05c0f0a1e27c097d63ffa157`
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0975083cc47e85fa89b04d0aa69a4da2bb2a37414382ad04fb59d49913a1117`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 643.7 KB (643721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f41034b2d93425d5b6bff560512628f1a73f3fd18d3a093ac34c1fe0768c28f`  
		Last Modified: Fri, 23 Aug 2024 20:03:07 GMT  
		Size: 76.1 MB (76086719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf52187a80164650078a03781ba2d3fd026439c238bccb371a0e7e1448655e`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:66e4cfc29aad40d5d4868101b96ce860b360f81658a11966662d13be2359611a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77936dd0968d2bc76bdcff88c3bbbbe43dd500b43e14ce506eebd91a1aa518c5`

```dockerfile
```

-	Layers:
	-	`sha256:d4027a5ab2a3f0424143507d1babe24a765e91b042e13cf4ee26c1aa36ec2575`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 3.1 MB (3079584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0efd2ca45b8c371ce9300a438ab4dee95ae934b7e018132f35ab487a1f5ef5`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 16.8 KB (16787 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:488169d3bc3ad2b4924b92d21eb7a6720556f7b661e8d1f06537c26f92edc7d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:f2e005f55dde53b1e270cd33651e430f449a0a2f2ba99d3f77ba23e7af8f27ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201677232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f1f0b3fe3fb889ae4a9b31188e4254c7e248418c248280c20bc3a28e51e8fb`
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a454f72269d025ad6f4817241e9be1d9fbfa6dc87737ff92645b43810a20ada0`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 643.7 KB (643738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a35c3328ef87f1d155f3d38ad25f01471677e7ed7c27f856c2c5a79a385dd8`  
		Last Modified: Fri, 23 Aug 2024 20:03:07 GMT  
		Size: 53.1 MB (53081013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:4cdc5097bf23793a6202b02512f282c91883f1704cfbb3fbcabd70d798ad1a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8797fae00ed087aa3e1dd12bc6bb52f524b4a46f9c4146565ee0e213e109a58e`

```dockerfile
```

-	Layers:
	-	`sha256:cc586bbd26e62f6758f7fb605103484a57266b43b90bca36d73c06794da471b6`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 3.0 MB (3022202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825a8f059c82153725376def2f9f7b77d90ac1947599543996036477e01b716e`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:b7df44d9d4e4003cb45034670bbace55beccc61ada245de56ade8af2248949a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e0612f45fe774a564e3b9b5a3b90b58ae70de1f360b12255a71f9585054b546c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224684293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc5fd5e581921cf52588f9ce7835410100cba4d05c0f0a1e27c097d63ffa157`
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0975083cc47e85fa89b04d0aa69a4da2bb2a37414382ad04fb59d49913a1117`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 643.7 KB (643721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f41034b2d93425d5b6bff560512628f1a73f3fd18d3a093ac34c1fe0768c28f`  
		Last Modified: Fri, 23 Aug 2024 20:03:07 GMT  
		Size: 76.1 MB (76086719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf52187a80164650078a03781ba2d3fd026439c238bccb371a0e7e1448655e`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:66e4cfc29aad40d5d4868101b96ce860b360f81658a11966662d13be2359611a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77936dd0968d2bc76bdcff88c3bbbbe43dd500b43e14ce506eebd91a1aa518c5`

```dockerfile
```

-	Layers:
	-	`sha256:d4027a5ab2a3f0424143507d1babe24a765e91b042e13cf4ee26c1aa36ec2575`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 3.1 MB (3079584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0efd2ca45b8c371ce9300a438ab4dee95ae934b7e018132f35ab487a1f5ef5`  
		Last Modified: Fri, 23 Aug 2024 20:03:06 GMT  
		Size: 16.8 KB (16787 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:6b1229f51d3cd7ba9f89f554c00e4af483e6bfab6f1a83cffe896d907d30c3e0
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
$ docker pull orientdb@sha256:c3265bd6a276e423e95401cd93560fafa4139d0a560191c016cbbcc059da44e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221519423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc39d978d30f3de4fe01f58edb2b9098f26c6cb33d6ee13c8a45b9964be98be`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ada40b5897ea94f50109e8a0c35454335cedfbfd6554ea84510aa932091d7`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 643.7 KB (643709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b5be55402ba925b826dd6c980a540c442130e44c9eac39a49e6e38492a01e`  
		Last Modified: Wed, 28 Aug 2024 18:55:39 GMT  
		Size: 72.9 MB (72923233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:94e491a57ad977c9083407b6b6353acf7d0c9a1cb08a6c95223778cec8490a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ae22423ba9ebafa53ab7aa87c9909753687ff88df316c21093e0c9fd41f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:109ed6287e4a3287a33504504dc26c0067f6f13fb342093da1d44702e5e9717c`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281990b5a423dc8a2d0f3dabbc26cb7423134b6b03f25a3f6a5e5bf1680401a4`  
		Last Modified: Wed, 28 Aug 2024 18:55:36 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:ad8e166e57876333e411e2121c4e304ba78ed2f1babdb97dfc083a2861b7ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213541918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a58134cae102717973ebb458dd965ed7dfa4e9ac68e0b9297c02b79180a3d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a900fb3dd3e6f143da55254b0216a8571da804287291ca576d9e5d91a2f4e34`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 569.9 KB (569879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd9d7548ea5046aaa03a253e9ebfb9bc4e7feba42d9f0af40848e60acf6203`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 72.9 MB (72923234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:d6591c795f64537dd5c7c0495f39cc0fdf2c54aa66228904d61688a71aa6cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d399a0c983c5203bfa33ac8e6a8686213860edfdb0f78a3972ed334fc7bcf4b`

```dockerfile
```

-	Layers:
	-	`sha256:bbf9971b4f6d7cc90bc3f8c8f38b6105406ceee7489311588ab5f5888fa2cb80`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439056504c0af7f1a9afc4247e1378be6c9c5ac03cec418219390b21da916222`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 14.5 KB (14493 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:10766d99adc1dfe500774d87ab14631c999d99497aee1e7b3b720e76b8b2b578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220003248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d098c5124d048f13e55f3e764b700860f38d4e3d1ed362e97362cdffadd7a7c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2610358824c74ef46f21dbcdff4aedd5417091f979c7e6b6cada05f13765b4b1`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 638.8 KB (638848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0a5dd567e5a7a4833bcf95e9f263cd16457c4646d39130c50d6d0b806e203`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 72.9 MB (72923207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f75e6751a42a5ccac173cf446ca90f20a4259d92058e8cd3d62b8a612c25159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14890522a9134f5317d9ab702dae24ee226b0dfc165c69ccc2e9cc0bf9fb1542`

```dockerfile
```

-	Layers:
	-	`sha256:26c8b6d938957f781a45248871e6e200fbe4b9a635e60161d895c78ef1bcb235`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 3.0 MB (3031479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b757ec0a451038666fc8391531e0f83e7f303609f4ebc57c0411803680e39956`  
		Last Modified: Wed, 28 Aug 2024 18:55:31 GMT  
		Size: 14.7 KB (14721 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:d21c6d769e82118a6545964a6ffc3acffce1cb053f3c0283a863623b5e765cbb
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
$ docker pull orientdb@sha256:94d28e76daf105136d503f46530d49ad164ab587a366e41e6fc6b6bc24b0a1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253447942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1bf09e2915979dcb5e8473582d7a5890ba86475611d0fe7a6cc9df25b6b3fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a7d9dbbaae17dfa6c691a11acd913a4b5bbb3b14720f69cad82f76c018a300`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 643.7 KB (643713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffbee63fc2885180214fa2cfb60b6793a7d0ed763e46bb2730bc6be9e0ecd0a`  
		Last Modified: Wed, 28 Aug 2024 18:55:49 GMT  
		Size: 104.9 MB (104850427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fb84a5293e0fb30108725ea74635b620a773bb83029330709d98c470ec09c5`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ef24fcb47dfc2fa28961d01ebb1388606aeb57715dc878068dc443a21abc0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ab8645b7bc7e14b298cee3252d755b77e3165cd65ea588f82fbc83bead57c1`

```dockerfile
```

-	Layers:
	-	`sha256:fb603a827e9fb9ff5a9b761ffe0544564984d18914e9fa563051b0172d98714e`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 3.2 MB (3153351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5687164606b2407640de918ffd43d50fb3097d46085511ae10f227b9d4a0daaa`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 16.8 KB (16790 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:6962d0ad9fd960f542f142738113dcd92ad1a2a4bffdc5a48cbd8575d731fa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245470383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a200fe2f6147d13d12e9d2d18cbf8d28de4c05f1315311c9690c25165a7facfa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca157c5a8f32699b98f64f551226b9973b08ff3235514c97dd9fa87a47368929`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 569.9 KB (569871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763455bcb6c7a08a7d2e231282a42e3faec8ff210858f6b30ddb0ea17478f104`  
		Last Modified: Wed, 28 Aug 2024 18:56:32 GMT  
		Size: 104.9 MB (104850387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208f4eb5582c8f06ea8e85454bc92286d72335f748255bfb5c26d2d9b1e866f`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0f549ff0eb687d46f07e04c0d0d6211f776dd26d943eba44417569952552dc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df408e57f7f9b84ae88b059b491ffc68dacb8462442ddb56f4ae9340898084da`

```dockerfile
```

-	Layers:
	-	`sha256:18c581d9d8a9a34e606912359d235f1906016fa7d73c5929d6557bae3d54afce`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 3.2 MB (3156054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d779c781174d3283ebc19914a6ec7ed73b313177d1e0e37d4d6d19bd278b330c`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 16.9 KB (16851 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:a93bd0e56dac867c29964c755c280951baa837580517f933a3e49b2682fd29db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251931753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff72f83c59f33c8e09597e5fc191bcfd356cce419f7c079e32179859697d25`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5df1cbe1ccdafa8e2bbe9d38fba90370beafd01dede6232d23b4553bbe244`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 638.9 KB (638871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c22ddb3329c48995e0be5499ac254eb899a6d3daa3cf3cf4a10400dd4c6286`  
		Last Modified: Wed, 28 Aug 2024 18:56:16 GMT  
		Size: 104.9 MB (104850369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a73145ca1750d4b0a52917ce65ad00b07f8849db78cbaa8c102f2b2eaf3313`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:22922d16215953cef761c1f00816afdc3acf88f249663ab0be940e10dae2d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e8034415e8c8e528c639bcf072fbafeb6ad8313bab88b99bcd82bca969803`

```dockerfile
```

-	Layers:
	-	`sha256:e74de5dddf83457bc4c64dcb3cc33766602429dd8a2fa9f2e96b4b6af8dd30a1`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 3.2 MB (3154412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d7e258065677b017408904647d46771503597b5c33cdeaaf7595e412fedceb`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.33`

```console
$ docker pull orientdb@sha256:6b1229f51d3cd7ba9f89f554c00e4af483e6bfab6f1a83cffe896d907d30c3e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.33` - linux; amd64

```console
$ docker pull orientdb@sha256:c3265bd6a276e423e95401cd93560fafa4139d0a560191c016cbbcc059da44e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221519423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc39d978d30f3de4fe01f58edb2b9098f26c6cb33d6ee13c8a45b9964be98be`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ada40b5897ea94f50109e8a0c35454335cedfbfd6554ea84510aa932091d7`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 643.7 KB (643709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b5be55402ba925b826dd6c980a540c442130e44c9eac39a49e6e38492a01e`  
		Last Modified: Wed, 28 Aug 2024 18:55:39 GMT  
		Size: 72.9 MB (72923233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33` - unknown; unknown

```console
$ docker pull orientdb@sha256:94e491a57ad977c9083407b6b6353acf7d0c9a1cb08a6c95223778cec8490a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ae22423ba9ebafa53ab7aa87c9909753687ff88df316c21093e0c9fd41f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:109ed6287e4a3287a33504504dc26c0067f6f13fb342093da1d44702e5e9717c`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281990b5a423dc8a2d0f3dabbc26cb7423134b6b03f25a3f6a5e5bf1680401a4`  
		Last Modified: Wed, 28 Aug 2024 18:55:36 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.33` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:ad8e166e57876333e411e2121c4e304ba78ed2f1babdb97dfc083a2861b7ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213541918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a58134cae102717973ebb458dd965ed7dfa4e9ac68e0b9297c02b79180a3d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a900fb3dd3e6f143da55254b0216a8571da804287291ca576d9e5d91a2f4e34`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 569.9 KB (569879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd9d7548ea5046aaa03a253e9ebfb9bc4e7feba42d9f0af40848e60acf6203`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 72.9 MB (72923234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33` - unknown; unknown

```console
$ docker pull orientdb@sha256:d6591c795f64537dd5c7c0495f39cc0fdf2c54aa66228904d61688a71aa6cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d399a0c983c5203bfa33ac8e6a8686213860edfdb0f78a3972ed334fc7bcf4b`

```dockerfile
```

-	Layers:
	-	`sha256:bbf9971b4f6d7cc90bc3f8c8f38b6105406ceee7489311588ab5f5888fa2cb80`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439056504c0af7f1a9afc4247e1378be6c9c5ac03cec418219390b21da916222`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 14.5 KB (14493 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.33` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:10766d99adc1dfe500774d87ab14631c999d99497aee1e7b3b720e76b8b2b578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220003248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d098c5124d048f13e55f3e764b700860f38d4e3d1ed362e97362cdffadd7a7c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2610358824c74ef46f21dbcdff4aedd5417091f979c7e6b6cada05f13765b4b1`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 638.8 KB (638848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0a5dd567e5a7a4833bcf95e9f263cd16457c4646d39130c50d6d0b806e203`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 72.9 MB (72923207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f75e6751a42a5ccac173cf446ca90f20a4259d92058e8cd3d62b8a612c25159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14890522a9134f5317d9ab702dae24ee226b0dfc165c69ccc2e9cc0bf9fb1542`

```dockerfile
```

-	Layers:
	-	`sha256:26c8b6d938957f781a45248871e6e200fbe4b9a635e60161d895c78ef1bcb235`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 3.0 MB (3031479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b757ec0a451038666fc8391531e0f83e7f303609f4ebc57c0411803680e39956`  
		Last Modified: Wed, 28 Aug 2024 18:55:31 GMT  
		Size: 14.7 KB (14721 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.33-tp3`

```console
$ docker pull orientdb@sha256:d21c6d769e82118a6545964a6ffc3acffce1cb053f3c0283a863623b5e765cbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.33-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:94d28e76daf105136d503f46530d49ad164ab587a366e41e6fc6b6bc24b0a1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253447942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1bf09e2915979dcb5e8473582d7a5890ba86475611d0fe7a6cc9df25b6b3fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a7d9dbbaae17dfa6c691a11acd913a4b5bbb3b14720f69cad82f76c018a300`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 643.7 KB (643713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffbee63fc2885180214fa2cfb60b6793a7d0ed763e46bb2730bc6be9e0ecd0a`  
		Last Modified: Wed, 28 Aug 2024 18:55:49 GMT  
		Size: 104.9 MB (104850427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fb84a5293e0fb30108725ea74635b620a773bb83029330709d98c470ec09c5`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ef24fcb47dfc2fa28961d01ebb1388606aeb57715dc878068dc443a21abc0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ab8645b7bc7e14b298cee3252d755b77e3165cd65ea588f82fbc83bead57c1`

```dockerfile
```

-	Layers:
	-	`sha256:fb603a827e9fb9ff5a9b761ffe0544564984d18914e9fa563051b0172d98714e`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 3.2 MB (3153351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5687164606b2407640de918ffd43d50fb3097d46085511ae10f227b9d4a0daaa`  
		Last Modified: Wed, 28 Aug 2024 18:55:46 GMT  
		Size: 16.8 KB (16790 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.33-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:6962d0ad9fd960f542f142738113dcd92ad1a2a4bffdc5a48cbd8575d731fa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245470383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a200fe2f6147d13d12e9d2d18cbf8d28de4c05f1315311c9690c25165a7facfa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca157c5a8f32699b98f64f551226b9973b08ff3235514c97dd9fa87a47368929`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 569.9 KB (569871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763455bcb6c7a08a7d2e231282a42e3faec8ff210858f6b30ddb0ea17478f104`  
		Last Modified: Wed, 28 Aug 2024 18:56:32 GMT  
		Size: 104.9 MB (104850387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208f4eb5582c8f06ea8e85454bc92286d72335f748255bfb5c26d2d9b1e866f`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:0f549ff0eb687d46f07e04c0d0d6211f776dd26d943eba44417569952552dc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df408e57f7f9b84ae88b059b491ffc68dacb8462442ddb56f4ae9340898084da`

```dockerfile
```

-	Layers:
	-	`sha256:18c581d9d8a9a34e606912359d235f1906016fa7d73c5929d6557bae3d54afce`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 3.2 MB (3156054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d779c781174d3283ebc19914a6ec7ed73b313177d1e0e37d4d6d19bd278b330c`  
		Last Modified: Wed, 28 Aug 2024 18:56:29 GMT  
		Size: 16.9 KB (16851 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.33-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:a93bd0e56dac867c29964c755c280951baa837580517f933a3e49b2682fd29db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251931753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff72f83c59f33c8e09597e5fc191bcfd356cce419f7c079e32179859697d25`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f75f2b418b6ba83d9e5931a620036693
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=658e1922ea022240969fdae79cc8cc8409caa335
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.33/orientdb-tp3-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[8182/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5df1cbe1ccdafa8e2bbe9d38fba90370beafd01dede6232d23b4553bbe244`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 638.9 KB (638871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c22ddb3329c48995e0be5499ac254eb899a6d3daa3cf3cf4a10400dd4c6286`  
		Last Modified: Wed, 28 Aug 2024 18:56:16 GMT  
		Size: 104.9 MB (104850369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a73145ca1750d4b0a52917ce65ad00b07f8849db78cbaa8c102f2b2eaf3313`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.33-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:22922d16215953cef761c1f00816afdc3acf88f249663ab0be940e10dae2d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e8034415e8c8e528c639bcf072fbafeb6ad8313bab88b99bcd82bca969803`

```dockerfile
```

-	Layers:
	-	`sha256:e74de5dddf83457bc4c64dcb3cc33766602429dd8a2fa9f2e96b4b6af8dd30a1`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 3.2 MB (3154412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d7e258065677b017408904647d46771503597b5c33cdeaaf7595e412fedceb`  
		Last Modified: Wed, 28 Aug 2024 18:56:13 GMT  
		Size: 17.1 KB (17076 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:6b1229f51d3cd7ba9f89f554c00e4af483e6bfab6f1a83cffe896d907d30c3e0
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
$ docker pull orientdb@sha256:c3265bd6a276e423e95401cd93560fafa4139d0a560191c016cbbcc059da44e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221519423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc39d978d30f3de4fe01f58edb2b9098f26c6cb33d6ee13c8a45b9964be98be`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ada40b5897ea94f50109e8a0c35454335cedfbfd6554ea84510aa932091d7`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 643.7 KB (643709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b5be55402ba925b826dd6c980a540c442130e44c9eac39a49e6e38492a01e`  
		Last Modified: Wed, 28 Aug 2024 18:55:39 GMT  
		Size: 72.9 MB (72923233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:94e491a57ad977c9083407b6b6353acf7d0c9a1cb08a6c95223778cec8490a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ae22423ba9ebafa53ab7aa87c9909753687ff88df316c21093e0c9fd41f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:109ed6287e4a3287a33504504dc26c0067f6f13fb342093da1d44702e5e9717c`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281990b5a423dc8a2d0f3dabbc26cb7423134b6b03f25a3f6a5e5bf1680401a4`  
		Last Modified: Wed, 28 Aug 2024 18:55:36 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:ad8e166e57876333e411e2121c4e304ba78ed2f1babdb97dfc083a2861b7ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213541918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a58134cae102717973ebb458dd965ed7dfa4e9ac68e0b9297c02b79180a3d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a900fb3dd3e6f143da55254b0216a8571da804287291ca576d9e5d91a2f4e34`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 569.9 KB (569879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd9d7548ea5046aaa03a253e9ebfb9bc4e7feba42d9f0af40848e60acf6203`  
		Last Modified: Wed, 28 Aug 2024 18:55:37 GMT  
		Size: 72.9 MB (72923234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:d6591c795f64537dd5c7c0495f39cc0fdf2c54aa66228904d61688a71aa6cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d399a0c983c5203bfa33ac8e6a8686213860edfdb0f78a3972ed334fc7bcf4b`

```dockerfile
```

-	Layers:
	-	`sha256:bbf9971b4f6d7cc90bc3f8c8f38b6105406ceee7489311588ab5f5888fa2cb80`  
		Last Modified: Wed, 28 Aug 2024 18:55:35 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439056504c0af7f1a9afc4247e1378be6c9c5ac03cec418219390b21da916222`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 14.5 KB (14493 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:10766d99adc1dfe500774d87ab14631c999d99497aee1e7b3b720e76b8b2b578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220003248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d098c5124d048f13e55f3e764b700860f38d4e3d1ed362e97362cdffadd7a7c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
# Wed, 28 Aug 2024 13:30:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 28 Aug 2024 13:30:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_VERSION=3.2.33
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=39619e431f8bd12a18722b25ef0e39fc
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=109fa0cdfbef3ae9b88578cfe1dcfd32b670184e
# Wed, 28 Aug 2024 13:30:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.33/orientdb-community-3.2.33.tar.gz
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Wed, 28 Aug 2024 13:30:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 13:30:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 28 Aug 2024 13:30:18 GMT
WORKDIR /orientdb
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2424/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
EXPOSE map[2480/tcp:{}]
# Wed, 28 Aug 2024 13:30:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2610358824c74ef46f21dbcdff4aedd5417091f979c7e6b6cada05f13765b4b1`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 638.8 KB (638848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0a5dd567e5a7a4833bcf95e9f263cd16457c4646d39130c50d6d0b806e203`  
		Last Modified: Wed, 28 Aug 2024 18:55:34 GMT  
		Size: 72.9 MB (72923207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f75e6751a42a5ccac173cf446ca90f20a4259d92058e8cd3d62b8a612c25159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14890522a9134f5317d9ab702dae24ee226b0dfc165c69ccc2e9cc0bf9fb1542`

```dockerfile
```

-	Layers:
	-	`sha256:26c8b6d938957f781a45248871e6e200fbe4b9a635e60161d895c78ef1bcb235`  
		Last Modified: Wed, 28 Aug 2024 18:55:32 GMT  
		Size: 3.0 MB (3031479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b757ec0a451038666fc8391531e0f83e7f303609f4ebc57c0411803680e39956`  
		Last Modified: Wed, 28 Aug 2024 18:55:31 GMT  
		Size: 14.7 KB (14721 bytes)  
		MIME: application/vnd.in-toto+json
