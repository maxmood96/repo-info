## `orientdb:latest`

```console
$ docker pull orientdb@sha256:f4af0a3fbbc1751da963d084906abb6267b09e41f84a848249512325ea6433ff
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
$ docker pull orientdb@sha256:3f1d2a7c104a0a97fb9153c273d9c5414012d8e048e661d50577d600591cbc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220924591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca24f8100f39d7cee58340fc1d3070870344ae7ea531b1b3a72cc64cc87e980`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:802008e7f7617aa11266de164e757a6c8d7bb57ed4c972cf7e9f519dd0a21708`  
		Last Modified: Fri, 11 Oct 2024 09:51:09 GMT  
		Size: 30.6 MB (30610919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da442b6a7976140ebd8a1198ded145af219e86718e91c0816eb4754dfa915aa`  
		Last Modified: Wed, 16 Oct 2024 02:16:59 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ce5efeaa4882ecccda95d3f09c5b65c90be69ec5d2578fc14c6a117222a3a`  
		Last Modified: Wed, 16 Oct 2024 02:17:05 GMT  
		Size: 103.6 MB (103615816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca9e9080f9d06790542a690c55856c9742680fd54ad9b91af6dc54c2d4fc914`  
		Last Modified: Wed, 16 Oct 2024 02:16:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9a4bbc5416f0431d9703cfe8abc2170b3ae5274fdc46d3334aa1caf817512`  
		Last Modified: Wed, 16 Oct 2024 02:16:56 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da1adcb50322a698003a9131318675ca9eddd8a0a94ed0d88795f4521ccc94`  
		Last Modified: Wed, 16 Oct 2024 16:13:55 GMT  
		Size: 72.9 MB (72924320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:5d173cd02205ca35617b31d69534b15317b598dee15a672a9b27fdf1b888334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19fb6a8f34a82ee4ce4e3adefd890c1d337c20f1af0249ecab044fbe08a2d55`

```dockerfile
```

-	Layers:
	-	`sha256:f8cc095b2bab74c654ca2f5bcc4f5cb8d39b001cab702922d5efea272ca7e2b3`  
		Last Modified: Wed, 16 Oct 2024 16:13:54 GMT  
		Size: 3.3 MB (3280735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad490c3c54a3b593be5e1cdbb1230e41e1f7d716290145af03dfc7d88ccd064`  
		Last Modified: Wed, 16 Oct 2024 16:13:54 GMT  
		Size: 14.4 KB (14449 bytes)  
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
$ docker pull orientdb@sha256:e44da1317c7b3009603993b0ee3a5c3069f11f9be30e91159eb9b9f0b305fae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219411025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5b70b68e4014628785db9f2fc1aa06f89316469f98fca63a21a7bac1a94535`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a41d12c80ea36c7de725d940c632c038bcc018950004c847f9988ae1278c83`  
		Last Modified: Wed, 16 Oct 2024 01:15:57 GMT  
		Size: 102.7 MB (102733006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7f521f3ca1a81d7bf44493178e821c82d4babdba47eda5dcbec9c3ff555409`  
		Last Modified: Wed, 16 Oct 2024 01:15:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f539c3016b2d48ba60e2ac9998883c4915741b5b175f716aebb1a5670d8d3b`  
		Last Modified: Wed, 16 Oct 2024 01:15:50 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7b19ef43ee0ce4c8d637e19f58be6ef453d3006624112642161e002773b5f3`  
		Last Modified: Wed, 16 Oct 2024 04:03:27 GMT  
		Size: 72.9 MB (72924326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f28f236019e4f39003495110fbb496693e60f317cc05d54c7895277b0363b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fafc228f2f182a4faf50ba3a1541b1d856d9e76995cf9560d94fe92696f7e7`

```dockerfile
```

-	Layers:
	-	`sha256:31631b10ec39538aec49eb1cb1813d2ae5a5f1ff78042523481aec541f289ea5`  
		Last Modified: Wed, 16 Oct 2024 04:03:25 GMT  
		Size: 3.3 MB (3281888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c989875541942852a5dabbb0c78241d9c870b10608cf352c9291eca6dd2f2acd`  
		Last Modified: Wed, 16 Oct 2024 04:03:24 GMT  
		Size: 14.6 KB (14550 bytes)  
		MIME: application/vnd.in-toto+json
