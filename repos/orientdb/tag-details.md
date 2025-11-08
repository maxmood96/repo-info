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
$ docker pull orientdb@sha256:0fbcf0dc3c85b50f06d3ce91040a61d663f61c87eefd14213ba3d1eb0b6db1d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:09be357b75678fbf699a0f37ca535b2273eefa7d03e60ab88bb7a56f098ad672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154521687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9801999034672d0f86ce261cbd2ed72575089b3e0c763bd74c43ab42488b51e6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Sat, 08 Nov 2025 18:03:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:18 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:18 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:18 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f952c75e6b83a2c2fa3164bde18fd47ce398ec4ab038f4fc565ab5710d52c`  
		Last Modified: Sat, 08 Nov 2025 18:03:37 GMT  
		Size: 53.1 MB (53081026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:91165d57ae1219f91cde5df12cae8fad3b20eb16204e4fa8772ad445dca8597d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cde6a496039c97f738f09dbfdd24c0f088611763c05aa896b09518940f8b9`

```dockerfile
```

-	Layers:
	-	`sha256:38fa8986950909b6c3ba9e3f2427d2e623b4822e190248f950d7190ea6599e02`  
		Last Modified: Sat, 08 Nov 2025 19:40:23 GMT  
		Size: 3.6 MB (3571130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8933513a855137051f26ba792bda411f48fd1411d856ad686ba77dc778b509`  
		Last Modified: Sat, 08 Nov 2025 19:40:24 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:9e8d63ee50ff9058808fef866a0800fbd343abf0b5d75203e4a619681b572924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:c28a27afc9e23792a86ee279f5493407bff63cc07b1eeb874c904c62525bc3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177528687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef08ff4d478ec1723792eba4e79bd99a7d8d72b1bd338b5f3c1b697f9c18485`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:23 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:23 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Sat, 08 Nov 2025 18:03:23 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:26 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:26 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd52b421ad531b37325cd3c34db73888e2d9471d99236cb4dfb010e725ddff`  
		Last Modified: Sat, 08 Nov 2025 18:03:52 GMT  
		Size: 76.1 MB (76086651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836d48fc7f613e5fdf53c916f340ec4a8cd42318f713fe402dac712a3c6f6bc8`  
		Last Modified: Sat, 08 Nov 2025 18:03:49 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ce610aaab09efd3ba45dfbdc74512f91e0051c264f9327ded0f57ef6582e24c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3651824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5b343b42db3edf0067ec4d7eed0dde164442fabff34eca0f54839a3c0f32b9`

```dockerfile
```

-	Layers:
	-	`sha256:32eefac7d526d5a6d5e172bcae41e42f5a3b70fe829811c0a844a9fc1762f361`  
		Last Modified: Sat, 08 Nov 2025 19:40:29 GMT  
		Size: 3.6 MB (3635024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0debe62e7eb618fee5e1c735bea68cce6532939d7fd33639d5d93c932856533b`  
		Last Modified: Sat, 08 Nov 2025 19:40:29 GMT  
		Size: 16.8 KB (16800 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:0fbcf0dc3c85b50f06d3ce91040a61d663f61c87eefd14213ba3d1eb0b6db1d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:09be357b75678fbf699a0f37ca535b2273eefa7d03e60ab88bb7a56f098ad672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154521687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9801999034672d0f86ce261cbd2ed72575089b3e0c763bd74c43ab42488b51e6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Sat, 08 Nov 2025 18:03:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Sat, 08 Nov 2025 18:03:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:18 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:18 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:18 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f952c75e6b83a2c2fa3164bde18fd47ce398ec4ab038f4fc565ab5710d52c`  
		Last Modified: Sat, 08 Nov 2025 18:03:37 GMT  
		Size: 53.1 MB (53081026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:91165d57ae1219f91cde5df12cae8fad3b20eb16204e4fa8772ad445dca8597d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cde6a496039c97f738f09dbfdd24c0f088611763c05aa896b09518940f8b9`

```dockerfile
```

-	Layers:
	-	`sha256:38fa8986950909b6c3ba9e3f2427d2e623b4822e190248f950d7190ea6599e02`  
		Last Modified: Sat, 08 Nov 2025 19:40:23 GMT  
		Size: 3.6 MB (3571130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8933513a855137051f26ba792bda411f48fd1411d856ad686ba77dc778b509`  
		Last Modified: Sat, 08 Nov 2025 19:40:24 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:9e8d63ee50ff9058808fef866a0800fbd343abf0b5d75203e4a619681b572924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:c28a27afc9e23792a86ee279f5493407bff63cc07b1eeb874c904c62525bc3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177528687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef08ff4d478ec1723792eba4e79bd99a7d8d72b1bd338b5f3c1b697f9c18485`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:23 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:23 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Sat, 08 Nov 2025 18:03:23 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Sat, 08 Nov 2025 18:03:23 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:26 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:26 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:03:26 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd52b421ad531b37325cd3c34db73888e2d9471d99236cb4dfb010e725ddff`  
		Last Modified: Sat, 08 Nov 2025 18:03:52 GMT  
		Size: 76.1 MB (76086651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836d48fc7f613e5fdf53c916f340ec4a8cd42318f713fe402dac712a3c6f6bc8`  
		Last Modified: Sat, 08 Nov 2025 18:03:49 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ce610aaab09efd3ba45dfbdc74512f91e0051c264f9327ded0f57ef6582e24c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3651824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5b343b42db3edf0067ec4d7eed0dde164442fabff34eca0f54839a3c0f32b9`

```dockerfile
```

-	Layers:
	-	`sha256:32eefac7d526d5a6d5e172bcae41e42f5a3b70fe829811c0a844a9fc1762f361`  
		Last Modified: Sat, 08 Nov 2025 19:40:29 GMT  
		Size: 3.6 MB (3635024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0debe62e7eb618fee5e1c735bea68cce6532939d7fd33639d5d93c932856533b`  
		Last Modified: Sat, 08 Nov 2025 19:40:29 GMT  
		Size: 16.8 KB (16800 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:b6ef85869b2e749978dbe48d17d7520f3cf7a34cbbabe7d40e6f8ff64f7e864d
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
$ docker pull orientdb@sha256:efdf40ebff316d9f5075b961b687719e0fe997fb97e88f6372d663b2caf0fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174377311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b369dfa8bf7bcd712dcda175d4c752872634a06bdcac42f82636805ea7da264b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:19 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:19 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:03:19 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:21 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14d78f49489a096ad7b3071bd1d4df04957ad5db1161d665bff2906f1e73960`  
		Last Modified: Sat, 08 Nov 2025 18:03:44 GMT  
		Size: 72.9 MB (72936650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:315ba55467048636517fc16160a0f2e5f5431a0f9d1c712fe0434f6cec1fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1545eaad3ddce932bfb2afabeae6a0037e7d5ece54d4f961147686100f3fa21`

```dockerfile
```

-	Layers:
	-	`sha256:5ed09740bcf7641f829977bbe7f95cdabb296b5e547c4628d147bb88181a4a2c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be721401b8cc018a706746f540c6ac0e501b93e249b050f6d02fd0eb835b00c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c4827f4576d6e5f5758ea4c8e6a9729ac96771c0ac60148a7a3518b5c13f80f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166242544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41645e27e3df1c37dd6b54671e9c0fd18144334b9a87508399d91aa1bf99e668`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:00:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:00:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:00:33 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396d961aab76153613bd3e8d4a9d48d07e63d43e60060e513175559495c4b8a`  
		Last Modified: Sat, 08 Nov 2025 18:00:58 GMT  
		Size: 72.9 MB (72936614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:d068967c8ee8c913913ca139431def705e82418ab123acea3b3088030cb2af6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b7265a1abda657ec9085db629deb6427887bb2f479d4d25aa21e9b92efbc47`

```dockerfile
```

-	Layers:
	-	`sha256:81dd3a23eb5d3b9f4dbc9954eed6aceb22d312bbb072e67bed856ae77ff9ffca`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6258dc928b70847ba4149f38a8f1ec082e36ebc359b0ed518c935c5ae7b3cfcd`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:6f844b72ab525012a9607d6af4454e82ce22e022370ad9afab19bc740eb71268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172609414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c8628909a25e581c76892191e4ed024ddec99b04d4438483e48c5d3625203a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:02:28 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:02:28 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:02:28 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:02:30 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1819f17fa3903f9c8008e9962cf5ec098b9afde1c77ac9b37521a4971e930a4`  
		Last Modified: Sat, 08 Nov 2025 18:03:17 GMT  
		Size: 72.9 MB (72936645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:9af456df111bdd65e89a92870cd129f8b5dcd1821fdf921bfc44166803153822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3b3475724547c863f5fa9b9364622ca0155dce5d63a74237def0c5e32cd39`

```dockerfile
```

-	Layers:
	-	`sha256:ad6505896af882f5b06c09040b04018c44ebf2dd2be6359bc9325694f2de8af3`  
		Last Modified: Sat, 08 Nov 2025 19:40:54 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8b1eefafd2c3e14e5c349cca3032e8263e1b7adca057144598400c0a3a4728`  
		Last Modified: Sat, 08 Nov 2025 19:40:55 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:a1bdd44d775a19ec759bbe984010d4d121adcfb757fd3fef7f7c650b68a5144d
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
$ docker pull orientdb@sha256:8978df5f98b69ae903b81820f2ae457eb6cdd90ce5240945b76c70e2a159725f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206312512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274e68f8ad3e03684260f7561d49845a05fbd3d05586d66534a274b4d37a133`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:03:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:20 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1560d8d4642a4c022a2368c308617ca1d64572fbfc3ed0995442a3c8d27819`  
		Last Modified: Sat, 08 Nov 2025 18:03:57 GMT  
		Size: 104.9 MB (104870484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdfc51be3003cdd877473fa881cc8fcda8202e91d348b42f2e7999f0fcb7fef`  
		Last Modified: Sat, 08 Nov 2025 18:03:40 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:f2ed7baa277d0a8954fa1a6da2be4b56e639277ad41cac1d11f59515e5e4226b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe35ab658caaa27ec497b11b4c4758d3294ed553c5936c6ad41e68d97298bb9d`

```dockerfile
```

-	Layers:
	-	`sha256:b55146130c3431bab786a6ca9054c7ed3d868fecf165ce0f643682d804b2dd22`  
		Last Modified: Sat, 08 Nov 2025 19:40:54 GMT  
		Size: 3.7 MB (3715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0010111bfacd189337d16e8a43a907cd510e626ba99ac523cc91b994f1f11ce`  
		Last Modified: Sat, 08 Nov 2025 19:40:55 GMT  
		Size: 16.8 KB (16802 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:0a80496562a5f7440d94e84c1a275811bafeffb0d32a029dbebad61a7cecd4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198177719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbe1f97455b3c1a9241742caf568585e26e1da8d80c3c778c17dc828856ffaa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:00:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:00:44 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:00:49 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c8234980f81eb2a4ea00efbdb0455b7a8a268c483d32c5054aee96cecb87f8`  
		Last Modified: Sat, 08 Nov 2025 18:01:19 GMT  
		Size: 104.9 MB (104870419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8bb555ea1a2bece56624a801c2b5431a660fa5f8fb039dae393a71f7dc017`  
		Last Modified: Sat, 08 Nov 2025 18:01:10 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:d71465b76fb31b82f445a4b1fb6503d25c65533f6bbb2cf1c07970ea7609e22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08500984fa797e69659a8bad24150dedde478c752ebd082c55b226a7b31ee6f4`

```dockerfile
```

-	Layers:
	-	`sha256:1e6f0dd0781e87d8fecbb4e8d940433a9cb1040f665969fea45d0ad398eddb33`  
		Last Modified: Sat, 08 Nov 2025 19:40:58 GMT  
		Size: 3.7 MB (3719126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93db22d801d2f2a7963de07e094c70e28e227df0899575581479f5f961f3206f`  
		Last Modified: Sat, 08 Nov 2025 19:40:59 GMT  
		Size: 16.9 KB (16880 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:dd89e54197ff8b5e466cc581216f28442d29cf1c84cc48e56512c8db23ee9abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204544578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1686367eb39f062b2ae605ce9766c1a53ce6fdb5b7c235f438c87db25f6298f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:02:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:02:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:02:31 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:34 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:02:34 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5ddceafb14a2b47442dd450fa9047a22e488690c69847b6615d44851b19d4`  
		Last Modified: Sat, 08 Nov 2025 18:02:50 GMT  
		Size: 104.9 MB (104870439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dce675483edd1112ebfc91f96ac78281d720e3fd81aa51536e4cc16401b8408`  
		Last Modified: Sat, 08 Nov 2025 18:02:58 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:19657ec5bd9057a2d92015bd1cf2b0b5fcf94c94c274de188b1715d3d9d145bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1ea971762f063f55ad4eddc05f11ed1ba6d34af82b5d75ce7d196a3c15b406`

```dockerfile
```

-	Layers:
	-	`sha256:f3d061aab9878c0c6d88cc745162d42d89548d2fe621a2fbea33184611ff998f`  
		Last Modified: Sat, 08 Nov 2025 19:41:03 GMT  
		Size: 3.7 MB (3716305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdc7ad704b88a4973439f36ac150f8685e42a4c1f62e115dd4ac00ecacfeb3b`  
		Last Modified: Sat, 08 Nov 2025 19:41:04 GMT  
		Size: 16.9 KB (16898 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.45`

```console
$ docker pull orientdb@sha256:b6ef85869b2e749978dbe48d17d7520f3cf7a34cbbabe7d40e6f8ff64f7e864d
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
$ docker pull orientdb@sha256:efdf40ebff316d9f5075b961b687719e0fe997fb97e88f6372d663b2caf0fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174377311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b369dfa8bf7bcd712dcda175d4c752872634a06bdcac42f82636805ea7da264b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:19 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:19 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:03:19 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:21 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14d78f49489a096ad7b3071bd1d4df04957ad5db1161d665bff2906f1e73960`  
		Last Modified: Sat, 08 Nov 2025 18:03:44 GMT  
		Size: 72.9 MB (72936650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:315ba55467048636517fc16160a0f2e5f5431a0f9d1c712fe0434f6cec1fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1545eaad3ddce932bfb2afabeae6a0037e7d5ece54d4f961147686100f3fa21`

```dockerfile
```

-	Layers:
	-	`sha256:5ed09740bcf7641f829977bbe7f95cdabb296b5e547c4628d147bb88181a4a2c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be721401b8cc018a706746f540c6ac0e501b93e249b050f6d02fd0eb835b00c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c4827f4576d6e5f5758ea4c8e6a9729ac96771c0ac60148a7a3518b5c13f80f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166242544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41645e27e3df1c37dd6b54671e9c0fd18144334b9a87508399d91aa1bf99e668`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:00:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:00:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:00:33 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396d961aab76153613bd3e8d4a9d48d07e63d43e60060e513175559495c4b8a`  
		Last Modified: Sat, 08 Nov 2025 18:00:58 GMT  
		Size: 72.9 MB (72936614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:d068967c8ee8c913913ca139431def705e82418ab123acea3b3088030cb2af6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b7265a1abda657ec9085db629deb6427887bb2f479d4d25aa21e9b92efbc47`

```dockerfile
```

-	Layers:
	-	`sha256:81dd3a23eb5d3b9f4dbc9954eed6aceb22d312bbb072e67bed856ae77ff9ffca`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6258dc928b70847ba4149f38a8f1ec082e36ebc359b0ed518c935c5ae7b3cfcd`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:6f844b72ab525012a9607d6af4454e82ce22e022370ad9afab19bc740eb71268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172609414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c8628909a25e581c76892191e4ed024ddec99b04d4438483e48c5d3625203a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:02:28 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:02:28 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:02:28 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:02:30 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1819f17fa3903f9c8008e9962cf5ec098b9afde1c77ac9b37521a4971e930a4`  
		Last Modified: Sat, 08 Nov 2025 18:03:17 GMT  
		Size: 72.9 MB (72936645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45` - unknown; unknown

```console
$ docker pull orientdb@sha256:9af456df111bdd65e89a92870cd129f8b5dcd1821fdf921bfc44166803153822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3b3475724547c863f5fa9b9364622ca0155dce5d63a74237def0c5e32cd39`

```dockerfile
```

-	Layers:
	-	`sha256:ad6505896af882f5b06c09040b04018c44ebf2dd2be6359bc9325694f2de8af3`  
		Last Modified: Sat, 08 Nov 2025 19:40:54 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8b1eefafd2c3e14e5c349cca3032e8263e1b7adca057144598400c0a3a4728`  
		Last Modified: Sat, 08 Nov 2025 19:40:55 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.45-tp3`

```console
$ docker pull orientdb@sha256:a1bdd44d775a19ec759bbe984010d4d121adcfb757fd3fef7f7c650b68a5144d
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
$ docker pull orientdb@sha256:8978df5f98b69ae903b81820f2ae457eb6cdd90ce5240945b76c70e2a159725f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206312512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274e68f8ad3e03684260f7561d49845a05fbd3d05586d66534a274b4d37a133`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:18 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:18 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:03:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:03:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:20 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:03:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1560d8d4642a4c022a2368c308617ca1d64572fbfc3ed0995442a3c8d27819`  
		Last Modified: Sat, 08 Nov 2025 18:03:57 GMT  
		Size: 104.9 MB (104870484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdfc51be3003cdd877473fa881cc8fcda8202e91d348b42f2e7999f0fcb7fef`  
		Last Modified: Sat, 08 Nov 2025 18:03:40 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:f2ed7baa277d0a8954fa1a6da2be4b56e639277ad41cac1d11f59515e5e4226b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe35ab658caaa27ec497b11b4c4758d3294ed553c5936c6ad41e68d97298bb9d`

```dockerfile
```

-	Layers:
	-	`sha256:b55146130c3431bab786a6ca9054c7ed3d868fecf165ce0f643682d804b2dd22`  
		Last Modified: Sat, 08 Nov 2025 19:40:54 GMT  
		Size: 3.7 MB (3715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0010111bfacd189337d16e8a43a907cd510e626ba99ac523cc91b994f1f11ce`  
		Last Modified: Sat, 08 Nov 2025 19:40:55 GMT  
		Size: 16.8 KB (16802 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:0a80496562a5f7440d94e84c1a275811bafeffb0d32a029dbebad61a7cecd4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198177719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbe1f97455b3c1a9241742caf568585e26e1da8d80c3c778c17dc828856ffaa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:00:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:00:44 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:00:44 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:00:49 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:00:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c8234980f81eb2a4ea00efbdb0455b7a8a268c483d32c5054aee96cecb87f8`  
		Last Modified: Sat, 08 Nov 2025 18:01:19 GMT  
		Size: 104.9 MB (104870419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a8bb555ea1a2bece56624a801c2b5431a660fa5f8fb039dae393a71f7dc017`  
		Last Modified: Sat, 08 Nov 2025 18:01:10 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:d71465b76fb31b82f445a4b1fb6503d25c65533f6bbb2cf1c07970ea7609e22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08500984fa797e69659a8bad24150dedde478c752ebd082c55b226a7b31ee6f4`

```dockerfile
```

-	Layers:
	-	`sha256:1e6f0dd0781e87d8fecbb4e8d940433a9cb1040f665969fea45d0ad398eddb33`  
		Last Modified: Sat, 08 Nov 2025 19:40:58 GMT  
		Size: 3.7 MB (3719126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93db22d801d2f2a7963de07e094c70e28e227df0899575581479f5f961f3206f`  
		Last Modified: Sat, 08 Nov 2025 19:40:59 GMT  
		Size: 16.9 KB (16880 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.45-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:dd89e54197ff8b5e466cc581216f28442d29cf1c84cc48e56512c8db23ee9abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204544578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1686367eb39f062b2ae605ce9766c1a53ce6fdb5b7c235f438c87db25f6298f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:02:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:02:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=deb1f4358b88e685e4e703f53e03948d
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ad6fe4934b35829eeb650e2f8d0bf0592e7ec83a
# Sat, 08 Nov 2025 18:02:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.45/orientdb-tp3-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:02:31 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Sat, 08 Nov 2025 18:02:34 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:34 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:02:34 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
EXPOSE map[8182/tcp:{}]
# Sat, 08 Nov 2025 18:02:34 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5ddceafb14a2b47442dd450fa9047a22e488690c69847b6615d44851b19d4`  
		Last Modified: Sat, 08 Nov 2025 18:02:50 GMT  
		Size: 104.9 MB (104870439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dce675483edd1112ebfc91f96ac78281d720e3fd81aa51536e4cc16401b8408`  
		Last Modified: Sat, 08 Nov 2025 18:02:58 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.45-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:19657ec5bd9057a2d92015bd1cf2b0b5fcf94c94c274de188b1715d3d9d145bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1ea971762f063f55ad4eddc05f11ed1ba6d34af82b5d75ce7d196a3c15b406`

```dockerfile
```

-	Layers:
	-	`sha256:f3d061aab9878c0c6d88cc745162d42d89548d2fe621a2fbea33184611ff998f`  
		Last Modified: Sat, 08 Nov 2025 19:41:03 GMT  
		Size: 3.7 MB (3716305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdc7ad704b88a4973439f36ac150f8685e42a4c1f62e115dd4ac00ecacfeb3b`  
		Last Modified: Sat, 08 Nov 2025 19:41:04 GMT  
		Size: 16.9 KB (16898 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:b6ef85869b2e749978dbe48d17d7520f3cf7a34cbbabe7d40e6f8ff64f7e864d
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
$ docker pull orientdb@sha256:efdf40ebff316d9f5075b961b687719e0fe997fb97e88f6372d663b2caf0fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174377311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b369dfa8bf7bcd712dcda175d4c752872634a06bdcac42f82636805ea7da264b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:19 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:03:19 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:03:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:03:19 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:03:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:03:21 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:03:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14d78f49489a096ad7b3071bd1d4df04957ad5db1161d665bff2906f1e73960`  
		Last Modified: Sat, 08 Nov 2025 18:03:44 GMT  
		Size: 72.9 MB (72936650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:315ba55467048636517fc16160a0f2e5f5431a0f9d1c712fe0434f6cec1fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1545eaad3ddce932bfb2afabeae6a0037e7d5ece54d4f961147686100f3fa21`

```dockerfile
```

-	Layers:
	-	`sha256:5ed09740bcf7641f829977bbe7f95cdabb296b5e547c4628d147bb88181a4a2c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 3.6 MB (3579595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be721401b8cc018a706746f540c6ac0e501b93e249b050f6d02fd0eb835b00c`  
		Last Modified: Sat, 08 Nov 2025 19:40:44 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c4827f4576d6e5f5758ea4c8e6a9729ac96771c0ac60148a7a3518b5c13f80f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166242544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41645e27e3df1c37dd6b54671e9c0fd18144334b9a87508399d91aa1bf99e668`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:30 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:00:30 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:00:30 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:00:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:00:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:00:33 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:00:33 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396d961aab76153613bd3e8d4a9d48d07e63d43e60060e513175559495c4b8a`  
		Last Modified: Sat, 08 Nov 2025 18:00:58 GMT  
		Size: 72.9 MB (72936614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:d068967c8ee8c913913ca139431def705e82418ab123acea3b3088030cb2af6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b7265a1abda657ec9085db629deb6427887bb2f479d4d25aa21e9b92efbc47`

```dockerfile
```

-	Layers:
	-	`sha256:81dd3a23eb5d3b9f4dbc9954eed6aceb22d312bbb072e67bed856ae77ff9ffca`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 3.6 MB (3583569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6258dc928b70847ba4149f38a8f1ec082e36ebc359b0ed518c935c5ae7b3cfcd`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:6f844b72ab525012a9607d6af4454e82ce22e022370ad9afab19bc740eb71268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172609414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c8628909a25e581c76892191e4ed024ddec99b04d4438483e48c5d3625203a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:02:28 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 08 Nov 2025 18:02:28 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_VERSION=3.2.45
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=d81bb8d81eb0a9dd9a9017d4cd4ecf92
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eacbe7a972c21e00223432dba11a61634af6c09a
# Sat, 08 Nov 2025 18:02:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.45/orientdb-community-3.2.45.tar.gz
# Sat, 08 Nov 2025 18:02:28 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Sat, 08 Nov 2025 18:02:30 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:30 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 08 Nov 2025 18:02:30 GMT
WORKDIR /orientdb
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2424/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
EXPOSE map[2480/tcp:{}]
# Sat, 08 Nov 2025 18:02:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1819f17fa3903f9c8008e9962cf5ec098b9afde1c77ac9b37521a4971e930a4`  
		Last Modified: Sat, 08 Nov 2025 18:03:17 GMT  
		Size: 72.9 MB (72936645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:9af456df111bdd65e89a92870cd129f8b5dcd1821fdf921bfc44166803153822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3b3475724547c863f5fa9b9364622ca0155dce5d63a74237def0c5e32cd39`

```dockerfile
```

-	Layers:
	-	`sha256:ad6505896af882f5b06c09040b04018c44ebf2dd2be6359bc9325694f2de8af3`  
		Last Modified: Sat, 08 Nov 2025 19:40:54 GMT  
		Size: 3.6 MB (3580752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8b1eefafd2c3e14e5c349cca3032e8263e1b7adca057144598400c0a3a4728`  
		Last Modified: Sat, 08 Nov 2025 19:40:55 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json
