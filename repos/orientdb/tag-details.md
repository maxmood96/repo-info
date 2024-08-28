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
$ docker pull orientdb@sha256:0e5e6034f806b617aea9cb6c505febfc775326732e0a33183570e3c8891529f8
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
$ docker pull orientdb@sha256:0942c6a94cc734eb6610fa18660d1260edf62d869f0d08211f43b917608a0e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221515718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15be91951e83e6a8227e498c18c0543f5c25580e18c0ded70b3a30c2dd0b527e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd6fccc7082fa915848b9798736b78ab709f3b488136f34bdf46a391122d48`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 643.7 KB (643725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded1051a96f5fd1d5acd1f8c3ad8fbff40a5fd3187dbd688da43bf01d2aa3f87`  
		Last Modified: Fri, 23 Aug 2024 20:03:19 GMT  
		Size: 72.9 MB (72919512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:f059202595671523f4e71b3f3f223d87b8693ead411e641a987f7685c00effe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15de7729e3a61a913f27700bfe55bc633c63e26ad0488fbf6cf37730077469f7`

```dockerfile
```

-	Layers:
	-	`sha256:d8fedefccf8886bafd8ebb508b23296014596f059ec66276937cbe8cbd84a2d9`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd809d4a406af4c1bf72b715c9c465fd7bd146bed431756c221227c4c4085129`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 14.4 KB (14422 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:4d13acf92a79765da5ac2a32b03aaf7c916cba0e5ef8856c176c74c2b900c998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253577ea216b7c9d0a5fb1911c767b1c1028f49e2de1dc7541e636ff630b40c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db752149988dbb0bca8c7f9ab95acf57b926b0f30e51fa29ea79f12934d9debc`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 569.9 KB (569915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7552b71e5b008200b23f6a34126b7db351636d11655681c7ee478b4894d7d2`  
		Last Modified: Fri, 23 Aug 2024 20:31:52 GMT  
		Size: 72.9 MB (72919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:004b17eee16d421e8a903a8f0095fb9fececfd020a4e70892d1467fdb7cae746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c780385913d0c53b1ea1cf4e1ee6753a02f3359f3c26b5a89da711b11b55d14`

```dockerfile
```

-	Layers:
	-	`sha256:71f208d0557a8fb73065a434075a49593e44770e99a3ceb658824f3edd49fff6`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612ae5f8c566e3d8e58f4f2a868af3e703677c5cd62d07352424f8b1cfdc1f42`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 14.5 KB (14494 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:db9668dd5521ff999911599e44645f8e60d9708d627a4932140c5887638197da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219999602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07749479594ddf73ac4fed4d12ec202b93ea82d849ce014e19127617916c0416`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:f1e9d9210fa7eebc88690f9767308e36b3818af754284ff053e6504949dcf159`  
		Last Modified: Fri, 23 Aug 2024 22:53:16 GMT  
		Size: 638.9 KB (638874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9a58019699db8c2ab094e152b96e40d585f205710f7e9206d5077804500345`  
		Last Modified: Fri, 23 Aug 2024 22:53:19 GMT  
		Size: 72.9 MB (72919535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:e6fe291c4aad740f676b535d14ad867fd18395cfb60c905817ca890f9ef1b121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b37cce08a8b8b148c9071218eca0b4e3deaa37f4c6174eb4575e748848bd762`

```dockerfile
```

-	Layers:
	-	`sha256:19d856ab84c982927d99167f6150ed3d334730c480dda881225307dd507ef88e`  
		Last Modified: Fri, 23 Aug 2024 22:53:17 GMT  
		Size: 3.0 MB (3031479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f6b2712ca8ffe4f37b74ad2690023d358a74d46da1e4a1b2801115dea3734c`  
		Last Modified: Fri, 23 Aug 2024 22:53:16 GMT  
		Size: 14.7 KB (14721 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:d363a42f6db26e198dc3993fcaae0e09dd9c31514d2b5cf1c10c5826b6f35390
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
$ docker pull orientdb@sha256:ac3915a2888089cce0c481f3088e67999039aee240183eb4cc9d9c20f96efbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253443409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2447a15f5a31bdb374321dfca48e1d3887f063e6e0d92ae7d7da92dbeec4740`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392f9a1df9d460c2064e58604de6793bb7bfa5d0f6ee8e50934b6da60cc93be8`  
		Last Modified: Fri, 23 Aug 2024 20:03:10 GMT  
		Size: 643.7 KB (643726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4c5bcb88a503a7ff1b2148d1bb2dcfdd09b95a01edc2d941428582d8cb7d3f`  
		Last Modified: Fri, 23 Aug 2024 20:03:12 GMT  
		Size: 104.8 MB (104845885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f55c65feb1f08838d6cb45a41c6fc963ab898d6057a1ec12a10428f097b824`  
		Last Modified: Fri, 23 Aug 2024 20:03:10 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:dceaea49b497f01dbb8859737395975fc47b67700ad197ae76f6a1f9112d214f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb4ea84bbe99ef38072d916989ac640c863152c2bcd0df5acfcc0544e8457a7`

```dockerfile
```

-	Layers:
	-	`sha256:4023227687a6062825cfe5581d2b340031676f026cfa2444f1f835a930a3e1d9`  
		Last Modified: Fri, 23 Aug 2024 20:03:10 GMT  
		Size: 3.2 MB (3153351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc8552dcaf454ddde2d4179c45a9e46efeacbcbd0132dceed4070daad6642ea6`  
		Last Modified: Fri, 23 Aug 2024 20:03:10 GMT  
		Size: 16.8 KB (16790 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:223b2cd447cfce9e16ecd599a8e0a5456f1fafda5e762dd2c5f99e0ddfe90b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245465888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f67d03aadb0ab293bf9bfa5aa3dfb03159551539c979e2001c4a33bbb14521`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e150cd376bd59107b95a726bd046d63d60a1d563f0855c69fe50df864b5ef`  
		Last Modified: Fri, 23 Aug 2024 20:32:42 GMT  
		Size: 569.9 KB (569884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2354e0f1c9cddb0fb8ec8690bbaeffb203e0ac0fb3975655ae59e32d43cc16`  
		Last Modified: Fri, 23 Aug 2024 20:32:45 GMT  
		Size: 104.8 MB (104845880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317f5f332105f08961eaf54af6c9c8054d70ef5fd0468bc6c367dc7ac6629fad`  
		Last Modified: Fri, 23 Aug 2024 20:32:42 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e8e319b00b28aa33a552d8f210fbb6585824ba3f91845a46aaf807f3fe0734af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1b7af61b4240f4651fec4bfb4745f687491c67bb7f5ec3bcfef444710f67d`

```dockerfile
```

-	Layers:
	-	`sha256:5bcecce1b8b4be4540fc079d466af76d2185237621c017878a11e0305739af42`  
		Last Modified: Fri, 23 Aug 2024 20:32:42 GMT  
		Size: 3.2 MB (3156054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a8fdea0433f729715de730c44e762a4481945ac5750d0728f32441805b7350`  
		Last Modified: Fri, 23 Aug 2024 20:32:42 GMT  
		Size: 16.9 KB (16852 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:14a2915212aa2c410dce408da1412276b8146450eff8236a00aa8007abddf92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251927219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06104287a7f670c4603ba0c68e4b20d26f054e28aed5ec0311f6649bea531552`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:2aa697e6e44771d906ee472f4df19bf206d406e42b42d1f52990469426578d00`  
		Last Modified: Fri, 23 Aug 2024 22:53:58 GMT  
		Size: 638.9 KB (638859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0c4e69ada8326ec822053d692b7358402e065b8450a00d502bb5c63b2a00c1`  
		Last Modified: Fri, 23 Aug 2024 22:54:01 GMT  
		Size: 104.8 MB (104845847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de70ed113e340f39d72a4568dcd42ba52fa65d43cf3f3a9f2325e3cc7fd0ec1b`  
		Last Modified: Fri, 23 Aug 2024 22:53:58 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:777bb944608b98992910d6e7d5e315322f7394bc8348077a6449a279544c3e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b21f0809ec6170add1513bd73f3e36e2887137b4178a7483905414c6706150`

```dockerfile
```

-	Layers:
	-	`sha256:1278ac5c34934eaceda5f8f72bbbf7f88d462045d128847031634aed332c26b8`  
		Last Modified: Fri, 23 Aug 2024 22:53:58 GMT  
		Size: 3.2 MB (3154412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ce1f6a0375f11de60a5acb565d091bc67d05729243411d8fa4981f87af0589`  
		Last Modified: Fri, 23 Aug 2024 22:53:58 GMT  
		Size: 17.1 KB (17075 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.33`

```console
$ docker pull orientdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `orientdb:3.2.33-tp3`

```console
$ docker pull orientdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:0e5e6034f806b617aea9cb6c505febfc775326732e0a33183570e3c8891529f8
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
$ docker pull orientdb@sha256:0942c6a94cc734eb6610fa18660d1260edf62d869f0d08211f43b917608a0e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221515718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15be91951e83e6a8227e498c18c0543f5c25580e18c0ded70b3a30c2dd0b527e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:908723dcdab8ae296afc2c91ee627dde55d2b71eaf2c977d43feaacc83836ad9`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd6fccc7082fa915848b9798736b78ab709f3b488136f34bdf46a391122d48`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 643.7 KB (643725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded1051a96f5fd1d5acd1f8c3ad8fbff40a5fd3187dbd688da43bf01d2aa3f87`  
		Last Modified: Fri, 23 Aug 2024 20:03:19 GMT  
		Size: 72.9 MB (72919512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:f059202595671523f4e71b3f3f223d87b8693ead411e641a987f7685c00effe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3044828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15de7729e3a61a913f27700bfe55bc633c63e26ad0488fbf6cf37730077469f7`

```dockerfile
```

-	Layers:
	-	`sha256:d8fedefccf8886bafd8ebb508b23296014596f059ec66276937cbe8cbd84a2d9`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 3.0 MB (3030406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd809d4a406af4c1bf72b715c9c465fd7bd146bed431756c221227c4c4085129`  
		Last Modified: Fri, 23 Aug 2024 20:03:16 GMT  
		Size: 14.4 KB (14422 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:4d13acf92a79765da5ac2a32b03aaf7c916cba0e5ef8856c176c74c2b900c998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213538271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253577ea216b7c9d0a5fb1911c767b1c1028f49e2de1dc7541e636ff630b40c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:b611d2ff1d07aefe83c1a30b90580e162fed21b9ebe372a491cd6adec7f655a4`  
		Last Modified: Fri, 23 Aug 2024 18:59:03 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db752149988dbb0bca8c7f9ab95acf57b926b0f30e51fa29ea79f12934d9debc`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 569.9 KB (569915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7552b71e5b008200b23f6a34126b7db351636d11655681c7ee478b4894d7d2`  
		Last Modified: Fri, 23 Aug 2024 20:31:52 GMT  
		Size: 72.9 MB (72919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:004b17eee16d421e8a903a8f0095fb9fececfd020a4e70892d1467fdb7cae746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c780385913d0c53b1ea1cf4e1ee6753a02f3359f3c26b5a89da711b11b55d14`

```dockerfile
```

-	Layers:
	-	`sha256:71f208d0557a8fb73065a434075a49593e44770e99a3ceb658824f3edd49fff6`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 3.0 MB (3033117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612ae5f8c566e3d8e58f4f2a868af3e703677c5cd62d07352424f8b1cfdc1f42`  
		Last Modified: Fri, 23 Aug 2024 20:31:50 GMT  
		Size: 14.5 KB (14494 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:db9668dd5521ff999911599e44645f8e60d9708d627a4932140c5887638197da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219999602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07749479594ddf73ac4fed4d12ec202b93ea82d849ce014e19127617916c0416`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 16 Jul 2024 16:57:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:f1e9d9210fa7eebc88690f9767308e36b3818af754284ff053e6504949dcf159`  
		Last Modified: Fri, 23 Aug 2024 22:53:16 GMT  
		Size: 638.9 KB (638874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9a58019699db8c2ab094e152b96e40d585f205710f7e9206d5077804500345`  
		Last Modified: Fri, 23 Aug 2024 22:53:19 GMT  
		Size: 72.9 MB (72919535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:e6fe291c4aad740f676b535d14ad867fd18395cfb60c905817ca890f9ef1b121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b37cce08a8b8b148c9071218eca0b4e3deaa37f4c6174eb4575e748848bd762`

```dockerfile
```

-	Layers:
	-	`sha256:19d856ab84c982927d99167f6150ed3d334730c480dda881225307dd507ef88e`  
		Last Modified: Fri, 23 Aug 2024 22:53:17 GMT  
		Size: 3.0 MB (3031479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f6b2712ca8ffe4f37b74ad2690023d358a74d46da1e4a1b2801115dea3734c`  
		Last Modified: Fri, 23 Aug 2024 22:53:16 GMT  
		Size: 14.7 KB (14721 bytes)  
		MIME: application/vnd.in-toto+json
