<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.51`](#orientdb3251)
-	[`orientdb:3.2.51-tp3`](#orientdb3251-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:8386a248163a1eab8751cd88d6eb3b8a22fdfc5fae0d9a90d63b5bda26aa2f55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:969853b32c9c73fa9fca69a0988c717240f3d3b551de3b87f31cced0c5c2537f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154973595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a5688500d563f91cd35b00c8fa2f63dbd28f01afa402e9ee3e2b7cb76a0516`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:02:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:02:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_VERSION=3.1.20
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Tue, 07 Apr 2026 03:02:03 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:06 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:06 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:06 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:06 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:06 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744b249cada6b401f9719dc4ad55562628851e8aed1228ebe67403aaff03c42d`  
		Last Modified: Tue, 07 Apr 2026 03:02:17 GMT  
		Size: 53.1 MB (53081035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:9e13004e308961dffc1b3b8dbbe777177126a5096d9040d2976818387dd6edc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57039c80af605572bac726c4c4b0ba9e07c4006fa0d988e8cecb12b30200e15`

```dockerfile
```

-	Layers:
	-	`sha256:eb80ba3c84a094bcfca64dd7605eb5726b57d872a882201aac66eb55e90cf747`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 3.6 MB (3571813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50c266c6ab63f26ffb9371121fd24a883f25c195c40bca94e263c6ee248669f`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 14.2 KB (14168 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:ab757c7137a80a767f332de66b82c87bfaff365a7739cc14b71bff7237514f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:dfe1856efcc5a2de956626c1e69c04483786810812c2dd53e8fcdd508f215d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177980617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c10c521a548b5ea85bd072e732545972c17ab954e36df4108df9d2b8323189`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:02:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:02:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Tue, 07 Apr 2026 03:02:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:18 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85279396dbb8d8631b56525220f7e4a266e871e602fd31fd5b932a7d1865b03`  
		Last Modified: Tue, 07 Apr 2026 03:02:29 GMT  
		Size: 76.1 MB (76086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4626f0d4395e06f542ab1ac66fc4e4174ecf1b9ff300b1186bc62286509f93`  
		Last Modified: Tue, 07 Apr 2026 03:02:27 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ea05aaba8697841c26307944d233e9be65a0bc9bc35dc2d18568763a130517e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a09d2dee40b8841db8d7aef3fe1de6e0ac9921c320810fb4de8a78a20c9af0`

```dockerfile
```

-	Layers:
	-	`sha256:a5b8704ac5a0678a4c09c86e78faf7e8541a7e5c9339a098bf6c4bfb7d60003c`  
		Last Modified: Tue, 07 Apr 2026 03:02:28 GMT  
		Size: 3.6 MB (3635707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0ad2e1b0f27d016e572cd00c2a318eab72279d742c84eb691bf918875d1cb4`  
		Last Modified: Tue, 07 Apr 2026 03:02:27 GMT  
		Size: 16.8 KB (16800 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:8386a248163a1eab8751cd88d6eb3b8a22fdfc5fae0d9a90d63b5bda26aa2f55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:969853b32c9c73fa9fca69a0988c717240f3d3b551de3b87f31cced0c5c2537f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154973595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a5688500d563f91cd35b00c8fa2f63dbd28f01afa402e9ee3e2b7cb76a0516`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:02:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:02:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_VERSION=3.1.20
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Tue, 07 Apr 2026 03:02:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Tue, 07 Apr 2026 03:02:03 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:06 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:06 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:06 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:06 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:06 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744b249cada6b401f9719dc4ad55562628851e8aed1228ebe67403aaff03c42d`  
		Last Modified: Tue, 07 Apr 2026 03:02:17 GMT  
		Size: 53.1 MB (53081035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:9e13004e308961dffc1b3b8dbbe777177126a5096d9040d2976818387dd6edc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57039c80af605572bac726c4c4b0ba9e07c4006fa0d988e8cecb12b30200e15`

```dockerfile
```

-	Layers:
	-	`sha256:eb80ba3c84a094bcfca64dd7605eb5726b57d872a882201aac66eb55e90cf747`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 3.6 MB (3571813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50c266c6ab63f26ffb9371121fd24a883f25c195c40bca94e263c6ee248669f`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 14.2 KB (14168 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:ab757c7137a80a767f332de66b82c87bfaff365a7739cc14b71bff7237514f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:dfe1856efcc5a2de956626c1e69c04483786810812c2dd53e8fcdd508f215d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177980617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c10c521a548b5ea85bd072e732545972c17ab954e36df4108df9d2b8323189`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:02:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:02:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_VERSION=3.1.20
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Tue, 07 Apr 2026 03:02:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Tue, 07 Apr 2026 03:02:16 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:02:18 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:18 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:18 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:02:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85279396dbb8d8631b56525220f7e4a266e871e602fd31fd5b932a7d1865b03`  
		Last Modified: Tue, 07 Apr 2026 03:02:29 GMT  
		Size: 76.1 MB (76086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4626f0d4395e06f542ab1ac66fc4e4174ecf1b9ff300b1186bc62286509f93`  
		Last Modified: Tue, 07 Apr 2026 03:02:27 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:ea05aaba8697841c26307944d233e9be65a0bc9bc35dc2d18568763a130517e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a09d2dee40b8841db8d7aef3fe1de6e0ac9921c320810fb4de8a78a20c9af0`

```dockerfile
```

-	Layers:
	-	`sha256:a5b8704ac5a0678a4c09c86e78faf7e8541a7e5c9339a098bf6c4bfb7d60003c`  
		Last Modified: Tue, 07 Apr 2026 03:02:28 GMT  
		Size: 3.6 MB (3635707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0ad2e1b0f27d016e572cd00c2a318eab72279d742c84eb691bf918875d1cb4`  
		Last Modified: Tue, 07 Apr 2026 03:02:27 GMT  
		Size: 16.8 KB (16800 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:f41e201b7657aa9f79485affb819a8a1dab4581840907679a89b6deee77b13da
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
$ docker pull orientdb@sha256:9b5a8f075279bafa40be9724d2d30ff4fcde68cb7c780fd9a349aa59e2e05740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175740656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f8d6418699d3e8296ccbd4e04405c3c3abfca4aba575fdbaed700cbde63d27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:01:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:01:49 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:01:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:01:51 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8165adebcf18a8048f4737df4900e82297c31dda6bbe10db90c8e131d6fd45`  
		Last Modified: Tue, 07 Apr 2026 03:02:05 GMT  
		Size: 73.8 MB (73848096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:8f0e5b71d77c909d7d713c07768809a191d27b8fe85b63cbd2e8ab3d1d1743e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c04a245d0d5cf7b3e46ce5b84eda53ff936d25c133897a521c6dfbf0cac0047`

```dockerfile
```

-	Layers:
	-	`sha256:97cbfd97db3b13d9949d0bf026fd93265133345d009844951bd930cce6c4ed84`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 3.6 MB (3580298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefc653cc84f2fc95d77c6760ac5312004dffc9258e33ab828219a4d0bda0004`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:0227ade03beb308cbe4137a721804fb498968abe09b198f8e38941ee10e07f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167552951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f530b317585be7e9bfacd41dcec7176b7e3a193f605fa5c9ad07615c89d451`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:36 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 04:03:36 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 04:03:36 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:03:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 04:03:38 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0f5e732f93f7f6f2ba4945f1cd0a6daf9792f4e3db0ca15326eaa086c9772`  
		Last Modified: Tue, 07 Apr 2026 04:03:51 GMT  
		Size: 73.8 MB (73848126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:fdba055340baaa5579fa6fe2d8cab6addb3ddeab7ea0c85a3b3b42eae76d7744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d00dee6643c4798eb804b6e05e5d1701b3373df87b5807f8783fe3302e686c3`

```dockerfile
```

-	Layers:
	-	`sha256:434d7b3101c9db94b62c4b041044bfbc90949586505d8d94dd8b16ee9884c2b6`  
		Last Modified: Tue, 07 Apr 2026 04:03:50 GMT  
		Size: 3.6 MB (3584278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b3da82ad3466a1e1b08383452326481ce036145a23ddd6a99d496e7b23294a`  
		Last Modified: Tue, 07 Apr 2026 04:03:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:265fab891b04d9150b5fb331508e399e6fea7fc714634e621daefe1f6d6c43fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (173981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c9f0ea8d995bf76556dcdc34de10250efc16eda302702704a0cfc2520aa9b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:14:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:14:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:14:44 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:14:46 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1b18df539adc7bb391c7f271270d3dcc63a9beb172a09f4cfc27f732cf2ed`  
		Last Modified: Tue, 07 Apr 2026 03:15:00 GMT  
		Size: 73.8 MB (73848125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:83d2290a8e6c1cc6dce80567c67fdcfcd50fc4f99c049ff25b4c3a1e4e296f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f56622e1667d86f982e8ce7abb2a879b2d2a82f606d8541b477c6dbde3f1b4`

```dockerfile
```

-	Layers:
	-	`sha256:d37572cbcb89e0b18d90613e005b67ab29f0de7ca0be831574d4fcd0f9621491`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 3.6 MB (3581457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c4ee6a92d3d0c5b24bdf2e6942abad8d7188dca63577bdaca99a09072a077b`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:0cef004680bb5fff65c8761139517dcd5fb6e3bf5ace795cded27cdce31d36a8
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
$ docker pull orientdb@sha256:27727cd95a37d4d6c640644a79ff80c7a05036bb33a921c0e6ac6a3977de0092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207674929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df95100abc660898fc55d1feb0729e05d899a7d2b09a5e627f2418393a7d054d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:58 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:01:58 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:01:58 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:01 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f0a458143238b524553a3b4415e79243a4855da69be69f6fe01610e3d547c8`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 105.8 MB (105780999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c61c989715156f5e3fa19bc7fdbfad24e87b6032b1eb56461badb100b15eb18`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:7362a75f9fc9d90ddb3788c8681f03de2fd698520fd469d0648438f43528ffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a7ba2aee428ccba73a12f349b5607dff019f58a94ce7b7a5faaed5854ed087`

```dockerfile
```

-	Layers:
	-	`sha256:42f9dfc61585562f8e6cbc174e59943e4f9ca14bba15dff6fa41c07893aa7c65`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 3.7 MB (3716437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d14abb2a46307672df35acf9ae7fd0fe30d6d0595358495c34992b7c5b2079c`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 16.8 KB (16803 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:e9aebf31e94a9ec7e432b247ece0f19f9b5bae52394517f2758a0514a46350b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199487236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aab9be09893da92d715bd40818adcfa32ec3df651750265ba182cc7c54270e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:48 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 04:03:48 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 04:03:48 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:03:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 04:03:51 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3cbfb6348b2518482673002d1502686e380fd2e6bb0a33d3f3746b399337cc`  
		Last Modified: Tue, 07 Apr 2026 04:04:06 GMT  
		Size: 105.8 MB (105781039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20b2d10c1b8df12b1f5d49fac2e37be89693873e1ee81814de7e6eb016edea`  
		Last Modified: Tue, 07 Apr 2026 04:04:04 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e6ea9a6ecfef02223715c26e69e35f6b61ce4455972159f24ff8832239bb4344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a557d3e97ef327c0731dfdb6c48eb9965660adf228e30bad04bffbb6e2232d`

```dockerfile
```

-	Layers:
	-	`sha256:845e1a2b5b71696e7e99542ae7e8bd682ef19d077be3d7a2e488f7c9984bacb1`  
		Last Modified: Tue, 07 Apr 2026 04:04:04 GMT  
		Size: 3.7 MB (3720409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fce3ab78e5b6fca8038c4b4e4e45f0fb9902731064a956ba8bfdde7ab8a754`  
		Last Modified: Tue, 07 Apr 2026 04:04:03 GMT  
		Size: 16.9 KB (16880 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:b8fa3c73fbae87110f1a3975da178ca5cf25cbd31752c4bb90384246af4a6824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e578fa951949f45a5e1edf8db84289719b8441f3875d02872bd9d4ed445855`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:14:59 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:14:59 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:14:59 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:15:01 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7782880e40617ea58d4ccdfb8e1b1cd6866dc4970e221d551cac01106a7823f9`  
		Last Modified: Tue, 07 Apr 2026 03:15:16 GMT  
		Size: 105.8 MB (105781044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171fef55324e84b855e183ed0ece4abbf5bf7d7b31913925e5a35d58f5977a4e`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e1be43471f598d5061dce64bb4e48714b8cb5f9c8e242a8333c6192ac876d03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b5dc77875cb8ab6d3de28288acd8f8b5a4ce2115f6e7b326745b823376000a`

```dockerfile
```

-	Layers:
	-	`sha256:1874680f5d293577e46bcc16b4fd371f3b8bfe74a4d8e44546b9ecfa88e120ed`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 3.7 MB (3717584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca83a38d9a6851d5af1fa4500f12e20fb72004d90c79717da6ef412747e4e54`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 16.9 KB (16898 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.51`

```console
$ docker pull orientdb@sha256:f41e201b7657aa9f79485affb819a8a1dab4581840907679a89b6deee77b13da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.51` - linux; amd64

```console
$ docker pull orientdb@sha256:9b5a8f075279bafa40be9724d2d30ff4fcde68cb7c780fd9a349aa59e2e05740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175740656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f8d6418699d3e8296ccbd4e04405c3c3abfca4aba575fdbaed700cbde63d27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:01:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:01:49 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:01:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:01:51 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8165adebcf18a8048f4737df4900e82297c31dda6bbe10db90c8e131d6fd45`  
		Last Modified: Tue, 07 Apr 2026 03:02:05 GMT  
		Size: 73.8 MB (73848096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51` - unknown; unknown

```console
$ docker pull orientdb@sha256:8f0e5b71d77c909d7d713c07768809a191d27b8fe85b63cbd2e8ab3d1d1743e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c04a245d0d5cf7b3e46ce5b84eda53ff936d25c133897a521c6dfbf0cac0047`

```dockerfile
```

-	Layers:
	-	`sha256:97cbfd97db3b13d9949d0bf026fd93265133345d009844951bd930cce6c4ed84`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 3.6 MB (3580298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefc653cc84f2fc95d77c6760ac5312004dffc9258e33ab828219a4d0bda0004`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.51` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:0227ade03beb308cbe4137a721804fb498968abe09b198f8e38941ee10e07f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167552951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f530b317585be7e9bfacd41dcec7176b7e3a193f605fa5c9ad07615c89d451`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:36 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 04:03:36 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 04:03:36 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:03:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 04:03:38 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0f5e732f93f7f6f2ba4945f1cd0a6daf9792f4e3db0ca15326eaa086c9772`  
		Last Modified: Tue, 07 Apr 2026 04:03:51 GMT  
		Size: 73.8 MB (73848126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51` - unknown; unknown

```console
$ docker pull orientdb@sha256:fdba055340baaa5579fa6fe2d8cab6addb3ddeab7ea0c85a3b3b42eae76d7744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d00dee6643c4798eb804b6e05e5d1701b3373df87b5807f8783fe3302e686c3`

```dockerfile
```

-	Layers:
	-	`sha256:434d7b3101c9db94b62c4b041044bfbc90949586505d8d94dd8b16ee9884c2b6`  
		Last Modified: Tue, 07 Apr 2026 04:03:50 GMT  
		Size: 3.6 MB (3584278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b3da82ad3466a1e1b08383452326481ce036145a23ddd6a99d496e7b23294a`  
		Last Modified: Tue, 07 Apr 2026 04:03:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.51` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:265fab891b04d9150b5fb331508e399e6fea7fc714634e621daefe1f6d6c43fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (173981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c9f0ea8d995bf76556dcdc34de10250efc16eda302702704a0cfc2520aa9b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:14:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:14:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:14:44 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:14:46 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1b18df539adc7bb391c7f271270d3dcc63a9beb172a09f4cfc27f732cf2ed`  
		Last Modified: Tue, 07 Apr 2026 03:15:00 GMT  
		Size: 73.8 MB (73848125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51` - unknown; unknown

```console
$ docker pull orientdb@sha256:83d2290a8e6c1cc6dce80567c67fdcfcd50fc4f99c049ff25b4c3a1e4e296f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f56622e1667d86f982e8ce7abb2a879b2d2a82f606d8541b477c6dbde3f1b4`

```dockerfile
```

-	Layers:
	-	`sha256:d37572cbcb89e0b18d90613e005b67ab29f0de7ca0be831574d4fcd0f9621491`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 3.6 MB (3581457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c4ee6a92d3d0c5b24bdf2e6942abad8d7188dca63577bdaca99a09072a077b`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.51-tp3`

```console
$ docker pull orientdb@sha256:0cef004680bb5fff65c8761139517dcd5fb6e3bf5ace795cded27cdce31d36a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.51-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:27727cd95a37d4d6c640644a79ff80c7a05036bb33a921c0e6ac6a3977de0092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207674929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df95100abc660898fc55d1feb0729e05d899a7d2b09a5e627f2418393a7d054d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:58 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:01:58 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 03:01:58 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:01:58 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:02:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:02:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:02:01 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:02:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f0a458143238b524553a3b4415e79243a4855da69be69f6fe01610e3d547c8`  
		Last Modified: Tue, 07 Apr 2026 03:02:16 GMT  
		Size: 105.8 MB (105780999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c61c989715156f5e3fa19bc7fdbfad24e87b6032b1eb56461badb100b15eb18`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:7362a75f9fc9d90ddb3788c8681f03de2fd698520fd469d0648438f43528ffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a7ba2aee428ccba73a12f349b5607dff019f58a94ce7b7a5faaed5854ed087`

```dockerfile
```

-	Layers:
	-	`sha256:42f9dfc61585562f8e6cbc174e59943e4f9ca14bba15dff6fa41c07893aa7c65`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 3.7 MB (3716437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d14abb2a46307672df35acf9ae7fd0fe30d6d0595358495c34992b7c5b2079c`  
		Last Modified: Tue, 07 Apr 2026 03:02:13 GMT  
		Size: 16.8 KB (16803 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.51-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:e9aebf31e94a9ec7e432b247ece0f19f9b5bae52394517f2758a0514a46350b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199487236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aab9be09893da92d715bd40818adcfa32ec3df651750265ba182cc7c54270e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:48 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 04:03:48 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 04:03:48 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 04:03:48 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 04:03:51 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:03:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 04:03:51 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 04:03:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3cbfb6348b2518482673002d1502686e380fd2e6bb0a33d3f3746b399337cc`  
		Last Modified: Tue, 07 Apr 2026 04:04:06 GMT  
		Size: 105.8 MB (105781039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20b2d10c1b8df12b1f5d49fac2e37be89693873e1ee81814de7e6eb016edea`  
		Last Modified: Tue, 07 Apr 2026 04:04:04 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e6ea9a6ecfef02223715c26e69e35f6b61ce4455972159f24ff8832239bb4344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a557d3e97ef327c0731dfdb6c48eb9965660adf228e30bad04bffbb6e2232d`

```dockerfile
```

-	Layers:
	-	`sha256:845e1a2b5b71696e7e99542ae7e8bd682ef19d077be3d7a2e488f7c9984bacb1`  
		Last Modified: Tue, 07 Apr 2026 04:04:04 GMT  
		Size: 3.7 MB (3720409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fce3ab78e5b6fca8038c4b4e4e45f0fb9902731064a956ba8bfdde7ab8a754`  
		Last Modified: Tue, 07 Apr 2026 04:04:03 GMT  
		Size: 16.9 KB (16880 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.51-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:b8fa3c73fbae87110f1a3975da178ca5cf25cbd31752c4bb90384246af4a6824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205916226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e578fa951949f45a5e1edf8db84289719b8441f3875d02872bd9d4ed445855`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:14:59 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:14:59 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_MD5=6078b836b1941c84728e74787490b5aa
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a360a68840da6221d399c85aa2b3d87352ab8955
# Tue, 07 Apr 2026 03:14:59 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.51/orientdb-tp3-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:14:59 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 07 Apr 2026 03:15:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:15:01 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 07 Apr 2026 03:15:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7782880e40617ea58d4ccdfb8e1b1cd6866dc4970e221d551cac01106a7823f9`  
		Last Modified: Tue, 07 Apr 2026 03:15:16 GMT  
		Size: 105.8 MB (105781044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171fef55324e84b855e183ed0ece4abbf5bf7d7b31913925e5a35d58f5977a4e`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.51-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:e1be43471f598d5061dce64bb4e48714b8cb5f9c8e242a8333c6192ac876d03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b5dc77875cb8ab6d3de28288acd8f8b5a4ce2115f6e7b326745b823376000a`

```dockerfile
```

-	Layers:
	-	`sha256:1874680f5d293577e46bcc16b4fd371f3b8bfe74a4d8e44546b9ecfa88e120ed`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 3.7 MB (3717584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca83a38d9a6851d5af1fa4500f12e20fb72004d90c79717da6ef412747e4e54`  
		Last Modified: Tue, 07 Apr 2026 03:15:14 GMT  
		Size: 16.9 KB (16898 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:f41e201b7657aa9f79485affb819a8a1dab4581840907679a89b6deee77b13da
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
$ docker pull orientdb@sha256:9b5a8f075279bafa40be9724d2d30ff4fcde68cb7c780fd9a349aa59e2e05740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175740656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f8d6418699d3e8296ccbd4e04405c3c3abfca4aba575fdbaed700cbde63d27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:01:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:01:49 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:01:49 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:01:51 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:01:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:01:51 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:01:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8165adebcf18a8048f4737df4900e82297c31dda6bbe10db90c8e131d6fd45`  
		Last Modified: Tue, 07 Apr 2026 03:02:05 GMT  
		Size: 73.8 MB (73848096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:8f0e5b71d77c909d7d713c07768809a191d27b8fe85b63cbd2e8ab3d1d1743e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c04a245d0d5cf7b3e46ce5b84eda53ff936d25c133897a521c6dfbf0cac0047`

```dockerfile
```

-	Layers:
	-	`sha256:97cbfd97db3b13d9949d0bf026fd93265133345d009844951bd930cce6c4ed84`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 3.6 MB (3580298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefc653cc84f2fc95d77c6760ac5312004dffc9258e33ab828219a4d0bda0004`  
		Last Modified: Tue, 07 Apr 2026 03:02:03 GMT  
		Size: 14.5 KB (14471 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:0227ade03beb308cbe4137a721804fb498968abe09b198f8e38941ee10e07f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167552951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f530b317585be7e9bfacd41dcec7176b7e3a193f605fa5c9ad07615c89d451`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:36 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 04:03:36 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 04:03:36 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 04:03:36 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 04:03:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:03:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 04:03:38 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 04:03:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0f5e732f93f7f6f2ba4945f1cd0a6daf9792f4e3db0ca15326eaa086c9772`  
		Last Modified: Tue, 07 Apr 2026 04:03:51 GMT  
		Size: 73.8 MB (73848126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:fdba055340baaa5579fa6fe2d8cab6addb3ddeab7ea0c85a3b3b42eae76d7744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d00dee6643c4798eb804b6e05e5d1701b3373df87b5807f8783fe3302e686c3`

```dockerfile
```

-	Layers:
	-	`sha256:434d7b3101c9db94b62c4b041044bfbc90949586505d8d94dd8b16ee9884c2b6`  
		Last Modified: Tue, 07 Apr 2026 04:03:50 GMT  
		Size: 3.6 MB (3584278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b3da82ad3466a1e1b08383452326481ce036145a23ddd6a99d496e7b23294a`  
		Last Modified: Tue, 07 Apr 2026 04:03:49 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:265fab891b04d9150b5fb331508e399e6fea7fc714634e621daefe1f6d6c43fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (173981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c9f0ea8d995bf76556dcdc34de10250efc16eda302702704a0cfc2520aa9b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:14:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 07 Apr 2026 03:14:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_VERSION=3.2.51
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_MD5=75ee7229880272d220ffeebf776fcefd
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c54a73fe01388fc426283f75247a7940a1f131e3
# Tue, 07 Apr 2026 03:14:44 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.51/orientdb-community-3.2.51.tar.gz
# Tue, 07 Apr 2026 03:14:44 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 07 Apr 2026 03:14:46 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 07 Apr 2026 03:14:46 GMT
WORKDIR /orientdb
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 07 Apr 2026 03:14:46 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1b18df539adc7bb391c7f271270d3dcc63a9beb172a09f4cfc27f732cf2ed`  
		Last Modified: Tue, 07 Apr 2026 03:15:00 GMT  
		Size: 73.8 MB (73848125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:83d2290a8e6c1cc6dce80567c67fdcfcd50fc4f99c049ff25b4c3a1e4e296f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f56622e1667d86f982e8ce7abb2a879b2d2a82f606d8541b477c6dbde3f1b4`

```dockerfile
```

-	Layers:
	-	`sha256:d37572cbcb89e0b18d90613e005b67ab29f0de7ca0be831574d4fcd0f9621491`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 3.6 MB (3581457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c4ee6a92d3d0c5b24bdf2e6942abad8d7188dca63577bdaca99a09072a077b`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 14.6 KB (14578 bytes)  
		MIME: application/vnd.in-toto+json
