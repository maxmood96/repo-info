<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.39`](#orientdb3239)
-	[`orientdb:3.2.39-tp3`](#orientdb3239-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:ad98ea29a27e3d47b91d48d93f4a33c82d44afed87642c1f9a0c9a74a0b0a830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:d08a51daf2a57441c2ccb3235db7de632b5521d134eebe5765582499bf10b580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154490159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22bcab5426cefa93afc026b511e676f62d6767ae8374c61cadbb4ddaf7f2b80`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ac50c127eb6d9a3eb24f13691c8a1084d40c3ec4fc8b4329fc875ee78fb0c7`  
		Last Modified: Mon, 05 May 2025 17:04:06 GMT  
		Size: 53.1 MB (53081017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:a6a97e1e795775db372402b144f3e329aa4f0be6c159ff189fa8e8a92a3cb5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3417007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee067be2dbc8855c03493bca0e6961b4d2bb77412b41c26119ce72b89c2d70e`

```dockerfile
```

-	Layers:
	-	`sha256:20437a9d1d6324ac0bdcb69fe460cf2b0d13017fe1710a392046de864abaa940`  
		Last Modified: Mon, 05 May 2025 17:04:06 GMT  
		Size: 3.4 MB (3402795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bf09f0f570654f6c3a2a6ecf38dbdb674bf1a5071a38a281bf201c52532706`  
		Last Modified: Mon, 05 May 2025 17:04:05 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:22c48d6268854a2bffd116c87c7a01412d1ae992ac3111be48b4c04f3f3ed467
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:3dc1d6bcc17349c653297f63e6b87d261187422f4a2f1543ec9f820537d2fbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177497261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0c6a20890a9596aa02774edd3af694eee8b1bf48f249ff740198ce5e1d5ef9`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6e59a2fdf6ac7316ebcdac23f8e5f65a034e713ef305a25dfed2e7cb3b56ae`  
		Last Modified: Mon, 05 May 2025 17:04:21 GMT  
		Size: 76.1 MB (76086741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad04d3e6ce4e579ad4e5903d49c710fb9c449c5f0fa48d737e219244a5bd0d4c`  
		Last Modified: Mon, 05 May 2025 17:04:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b8d3de72953c5e1e6df9aa5141999c6411f527816ffc149bef0d6d8731fed6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b610bbaeb8e24e46f3724703d3bb8040a829256923e2bbc0131492a51f703c`

```dockerfile
```

-	Layers:
	-	`sha256:20a4b1bf06258a13d6cb86e6e87b85cae4d4f2c89aebafa65646b232c8dc1bf6`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 3.5 MB (3464851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcbfcfebf8c4965637148d2678f5e4ce0ed6ae4fba871e99e0c5796267d135c`  
		Last Modified: Mon, 05 May 2025 17:04:18 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:ad98ea29a27e3d47b91d48d93f4a33c82d44afed87642c1f9a0c9a74a0b0a830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:d08a51daf2a57441c2ccb3235db7de632b5521d134eebe5765582499bf10b580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154490159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22bcab5426cefa93afc026b511e676f62d6767ae8374c61cadbb4ddaf7f2b80`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ac50c127eb6d9a3eb24f13691c8a1084d40c3ec4fc8b4329fc875ee78fb0c7`  
		Last Modified: Mon, 05 May 2025 17:04:06 GMT  
		Size: 53.1 MB (53081017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:a6a97e1e795775db372402b144f3e329aa4f0be6c159ff189fa8e8a92a3cb5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3417007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee067be2dbc8855c03493bca0e6961b4d2bb77412b41c26119ce72b89c2d70e`

```dockerfile
```

-	Layers:
	-	`sha256:20437a9d1d6324ac0bdcb69fe460cf2b0d13017fe1710a392046de864abaa940`  
		Last Modified: Mon, 05 May 2025 17:04:06 GMT  
		Size: 3.4 MB (3402795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7bf09f0f570654f6c3a2a6ecf38dbdb674bf1a5071a38a281bf201c52532706`  
		Last Modified: Mon, 05 May 2025 17:04:05 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:22c48d6268854a2bffd116c87c7a01412d1ae992ac3111be48b4c04f3f3ed467
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:3dc1d6bcc17349c653297f63e6b87d261187422f4a2f1543ec9f820537d2fbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177497261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0c6a20890a9596aa02774edd3af694eee8b1bf48f249ff740198ce5e1d5ef9`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6e59a2fdf6ac7316ebcdac23f8e5f65a034e713ef305a25dfed2e7cb3b56ae`  
		Last Modified: Mon, 05 May 2025 17:04:21 GMT  
		Size: 76.1 MB (76086741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad04d3e6ce4e579ad4e5903d49c710fb9c449c5f0fa48d737e219244a5bd0d4c`  
		Last Modified: Mon, 05 May 2025 17:04:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b8d3de72953c5e1e6df9aa5141999c6411f527816ffc149bef0d6d8731fed6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b610bbaeb8e24e46f3724703d3bb8040a829256923e2bbc0131492a51f703c`

```dockerfile
```

-	Layers:
	-	`sha256:20a4b1bf06258a13d6cb86e6e87b85cae4d4f2c89aebafa65646b232c8dc1bf6`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 3.5 MB (3464851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcbfcfebf8c4965637148d2678f5e4ce0ed6ae4fba871e99e0c5796267d135c`  
		Last Modified: Mon, 05 May 2025 17:04:18 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:75773f96a82bb695f1cc9d96c29b26f21223b843e725fd7a8a6d32997a714152
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
$ docker pull orientdb@sha256:dd7db6658aa0e68cf39ed8638eccc645ae500ae52051cc8a267f49bc7b233a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19d25537611c0c48b0fc69e0da1a65cad9a1ec653564bff8ea2350ea2c48036`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c121269683fe2e9c55f0deef715507654a1547306b22c220c50d4b880370a087`  
		Last Modified: Mon, 05 May 2025 17:04:13 GMT  
		Size: 72.9 MB (72930459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:2e17cbec653c00e14517e39b4288f3472fc1f22abddebcd8f223f2b869b8d5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c35dc4be7dfdfa3948555d942612e794411f86fd314493c125aaecabcc27`

```dockerfile
```

-	Layers:
	-	`sha256:9adbdbf113d4b29b7fcaaaa11e889ab70cefbca758fa3e30bc114191706d0354`  
		Last Modified: Mon, 05 May 2025 17:04:12 GMT  
		Size: 3.4 MB (3412173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175cfc1d457798f0920bc45e816faa704bf5efa99d87c5b3a783ceb3404d751b`  
		Last Modified: Mon, 05 May 2025 17:04:11 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:d37a2af5d4e461bef289e8ba3913ad766de1f7a553f7827d0f145768005822f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ac4b7269900e1cb88b63d2ae26ee23ef0c699fc3191be7f4df52edd04763ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b157f780e653c1a33073cc6ccdbc3112316290660924adc18d51cd4324712`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 16.3 MB (16304423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ccb0100256bf04a7a03990abd99cc1d862727c2f1d20f5a2cfac8b8e7517d`  
		Last Modified: Mon, 05 May 2025 16:37:29 GMT  
		Size: 50.1 MB (50117420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247602be3f7100b1e02cd5c1366819fe146c0d9d70eb175cf0d99fd75f4f3a1`  
		Last Modified: Mon, 05 May 2025 16:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11173ee8c2afd8e4ec8ac8982e449ad41a73217fc87b69abacb63366898b63d`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a3da3675234c91b5245bf76a56108c89670c5737ccf4e279bcf41433b0b4eb`  
		Last Modified: Mon, 05 May 2025 17:18:44 GMT  
		Size: 72.9 MB (72930462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:940f46a6838e36fac2a49c3af2625ccba39251584b83819d8e98fb3677c41da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a9f62a2f7032f8384e76f07888e3a60888e7abd2aff998a19cd7fbab4668de`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8ab96b0ee8b06e84e59db0bc6874243403f76adb91e18ba1e480f4126dbb7`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 3.4 MB (3415857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f530bbc30ad7d7ce2c4e60374751097e0438dd3b5f73198aa88af6603792ffc8`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 14.6 KB (14595 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:a2aa5e518309567843a22f5fe0ca9834456340a105f7a2b41d98790332969599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172600737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12f994fa75b9fdd48fe2a187fea81c577f83b7a968699de8a84236ad8727465`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddf57e92260f1e2b02ff57bd9a27f7bdd5bdc116e4cc25a262267aaa648500`  
		Last Modified: Mon, 28 Apr 2025 20:08:08 GMT  
		Size: 53.8 MB (53833592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b763057c52c312ef65f7de21020ca6aa5aa2248b86bb93a3940bb0594cb49e80`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2f4802cf80a4f517265104e55a6c5ac1a339280cc77b78f6cf92b4e82b7974`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b15026d7732ed082aa7a679c4ab1858d15beb379774f73abfdc89385e4e8f`  
		Last Modified: Mon, 28 Apr 2025 21:10:56 GMT  
		Size: 72.9 MB (72930448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:4f12eeb7ec669be3efb7674a3faf4103a8df16308cf4de3c8dd14ad23c2007f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3427946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd4c18b3f6f8c0d3ab1bd77791078165637a5218e43a0bfa10b3bf59b938691`

```dockerfile
```

-	Layers:
	-	`sha256:326a3619b965badcb338c732e7ec702067bd4840aca582ab346632de2a04b151`  
		Last Modified: Mon, 28 Apr 2025 21:10:54 GMT  
		Size: 3.4 MB (3413326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2e8791ae6957cd1836d39bc63fe8bd9df32dc7a3ff9b76249f2e6153913d49`  
		Last Modified: Mon, 28 Apr 2025 21:10:53 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:548a177fdb8785188ee941663b9eb2a6b61a1d1127f79859a3d15bf64483252a
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
$ docker pull orientdb@sha256:808d2cb11139b21dcdcc7524b1fdfac5b1b161714652036df39da6ca0d0d908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206265989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8da8b4adee92abc29a8238c0327f0fc9c51fbf53692e147cdfd055250bc408`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b66ca91c1033086da4d6e1eab279b559cee0474ed5a584787cb0385c1300de`  
		Last Modified: Mon, 05 May 2025 17:04:22 GMT  
		Size: 104.9 MB (104855477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0433418279ea4644e84faae2a5feb3154ce2f9c40d4d922b97e98183060892e`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:5af996d46444671bcbc5a0b490c91128a6dc7377cf972359c48b43482b49088a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b7a9155b55d004f0ac3057a6129edce55f984f49bf8c4ce6eaac92db77af9f`

```dockerfile
```

-	Layers:
	-	`sha256:762f8de26136fed84e0b5cba61f1fb41595736024f43f3314e7aaabe4092fb0b`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 3.5 MB (3542829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03ee3d3e018ba23bda81b386cf57310701650cfff8d83daccf0bbd0300db289`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:952458ae93850b3f8f8a5a457293c12e2d8b2f354aaaf7abf68d6f879a1e3bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198119011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838f3b2688476b6f00bee48dcf35907c63fc4d48d640b0ad9d5643f3b04fb20a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b157f780e653c1a33073cc6ccdbc3112316290660924adc18d51cd4324712`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 16.3 MB (16304423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ccb0100256bf04a7a03990abd99cc1d862727c2f1d20f5a2cfac8b8e7517d`  
		Last Modified: Mon, 05 May 2025 16:37:29 GMT  
		Size: 50.1 MB (50117420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247602be3f7100b1e02cd5c1366819fe146c0d9d70eb175cf0d99fd75f4f3a1`  
		Last Modified: Mon, 05 May 2025 16:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11173ee8c2afd8e4ec8ac8982e449ad41a73217fc87b69abacb63366898b63d`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f247ecfeeeb2a946e3dd00a7ca302c5c961d427f79b7ea0206bd84c128f5026`  
		Last Modified: Mon, 05 May 2025 17:19:38 GMT  
		Size: 104.9 MB (104855516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120219c96b3a81c5e3cedae64d0841af7c1560e6d20dba47dfcb3eacc6ccae83`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b931b9fba2c13ac82dd1e769811a9b3cf5ee012f5af63432519525fcf6fa109b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca52f203db983503108738d3bf511f390e3a0c89ea621efd151ca6d6a7929f`

```dockerfile
```

-	Layers:
	-	`sha256:aa5567f528057ab3bbdd158c0c8ebff2458fae044cb5cc8906989c359c33419f`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 3.5 MB (3546505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5aa2398c6f8cdd872c97e91b38b63b23ffc3c5867a0023198196272132535a`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 16.9 KB (16918 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:d47f01d5797776e8c25f5f4422c9208d4cd4c5bab66e69b10ae5552e67f45ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204527153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd65a93e68e83a66bdd50002d45fd7b4da2d0e867efa77f191e024800cf87c7d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddf57e92260f1e2b02ff57bd9a27f7bdd5bdc116e4cc25a262267aaa648500`  
		Last Modified: Mon, 28 Apr 2025 20:08:08 GMT  
		Size: 53.8 MB (53833592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b763057c52c312ef65f7de21020ca6aa5aa2248b86bb93a3940bb0594cb49e80`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2f4802cf80a4f517265104e55a6c5ac1a339280cc77b78f6cf92b4e82b7974`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0e22b0cc278e44886d0a5e631e411e2ee0554a0aef48d9dd0141e101e94c7a`  
		Last Modified: Mon, 28 Apr 2025 21:11:26 GMT  
		Size: 104.9 MB (104855494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83013adac44c5056c76791e2b78782074daf683f187eed3762548412025bcc29`  
		Last Modified: Mon, 28 Apr 2025 21:11:23 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:f2250d382f3144290ca6810ba088d51cf30d2db503408de5db8117d9438922a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d3c3885c8982315c1f85f13ede76e02b0aaab9b55907fda84f34b65f3657c4`

```dockerfile
```

-	Layers:
	-	`sha256:514bc336c336b3b40be593b8dd450d6f5aaab4e3ee296273abff6550160ff818`  
		Last Modified: Mon, 28 Apr 2025 21:11:24 GMT  
		Size: 3.5 MB (3543970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59212137a5f1c4c0c5774ec599e34ba9f7c3fb049eea78f331edd667bea8074e`  
		Last Modified: Mon, 28 Apr 2025 21:11:23 GMT  
		Size: 16.9 KB (16941 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.39`

```console
$ docker pull orientdb@sha256:75773f96a82bb695f1cc9d96c29b26f21223b843e725fd7a8a6d32997a714152
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.39` - linux; amd64

```console
$ docker pull orientdb@sha256:dd7db6658aa0e68cf39ed8638eccc645ae500ae52051cc8a267f49bc7b233a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19d25537611c0c48b0fc69e0da1a65cad9a1ec653564bff8ea2350ea2c48036`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c121269683fe2e9c55f0deef715507654a1547306b22c220c50d4b880370a087`  
		Last Modified: Mon, 05 May 2025 17:04:13 GMT  
		Size: 72.9 MB (72930459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39` - unknown; unknown

```console
$ docker pull orientdb@sha256:2e17cbec653c00e14517e39b4288f3472fc1f22abddebcd8f223f2b869b8d5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c35dc4be7dfdfa3948555d942612e794411f86fd314493c125aaecabcc27`

```dockerfile
```

-	Layers:
	-	`sha256:9adbdbf113d4b29b7fcaaaa11e889ab70cefbca758fa3e30bc114191706d0354`  
		Last Modified: Mon, 05 May 2025 17:04:12 GMT  
		Size: 3.4 MB (3412173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175cfc1d457798f0920bc45e816faa704bf5efa99d87c5b3a783ceb3404d751b`  
		Last Modified: Mon, 05 May 2025 17:04:11 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:d37a2af5d4e461bef289e8ba3913ad766de1f7a553f7827d0f145768005822f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ac4b7269900e1cb88b63d2ae26ee23ef0c699fc3191be7f4df52edd04763ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b157f780e653c1a33073cc6ccdbc3112316290660924adc18d51cd4324712`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 16.3 MB (16304423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ccb0100256bf04a7a03990abd99cc1d862727c2f1d20f5a2cfac8b8e7517d`  
		Last Modified: Mon, 05 May 2025 16:37:29 GMT  
		Size: 50.1 MB (50117420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247602be3f7100b1e02cd5c1366819fe146c0d9d70eb175cf0d99fd75f4f3a1`  
		Last Modified: Mon, 05 May 2025 16:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11173ee8c2afd8e4ec8ac8982e449ad41a73217fc87b69abacb63366898b63d`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a3da3675234c91b5245bf76a56108c89670c5737ccf4e279bcf41433b0b4eb`  
		Last Modified: Mon, 05 May 2025 17:18:44 GMT  
		Size: 72.9 MB (72930462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39` - unknown; unknown

```console
$ docker pull orientdb@sha256:940f46a6838e36fac2a49c3af2625ccba39251584b83819d8e98fb3677c41da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a9f62a2f7032f8384e76f07888e3a60888e7abd2aff998a19cd7fbab4668de`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8ab96b0ee8b06e84e59db0bc6874243403f76adb91e18ba1e480f4126dbb7`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 3.4 MB (3415857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f530bbc30ad7d7ce2c4e60374751097e0438dd3b5f73198aa88af6603792ffc8`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 14.6 KB (14595 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:a2aa5e518309567843a22f5fe0ca9834456340a105f7a2b41d98790332969599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172600737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12f994fa75b9fdd48fe2a187fea81c577f83b7a968699de8a84236ad8727465`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddf57e92260f1e2b02ff57bd9a27f7bdd5bdc116e4cc25a262267aaa648500`  
		Last Modified: Mon, 28 Apr 2025 20:08:08 GMT  
		Size: 53.8 MB (53833592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b763057c52c312ef65f7de21020ca6aa5aa2248b86bb93a3940bb0594cb49e80`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2f4802cf80a4f517265104e55a6c5ac1a339280cc77b78f6cf92b4e82b7974`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b15026d7732ed082aa7a679c4ab1858d15beb379774f73abfdc89385e4e8f`  
		Last Modified: Mon, 28 Apr 2025 21:10:56 GMT  
		Size: 72.9 MB (72930448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39` - unknown; unknown

```console
$ docker pull orientdb@sha256:4f12eeb7ec669be3efb7674a3faf4103a8df16308cf4de3c8dd14ad23c2007f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3427946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd4c18b3f6f8c0d3ab1bd77791078165637a5218e43a0bfa10b3bf59b938691`

```dockerfile
```

-	Layers:
	-	`sha256:326a3619b965badcb338c732e7ec702067bd4840aca582ab346632de2a04b151`  
		Last Modified: Mon, 28 Apr 2025 21:10:54 GMT  
		Size: 3.4 MB (3413326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2e8791ae6957cd1836d39bc63fe8bd9df32dc7a3ff9b76249f2e6153913d49`  
		Last Modified: Mon, 28 Apr 2025 21:10:53 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.39-tp3`

```console
$ docker pull orientdb@sha256:548a177fdb8785188ee941663b9eb2a6b61a1d1127f79859a3d15bf64483252a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.39-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:808d2cb11139b21dcdcc7524b1fdfac5b1b161714652036df39da6ca0d0d908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206265989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8da8b4adee92abc29a8238c0327f0fc9c51fbf53692e147cdfd055250bc408`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b66ca91c1033086da4d6e1eab279b559cee0474ed5a584787cb0385c1300de`  
		Last Modified: Mon, 05 May 2025 17:04:22 GMT  
		Size: 104.9 MB (104855477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0433418279ea4644e84faae2a5feb3154ce2f9c40d4d922b97e98183060892e`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:5af996d46444671bcbc5a0b490c91128a6dc7377cf972359c48b43482b49088a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b7a9155b55d004f0ac3057a6129edce55f984f49bf8c4ce6eaac92db77af9f`

```dockerfile
```

-	Layers:
	-	`sha256:762f8de26136fed84e0b5cba61f1fb41595736024f43f3314e7aaabe4092fb0b`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 3.5 MB (3542829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03ee3d3e018ba23bda81b386cf57310701650cfff8d83daccf0bbd0300db289`  
		Last Modified: Mon, 05 May 2025 17:04:19 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:952458ae93850b3f8f8a5a457293c12e2d8b2f354aaaf7abf68d6f879a1e3bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198119011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838f3b2688476b6f00bee48dcf35907c63fc4d48d640b0ad9d5643f3b04fb20a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b157f780e653c1a33073cc6ccdbc3112316290660924adc18d51cd4324712`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 16.3 MB (16304423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ccb0100256bf04a7a03990abd99cc1d862727c2f1d20f5a2cfac8b8e7517d`  
		Last Modified: Mon, 05 May 2025 16:37:29 GMT  
		Size: 50.1 MB (50117420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247602be3f7100b1e02cd5c1366819fe146c0d9d70eb175cf0d99fd75f4f3a1`  
		Last Modified: Mon, 05 May 2025 16:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11173ee8c2afd8e4ec8ac8982e449ad41a73217fc87b69abacb63366898b63d`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f247ecfeeeb2a946e3dd00a7ca302c5c961d427f79b7ea0206bd84c128f5026`  
		Last Modified: Mon, 05 May 2025 17:19:38 GMT  
		Size: 104.9 MB (104855516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120219c96b3a81c5e3cedae64d0841af7c1560e6d20dba47dfcb3eacc6ccae83`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b931b9fba2c13ac82dd1e769811a9b3cf5ee012f5af63432519525fcf6fa109b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca52f203db983503108738d3bf511f390e3a0c89ea621efd151ca6d6a7929f`

```dockerfile
```

-	Layers:
	-	`sha256:aa5567f528057ab3bbdd158c0c8ebff2458fae044cb5cc8906989c359c33419f`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 3.5 MB (3546505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5aa2398c6f8cdd872c97e91b38b63b23ffc3c5867a0023198196272132535a`  
		Last Modified: Mon, 05 May 2025 17:19:34 GMT  
		Size: 16.9 KB (16918 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:d47f01d5797776e8c25f5f4422c9208d4cd4c5bab66e69b10ae5552e67f45ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204527153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd65a93e68e83a66bdd50002d45fd7b4da2d0e867efa77f191e024800cf87c7d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=52f255465bfecafbe1a2a5ef864fda1e
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a7354d84b605e07cc4bb74e937b67821f9e6760d
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.39/orientdb-tp3-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[8182/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddf57e92260f1e2b02ff57bd9a27f7bdd5bdc116e4cc25a262267aaa648500`  
		Last Modified: Mon, 28 Apr 2025 20:08:08 GMT  
		Size: 53.8 MB (53833592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b763057c52c312ef65f7de21020ca6aa5aa2248b86bb93a3940bb0594cb49e80`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2f4802cf80a4f517265104e55a6c5ac1a339280cc77b78f6cf92b4e82b7974`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0e22b0cc278e44886d0a5e631e411e2ee0554a0aef48d9dd0141e101e94c7a`  
		Last Modified: Mon, 28 Apr 2025 21:11:26 GMT  
		Size: 104.9 MB (104855494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83013adac44c5056c76791e2b78782074daf683f187eed3762548412025bcc29`  
		Last Modified: Mon, 28 Apr 2025 21:11:23 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:f2250d382f3144290ca6810ba088d51cf30d2db503408de5db8117d9438922a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d3c3885c8982315c1f85f13ede76e02b0aaab9b55907fda84f34b65f3657c4`

```dockerfile
```

-	Layers:
	-	`sha256:514bc336c336b3b40be593b8dd450d6f5aaab4e3ee296273abff6550160ff818`  
		Last Modified: Mon, 28 Apr 2025 21:11:24 GMT  
		Size: 3.5 MB (3543970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59212137a5f1c4c0c5774ec599e34ba9f7c3fb049eea78f331edd667bea8074e`  
		Last Modified: Mon, 28 Apr 2025 21:11:23 GMT  
		Size: 16.9 KB (16941 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:75773f96a82bb695f1cc9d96c29b26f21223b843e725fd7a8a6d32997a714152
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
$ docker pull orientdb@sha256:dd7db6658aa0e68cf39ed8638eccc645ae500ae52051cc8a267f49bc7b233a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19d25537611c0c48b0fc69e0da1a65cad9a1ec653564bff8ea2350ea2c48036`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Mon, 05 May 2025 16:34:48 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Mon, 05 May 2025 16:34:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c121269683fe2e9c55f0deef715507654a1547306b22c220c50d4b880370a087`  
		Last Modified: Mon, 05 May 2025 17:04:13 GMT  
		Size: 72.9 MB (72930459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:2e17cbec653c00e14517e39b4288f3472fc1f22abddebcd8f223f2b869b8d5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9679c35dc4be7dfdfa3948555d942612e794411f86fd314493c125aaecabcc27`

```dockerfile
```

-	Layers:
	-	`sha256:9adbdbf113d4b29b7fcaaaa11e889ab70cefbca758fa3e30bc114191706d0354`  
		Last Modified: Mon, 05 May 2025 17:04:12 GMT  
		Size: 3.4 MB (3412173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175cfc1d457798f0920bc45e816faa704bf5efa99d87c5b3a783ceb3404d751b`  
		Last Modified: Mon, 05 May 2025 17:04:11 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:d37a2af5d4e461bef289e8ba3913ad766de1f7a553f7827d0f145768005822f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ac4b7269900e1cb88b63d2ae26ee23ef0c699fc3191be7f4df52edd04763ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 14 Apr 2025 15:49:16 GMT
ARG RELEASE
# Mon, 14 Apr 2025 15:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Apr 2025 15:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 14 Apr 2025 15:49:16 GMT
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Mon, 28 Apr 2025 10:54:02 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b157f780e653c1a33073cc6ccdbc3112316290660924adc18d51cd4324712`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 16.3 MB (16304423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ccb0100256bf04a7a03990abd99cc1d862727c2f1d20f5a2cfac8b8e7517d`  
		Last Modified: Mon, 05 May 2025 16:37:29 GMT  
		Size: 50.1 MB (50117420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247602be3f7100b1e02cd5c1366819fe146c0d9d70eb175cf0d99fd75f4f3a1`  
		Last Modified: Mon, 05 May 2025 16:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11173ee8c2afd8e4ec8ac8982e449ad41a73217fc87b69abacb63366898b63d`  
		Last Modified: Mon, 05 May 2025 16:37:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a3da3675234c91b5245bf76a56108c89670c5737ccf4e279bcf41433b0b4eb`  
		Last Modified: Mon, 05 May 2025 17:18:44 GMT  
		Size: 72.9 MB (72930462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:940f46a6838e36fac2a49c3af2625ccba39251584b83819d8e98fb3677c41da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a9f62a2f7032f8384e76f07888e3a60888e7abd2aff998a19cd7fbab4668de`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8ab96b0ee8b06e84e59db0bc6874243403f76adb91e18ba1e480f4126dbb7`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 3.4 MB (3415857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f530bbc30ad7d7ce2c4e60374751097e0438dd3b5f73198aa88af6603792ffc8`  
		Last Modified: Mon, 05 May 2025 17:18:41 GMT  
		Size: 14.6 KB (14595 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:a2aa5e518309567843a22f5fe0ca9834456340a105f7a2b41d98790332969599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172600737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12f994fa75b9fdd48fe2a187fea81c577f83b7a968699de8a84236ad8727465`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Apr 2025 15:49:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 14 Apr 2025 15:49:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_VERSION=3.2.39
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0d6df6bc6191c28ea3541168159495b8
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8cad76fdbfe132a7229833ee3d64566043cae22a
# Mon, 14 Apr 2025 15:49:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.39/orientdb-community-3.2.39.tar.gz
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Mon, 14 Apr 2025 15:49:16 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 15:49:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 14 Apr 2025 15:49:16 GMT
WORKDIR /orientdb
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2424/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
EXPOSE map[2480/tcp:{}]
# Mon, 14 Apr 2025 15:49:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddf57e92260f1e2b02ff57bd9a27f7bdd5bdc116e4cc25a262267aaa648500`  
		Last Modified: Mon, 28 Apr 2025 20:08:08 GMT  
		Size: 53.8 MB (53833592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b763057c52c312ef65f7de21020ca6aa5aa2248b86bb93a3940bb0594cb49e80`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2f4802cf80a4f517265104e55a6c5ac1a339280cc77b78f6cf92b4e82b7974`  
		Last Modified: Mon, 28 Apr 2025 20:08:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b15026d7732ed082aa7a679c4ab1858d15beb379774f73abfdc89385e4e8f`  
		Last Modified: Mon, 28 Apr 2025 21:10:56 GMT  
		Size: 72.9 MB (72930448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:4f12eeb7ec669be3efb7674a3faf4103a8df16308cf4de3c8dd14ad23c2007f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3427946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd4c18b3f6f8c0d3ab1bd77791078165637a5218e43a0bfa10b3bf59b938691`

```dockerfile
```

-	Layers:
	-	`sha256:326a3619b965badcb338c732e7ec702067bd4840aca582ab346632de2a04b151`  
		Last Modified: Mon, 28 Apr 2025 21:10:54 GMT  
		Size: 3.4 MB (3413326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af2e8791ae6957cd1836d39bc63fe8bd9df32dc7a3ff9b76249f2e6153913d49`  
		Last Modified: Mon, 28 Apr 2025 21:10:53 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json
