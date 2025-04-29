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
$ docker pull orientdb@sha256:686aac027896f98386f686a622df1b26f2ba05a1988748e07990c6bf703386c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:fa2b18b04df959993c0653c7a088103cc960f89b90892379fba2fdbe6c38bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154490385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031128fbbe35343789d0cd785608987a6a65d0c894b00750bc61fd0f13dc23c`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5315063b1781a9478f68c3efd1d6328129e5844bfcd8e2adce465de0dacc8af9`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 53.1 MB (53081034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:a9fae8f340db7b37a4a196bed0c378ea80bd4468238a1b1f1b6ab012ebbb02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3417003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edefcc3df18ebaa8086dfa5ec3b3f77a4e117e3db83eea2b2e1542798061a8d`

```dockerfile
```

-	Layers:
	-	`sha256:78ab43c8507e5fbaf68b1395d9966ceb2b63e708e527f47f4e2c8c9fe97fea75`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 3.4 MB (3402791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4aa752b13e737b345b402363b825df6be25e52ee02d4d350bf64ae62f300997`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:cb8dcbe9917928a4bd35581c1438421275969b56104a49db4d5a232db3170145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:9a55844c958c9809bceab9bc61e4a93782bf819ce5e4448d781d851ddae9de23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177497319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a343c7a47601b9f980eef3c496fbee2dda14121937cf862311b1c56063fc3d8c`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922ceb92a697f906725b1ab3eed4f5cff8ce9aa2653796850ce6b2d765b9c6d`  
		Last Modified: Mon, 28 Apr 2025 20:50:43 GMT  
		Size: 76.1 MB (76086596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032d3abab63053a75ef4667ad8a879bdfc7406427471ce6efb204a2fb4826f14`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:4b486ee41a0e4dba61bd8e6af2a8e83bdca1b09ceaf8903ace7591d57462f1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3065b33117cec62a8366157143fa9f1573fa4ce1150a97bcbe684051b65afb76`

```dockerfile
```

-	Layers:
	-	`sha256:aff0974bd9d51cbaaad4c4dc42e07b5744f642046c7438435617cfdefb7fcc8d`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 3.5 MB (3464847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45ecacfc14212266c107492bceb24bda7162e0963dfaeb47f8a2383027fe8fa`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:686aac027896f98386f686a622df1b26f2ba05a1988748e07990c6bf703386c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:fa2b18b04df959993c0653c7a088103cc960f89b90892379fba2fdbe6c38bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154490385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031128fbbe35343789d0cd785608987a6a65d0c894b00750bc61fd0f13dc23c`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5315063b1781a9478f68c3efd1d6328129e5844bfcd8e2adce465de0dacc8af9`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 53.1 MB (53081034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:a9fae8f340db7b37a4a196bed0c378ea80bd4468238a1b1f1b6ab012ebbb02ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3417003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edefcc3df18ebaa8086dfa5ec3b3f77a4e117e3db83eea2b2e1542798061a8d`

```dockerfile
```

-	Layers:
	-	`sha256:78ab43c8507e5fbaf68b1395d9966ceb2b63e708e527f47f4e2c8c9fe97fea75`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 3.4 MB (3402791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4aa752b13e737b345b402363b825df6be25e52ee02d4d350bf64ae62f300997`  
		Last Modified: Mon, 28 Apr 2025 20:50:41 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:cb8dcbe9917928a4bd35581c1438421275969b56104a49db4d5a232db3170145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:9a55844c958c9809bceab9bc61e4a93782bf819ce5e4448d781d851ddae9de23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177497319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a343c7a47601b9f980eef3c496fbee2dda14121937cf862311b1c56063fc3d8c`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922ceb92a697f906725b1ab3eed4f5cff8ce9aa2653796850ce6b2d765b9c6d`  
		Last Modified: Mon, 28 Apr 2025 20:50:43 GMT  
		Size: 76.1 MB (76086596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032d3abab63053a75ef4667ad8a879bdfc7406427471ce6efb204a2fb4826f14`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:4b486ee41a0e4dba61bd8e6af2a8e83bdca1b09ceaf8903ace7591d57462f1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3065b33117cec62a8366157143fa9f1573fa4ce1150a97bcbe684051b65afb76`

```dockerfile
```

-	Layers:
	-	`sha256:aff0974bd9d51cbaaad4c4dc42e07b5744f642046c7438435617cfdefb7fcc8d`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 3.5 MB (3464847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45ecacfc14212266c107492bceb24bda7162e0963dfaeb47f8a2383027fe8fa`  
		Last Modified: Mon, 28 Apr 2025 20:50:42 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:659df4ecc8f78f2a900ccceca990d4359eb084153257521d7f6e6aec1ad962a5
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
$ docker pull orientdb@sha256:b1963106c7da70f7a2c0987b58c49d7e4fd0890bafa7ce91bbb7e53535ab19bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce69a08d5022f414c33c6b0a315622fb8145b5e59a40ca701073ae82494241`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d49df540b80bf37973230f1306c50217b704a7ef5c4f2fed542ce90a086929`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 72.9 MB (72930477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f77a419f7715e6d6c012d4dacdc88c9ee35bedb0ab110633dd494b9f0089415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b9747e6b05a653327b93920e1bb20decf9c7d22ac6af43f6a871e4b6d529ee`

```dockerfile
```

-	Layers:
	-	`sha256:3a582dbb17ba00be07c9c04fa143b924ba0725fe5c3d9991cb9bb179470d7fa1`  
		Last Modified: Mon, 28 Apr 2025 20:51:25 GMT  
		Size: 3.4 MB (3412169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef3a26713734a58467b349d72f612c355ec15b79c6d1207b1fb850a58d9d3f2`  
		Last Modified: Mon, 28 Apr 2025 20:51:24 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:23a8f97a3085aa7e74e5a0f74873b470d5f76daa6fb5139cd9b079edb7f3a246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057e65b81b970c62625518d3ad949d38147d703b694d9610f06f4dec2eb36d33`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd969451333ff00c3e71b2f2bbc0cd89882a071464074b810b4fa5d666733a57`  
		Last Modified: Wed, 09 Apr 2025 11:40:25 GMT  
		Size: 16.3 MB (16304381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9767a5fc28208c898a3f44d23336651492e4d49e9e5d29f58db6513a70440e`  
		Last Modified: Mon, 28 Apr 2025 20:09:41 GMT  
		Size: 50.1 MB (50117535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4779dc759a7ac1238d5c5168b3b6c926eed64779acbdb636d8b184d8463203dd`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec7ff3fcaa95c9137d9703a73bde8406fb6714bf75e54a311ef94cc0c7631d`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee95286c68db8e309d4de664a4c98d81ef1efcbc77a0e544d61e4f7473278d9`  
		Last Modified: Mon, 28 Apr 2025 21:07:03 GMT  
		Size: 72.9 MB (72930453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:ba883d02ba0fd64fd28d3f211a8344eb99e374ea39503ae7d3edac3f79202c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5118a9b1a3c81f2eeac1eb2a5e3f9139094bed91025e678051b6c2412ef58358`

```dockerfile
```

-	Layers:
	-	`sha256:70067dbdaa21914d6d576b6b92cc15fe05fcb2b676129c204413d1ca6951adcc`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
		Size: 3.4 MB (3415853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82709aaef1300f735bfd8a8315df1edf621a7e983dcbb944c579380c9eaba1db`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
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
$ docker pull orientdb@sha256:24db5b30ba0c2572b80c779f737d9504988e881025e3b114c5b6730e882b6362
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
$ docker pull orientdb@sha256:adf22d112861ee160d7b5e618a5b5949d202d875dc5e459e764bc58b440379db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206266203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ac9e4703d417a4052104c8213c05c21b0563854fd202bfe4a01e190ea0aca5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eba60aec778c09ce30cc92c6c2210559febcff44803d1c91fe4795229d0bdbc`  
		Last Modified: Mon, 28 Apr 2025 20:51:28 GMT  
		Size: 104.9 MB (104855481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd2b997856bf4899244ca49b071335e44fc50a82db69e01efbd8bcd4402ba8`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ab40b28d199d57e90f4565ef632d7598e8b45d7a5ee12396bc79d58164bf483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed21f0c0ef92903580b145f93ee6c1cdebee8d82e63866488c9dac6a97437d`

```dockerfile
```

-	Layers:
	-	`sha256:199543af196905c2accacba12f22c177bcaf2b03e3490b65f8ad63c61a1dde2d`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 3.5 MB (3542825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e230cb71522643557ce5bd54c050e319b8d40913299069057b3ce5b8ff979a9d`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:9737ab788066edcca9c7521ebc69f5cce2ba029285c9efe0a93553b07c8e6700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198118811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1a3de63c5d80165c44c35e80e3a304cfabb3cea562c0b9d73401d70edc4379`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd969451333ff00c3e71b2f2bbc0cd89882a071464074b810b4fa5d666733a57`  
		Last Modified: Wed, 09 Apr 2025 11:40:25 GMT  
		Size: 16.3 MB (16304381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9767a5fc28208c898a3f44d23336651492e4d49e9e5d29f58db6513a70440e`  
		Last Modified: Mon, 28 Apr 2025 20:09:41 GMT  
		Size: 50.1 MB (50117535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4779dc759a7ac1238d5c5168b3b6c926eed64779acbdb636d8b184d8463203dd`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec7ff3fcaa95c9137d9703a73bde8406fb6714bf75e54a311ef94cc0c7631d`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f30065dd527ad90cf093f4c6407d82c7c789fa97f8df2ee895bcfae7fc8c2`  
		Last Modified: Mon, 28 Apr 2025 21:07:57 GMT  
		Size: 104.9 MB (104855496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61127b96813c703f2d9fd8f93775548e70802da34e251a5241d8ca18aec9404`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:369619cb773bab03b3f81c3bbf2403094786cd8b5229f6b29055edaeaa6ec241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3b4dba513ea801ad52079aa48812a76f29e4f2fc62dd0aa0751d885037d20`

```dockerfile
```

-	Layers:
	-	`sha256:9c26e258bc2d21a7fc5703369f368ce369c3116700364ff02a0c33b1b41b3e25`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 3.5 MB (3546501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c55eea6aa393bc8ccaeb5bdeb0d1134d91a96ae384909c6c0f472bbe45243d9`  
		Last Modified: Mon, 28 Apr 2025 21:07:53 GMT  
		Size: 16.9 KB (16917 bytes)  
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
$ docker pull orientdb@sha256:659df4ecc8f78f2a900ccceca990d4359eb084153257521d7f6e6aec1ad962a5
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
$ docker pull orientdb@sha256:b1963106c7da70f7a2c0987b58c49d7e4fd0890bafa7ce91bbb7e53535ab19bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce69a08d5022f414c33c6b0a315622fb8145b5e59a40ca701073ae82494241`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d49df540b80bf37973230f1306c50217b704a7ef5c4f2fed542ce90a086929`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 72.9 MB (72930477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f77a419f7715e6d6c012d4dacdc88c9ee35bedb0ab110633dd494b9f0089415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b9747e6b05a653327b93920e1bb20decf9c7d22ac6af43f6a871e4b6d529ee`

```dockerfile
```

-	Layers:
	-	`sha256:3a582dbb17ba00be07c9c04fa143b924ba0725fe5c3d9991cb9bb179470d7fa1`  
		Last Modified: Mon, 28 Apr 2025 20:51:25 GMT  
		Size: 3.4 MB (3412169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef3a26713734a58467b349d72f612c355ec15b79c6d1207b1fb850a58d9d3f2`  
		Last Modified: Mon, 28 Apr 2025 20:51:24 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:23a8f97a3085aa7e74e5a0f74873b470d5f76daa6fb5139cd9b079edb7f3a246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057e65b81b970c62625518d3ad949d38147d703b694d9610f06f4dec2eb36d33`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd969451333ff00c3e71b2f2bbc0cd89882a071464074b810b4fa5d666733a57`  
		Last Modified: Wed, 09 Apr 2025 11:40:25 GMT  
		Size: 16.3 MB (16304381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9767a5fc28208c898a3f44d23336651492e4d49e9e5d29f58db6513a70440e`  
		Last Modified: Mon, 28 Apr 2025 20:09:41 GMT  
		Size: 50.1 MB (50117535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4779dc759a7ac1238d5c5168b3b6c926eed64779acbdb636d8b184d8463203dd`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec7ff3fcaa95c9137d9703a73bde8406fb6714bf75e54a311ef94cc0c7631d`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee95286c68db8e309d4de664a4c98d81ef1efcbc77a0e544d61e4f7473278d9`  
		Last Modified: Mon, 28 Apr 2025 21:07:03 GMT  
		Size: 72.9 MB (72930453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39` - unknown; unknown

```console
$ docker pull orientdb@sha256:ba883d02ba0fd64fd28d3f211a8344eb99e374ea39503ae7d3edac3f79202c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5118a9b1a3c81f2eeac1eb2a5e3f9139094bed91025e678051b6c2412ef58358`

```dockerfile
```

-	Layers:
	-	`sha256:70067dbdaa21914d6d576b6b92cc15fe05fcb2b676129c204413d1ca6951adcc`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
		Size: 3.4 MB (3415853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82709aaef1300f735bfd8a8315df1edf621a7e983dcbb944c579380c9eaba1db`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
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
$ docker pull orientdb@sha256:24db5b30ba0c2572b80c779f737d9504988e881025e3b114c5b6730e882b6362
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
$ docker pull orientdb@sha256:adf22d112861ee160d7b5e618a5b5949d202d875dc5e459e764bc58b440379db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206266203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ac9e4703d417a4052104c8213c05c21b0563854fd202bfe4a01e190ea0aca5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eba60aec778c09ce30cc92c6c2210559febcff44803d1c91fe4795229d0bdbc`  
		Last Modified: Mon, 28 Apr 2025 20:51:28 GMT  
		Size: 104.9 MB (104855481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd2b997856bf4899244ca49b071335e44fc50a82db69e01efbd8bcd4402ba8`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ab40b28d199d57e90f4565ef632d7598e8b45d7a5ee12396bc79d58164bf483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed21f0c0ef92903580b145f93ee6c1cdebee8d82e63866488c9dac6a97437d`

```dockerfile
```

-	Layers:
	-	`sha256:199543af196905c2accacba12f22c177bcaf2b03e3490b65f8ad63c61a1dde2d`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 3.5 MB (3542825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e230cb71522643557ce5bd54c050e319b8d40913299069057b3ce5b8ff979a9d`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.39-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:9737ab788066edcca9c7521ebc69f5cce2ba029285c9efe0a93553b07c8e6700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198118811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1a3de63c5d80165c44c35e80e3a304cfabb3cea562c0b9d73401d70edc4379`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd969451333ff00c3e71b2f2bbc0cd89882a071464074b810b4fa5d666733a57`  
		Last Modified: Wed, 09 Apr 2025 11:40:25 GMT  
		Size: 16.3 MB (16304381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9767a5fc28208c898a3f44d23336651492e4d49e9e5d29f58db6513a70440e`  
		Last Modified: Mon, 28 Apr 2025 20:09:41 GMT  
		Size: 50.1 MB (50117535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4779dc759a7ac1238d5c5168b3b6c926eed64779acbdb636d8b184d8463203dd`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec7ff3fcaa95c9137d9703a73bde8406fb6714bf75e54a311ef94cc0c7631d`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f30065dd527ad90cf093f4c6407d82c7c789fa97f8df2ee895bcfae7fc8c2`  
		Last Modified: Mon, 28 Apr 2025 21:07:57 GMT  
		Size: 104.9 MB (104855496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61127b96813c703f2d9fd8f93775548e70802da34e251a5241d8ca18aec9404`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.39-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:369619cb773bab03b3f81c3bbf2403094786cd8b5229f6b29055edaeaa6ec241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3b4dba513ea801ad52079aa48812a76f29e4f2fc62dd0aa0751d885037d20`

```dockerfile
```

-	Layers:
	-	`sha256:9c26e258bc2d21a7fc5703369f368ce369c3116700364ff02a0c33b1b41b3e25`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 3.5 MB (3546501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c55eea6aa393bc8ccaeb5bdeb0d1134d91a96ae384909c6c0f472bbe45243d9`  
		Last Modified: Mon, 28 Apr 2025 21:07:53 GMT  
		Size: 16.9 KB (16917 bytes)  
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
$ docker pull orientdb@sha256:659df4ecc8f78f2a900ccceca990d4359eb084153257521d7f6e6aec1ad962a5
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
$ docker pull orientdb@sha256:b1963106c7da70f7a2c0987b58c49d7e4fd0890bafa7ce91bbb7e53535ab19bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174339828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce69a08d5022f414c33c6b0a315622fb8145b5e59a40ca701073ae82494241`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef40b69a6254f064e0ba9d2e55a77de5fd5ab646d98cd8ee5c036c0b2531800`  
		Last Modified: Mon, 28 Apr 2025 20:07:52 GMT  
		Size: 17.0 MB (16967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03146b78ab538477cf7ea4e619db6d39e9bb852e0c3192dd5f72aa6d85b62a71`  
		Last Modified: Mon, 28 Apr 2025 20:07:53 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e608bcfbe424c0ac644b7b32b78cded6294e7d61adb5c5ecb48671bfc1d6d12d`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Mon, 28 Apr 2025 20:07:51 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d49df540b80bf37973230f1306c50217b704a7ef5c4f2fed542ce90a086929`  
		Last Modified: Mon, 28 Apr 2025 20:51:26 GMT  
		Size: 72.9 MB (72930477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:7f77a419f7715e6d6c012d4dacdc88c9ee35bedb0ab110633dd494b9f0089415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b9747e6b05a653327b93920e1bb20decf9c7d22ac6af43f6a871e4b6d529ee`

```dockerfile
```

-	Layers:
	-	`sha256:3a582dbb17ba00be07c9c04fa143b924ba0725fe5c3d9991cb9bb179470d7fa1`  
		Last Modified: Mon, 28 Apr 2025 20:51:25 GMT  
		Size: 3.4 MB (3412169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef3a26713734a58467b349d72f612c355ec15b79c6d1207b1fb850a58d9d3f2`  
		Last Modified: Mon, 28 Apr 2025 20:51:24 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:23a8f97a3085aa7e74e5a0f74873b470d5f76daa6fb5139cd9b079edb7f3a246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057e65b81b970c62625518d3ad949d38147d703b694d9610f06f4dec2eb36d33`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd969451333ff00c3e71b2f2bbc0cd89882a071464074b810b4fa5d666733a57`  
		Last Modified: Wed, 09 Apr 2025 11:40:25 GMT  
		Size: 16.3 MB (16304381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9767a5fc28208c898a3f44d23336651492e4d49e9e5d29f58db6513a70440e`  
		Last Modified: Mon, 28 Apr 2025 20:09:41 GMT  
		Size: 50.1 MB (50117535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4779dc759a7ac1238d5c5168b3b6c926eed64779acbdb636d8b184d8463203dd`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec7ff3fcaa95c9137d9703a73bde8406fb6714bf75e54a311ef94cc0c7631d`  
		Last Modified: Mon, 28 Apr 2025 20:09:39 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee95286c68db8e309d4de664a4c98d81ef1efcbc77a0e544d61e4f7473278d9`  
		Last Modified: Mon, 28 Apr 2025 21:07:03 GMT  
		Size: 72.9 MB (72930453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:ba883d02ba0fd64fd28d3f211a8344eb99e374ea39503ae7d3edac3f79202c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5118a9b1a3c81f2eeac1eb2a5e3f9139094bed91025e678051b6c2412ef58358`

```dockerfile
```

-	Layers:
	-	`sha256:70067dbdaa21914d6d576b6b92cc15fe05fcb2b676129c204413d1ca6951adcc`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
		Size: 3.4 MB (3415853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82709aaef1300f735bfd8a8315df1edf621a7e983dcbb944c579380c9eaba1db`  
		Last Modified: Mon, 28 Apr 2025 21:07:01 GMT  
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
