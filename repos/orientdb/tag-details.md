<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.37`](#orientdb3237)
-	[`orientdb:3.2.37-tp3`](#orientdb3237-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:efad1eac77762782c796159c9bc6780e7e147dce82458d26aebe2af1e3422b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:b7e34e4e347c7f10bee48a137ccb986bc2e321ad0904cbe174424f7823ee276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154522409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7017af3fd65b54f5b2744f9cd51f3b3482d5570f585cf2b858d337ad27c84a15`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a285b4f867a47bd986740253a527cc7db316755d9b517ce8256d05029283cd`  
		Last Modified: Tue, 04 Feb 2025 05:25:37 GMT  
		Size: 53.1 MB (53081029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1` - unknown; unknown

```console
$ docker pull orientdb@sha256:66031d9a8617b071577e62187b23dd7db9fe24cc609d81b6e5b26fbd367e19cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9cd761f94bc177584fe74b4cbe57c7d59cc28870839cd2326018b8def9de51`

```dockerfile
```

-	Layers:
	-	`sha256:e7458703c2c9a61232a65e3c26748528a55fb4ec699568c0ad27929b50a2345a`  
		Last Modified: Tue, 04 Feb 2025 05:25:36 GMT  
		Size: 3.4 MB (3405152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3c00340d40e53eae40dd6c10f6be537dcc2583b1fdcbf7f2b04f92b3094bd3`  
		Last Modified: Tue, 04 Feb 2025 05:25:36 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:a0c9ffddbc3c64261d908788e0fb197f51634b851a5eab0050c2f76623831b87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:dd7f843d1b4b18190b543da00085e23c950d6e3725ead6139534b510a4d9e31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177529496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa0784b9b89d140f8f848e75bc097f804462db93ab106aa6cef356b60bc736`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c520c52d0c5508403122a0ae850816a0e6f5fefa4c14945aeefd8ead88407c77`  
		Last Modified: Tue, 04 Feb 2025 05:25:56 GMT  
		Size: 76.1 MB (76086742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c44eb018f71f96c53d983cdcd3b3c324fd452b9cabc9e2fd69439851ddb69`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:080508d0839bf16ed2b4c38e95f291249395425729d44c58b5cb927eb57cf369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaa11ae817c0ebc777dc422032fdd561213425b473ed89d222aebe63d000841`

```dockerfile
```

-	Layers:
	-	`sha256:62a1bd443a1235c2d5f316364d5d6145000ed8d8b3409ce159bef94243456d6a`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 3.5 MB (3467204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1805e49d424e02e2d207e7dcaf1bf30581b4f69245559151be41a154f91c56fa`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:efad1eac77762782c796159c9bc6780e7e147dce82458d26aebe2af1e3422b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:b7e34e4e347c7f10bee48a137ccb986bc2e321ad0904cbe174424f7823ee276d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154522409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7017af3fd65b54f5b2744f9cd51f3b3482d5570f585cf2b858d337ad27c84a15`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a285b4f867a47bd986740253a527cc7db316755d9b517ce8256d05029283cd`  
		Last Modified: Tue, 04 Feb 2025 05:25:37 GMT  
		Size: 53.1 MB (53081029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20` - unknown; unknown

```console
$ docker pull orientdb@sha256:66031d9a8617b071577e62187b23dd7db9fe24cc609d81b6e5b26fbd367e19cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9cd761f94bc177584fe74b4cbe57c7d59cc28870839cd2326018b8def9de51`

```dockerfile
```

-	Layers:
	-	`sha256:e7458703c2c9a61232a65e3c26748528a55fb4ec699568c0ad27929b50a2345a`  
		Last Modified: Tue, 04 Feb 2025 05:25:36 GMT  
		Size: 3.4 MB (3405152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3c00340d40e53eae40dd6c10f6be537dcc2583b1fdcbf7f2b04f92b3094bd3`  
		Last Modified: Tue, 04 Feb 2025 05:25:36 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:a0c9ffddbc3c64261d908788e0fb197f51634b851a5eab0050c2f76623831b87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:dd7f843d1b4b18190b543da00085e23c950d6e3725ead6139534b510a4d9e31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177529496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa0784b9b89d140f8f848e75bc097f804462db93ab106aa6cef356b60bc736`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 15 Sep 2022 13:05:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c520c52d0c5508403122a0ae850816a0e6f5fefa4c14945aeefd8ead88407c77`  
		Last Modified: Tue, 04 Feb 2025 05:25:56 GMT  
		Size: 76.1 MB (76086742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1c44eb018f71f96c53d983cdcd3b3c324fd452b9cabc9e2fd69439851ddb69`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.1.20-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:080508d0839bf16ed2b4c38e95f291249395425729d44c58b5cb927eb57cf369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaa11ae817c0ebc777dc422032fdd561213425b473ed89d222aebe63d000841`

```dockerfile
```

-	Layers:
	-	`sha256:62a1bd443a1235c2d5f316364d5d6145000ed8d8b3409ce159bef94243456d6a`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 3.5 MB (3467204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1805e49d424e02e2d207e7dcaf1bf30581b4f69245559151be41a154f91c56fa`  
		Last Modified: Tue, 04 Feb 2025 05:25:54 GMT  
		Size: 16.8 KB (16843 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:d1d6997df5782a20483b1b652dc7d1ced800ebc0daa6b1af6bbf26a3ebef1c9f
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
$ docker pull orientdb@sha256:3663ef76923c9a40cba65c82b54309bcf86e148b573f4d961272aa2e79540d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174370370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929682e5d7fb319f69a87082e8eba63acac8211b835cc39614aed83d06aa24a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 14 Jan 2025 21:39:38 GMT
ARG RELEASE
# Tue, 14 Jan 2025 21:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 14 Jan 2025 21:39:38 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ed528459e0f4728c1e9e4235261901d2cb103c9713aca0396e15d7e20de0ac`  
		Last Modified: Tue, 04 Feb 2025 05:25:43 GMT  
		Size: 72.9 MB (72928990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:49ad80ffca4d1ab41f268db58496040468cb5f5d4b3e917aa726ec6e61b23fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d41a1a19b4080669b70dde3324c37e36514a89a7255c5c7a67872c0f53ced3`

```dockerfile
```

-	Layers:
	-	`sha256:099d290d537309f8e7b2d606cf46a4535808e5df7325f2b88fe25371a29950f1`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 3.4 MB (3414530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfeed755a75d35633c902a1982e0d365ef0d6aaeee53602d43e5eed03cbe71c`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c48336e78ecc2aee498077dd66f5a39648eaded27872f21166def144afc223b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166793628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488738b8aebe1c0b00f3f5fb2d051640a8580a546c852ea3caa4f27b5697ab93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f93a80dde6e9684cad938824cb418dd4c7525b2edbf7c763cb87fba459fdfb`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 582.9 KB (582896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430943af2548b8079e445ad27ccab8722d54b62d3f427fcbe7b5a9fed61d9289`  
		Last Modified: Fri, 31 Jan 2025 02:35:16 GMT  
		Size: 72.9 MB (72928993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:55d5db862ee73a23327a245193587c8cf5d8c297f39ff255282254714565ea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925c780bca99c543a31d9a853554c9a9d2050eaf28b2d5028bb31660f9858cb`

```dockerfile
```

-	Layers:
	-	`sha256:62c02e2c148a0004afc0015dd4e115034f81c9466b21733ac2a170051bc27307`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 3.4 MB (3414864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29c07ce2988899b7d25b784adba4591a9556443450d3234bf562384c2aeaf1a`  
		Last Modified: Fri, 31 Jan 2025 02:35:13 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:8aef8a45eaa020126a64ad5e8ed00cb524049d2d78b83f3d81ff46de2f9491b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172633726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e569751a045f029f3691934d55516a724b354e1567524fd66f12b3b1cc43944`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b19f6957ca7ae3ee3247396433d9cd26957f1959062f1573076801c92e3314`  
		Last Modified: Fri, 31 Jan 2025 01:32:08 GMT  
		Size: 53.8 MB (53826711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948541f3f2dedc142267828b326b04dc5743dc1a6f033fd23b1304f2de545f9`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7797501b77dbe21eacf7bb6ec41647e6509ea93dd3b6a92f5e0e495f7184be`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64500d73efbdca5bea78bcfc9ba51b84e771eeca97cdb15709d021deb66adc`  
		Last Modified: Fri, 31 Jan 2025 03:38:13 GMT  
		Size: 72.9 MB (72928996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2` - unknown; unknown

```console
$ docker pull orientdb@sha256:7b2779cf375b95f44fa38395d07072d0124eea4514055155d28970566987764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299dbac6fac93340a14248d4e9b5daffdb290ee4c82ab0b2e22b10b81b2bcef8`

```dockerfile
```

-	Layers:
	-	`sha256:0199562dae0f51689038af2445056eb0078667cec7669aa3b521c1f8d71a58c6`  
		Last Modified: Fri, 31 Jan 2025 03:38:11 GMT  
		Size: 3.4 MB (3412337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406235b291972c6cfa77677ebc3c427584740aa13cfe76e8a072b6fe18c9e669`  
		Last Modified: Fri, 31 Jan 2025 03:38:10 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:83e7e28a2fde0b55278f7b90fb9e63790e983f71027c145e9c673b1ffbb7b0b2
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
$ docker pull orientdb@sha256:529879a9bb46d43c3bed28fbe3ef5990bdd3bc749e75c80c62daf524a9ef14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206296581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ed328bb9d576f5dce35da67a8a687c73ef5bacafb6da886699040d28588d7e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 14 Jan 2025 21:39:38 GMT
ARG RELEASE
# Tue, 14 Jan 2025 21:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 14 Jan 2025 21:39:38 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4749285af0b32c893a5b34c08fc0a5f29a0cc5ae45f337b8bc79f45061cd06`  
		Last Modified: Tue, 04 Feb 2025 05:25:47 GMT  
		Size: 104.9 MB (104853828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf1725b1bd7c6ee59d8359019ec6612c8504ca5335036f57d96ecb22113670`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:01a068ec84d6fcee61cc1868b971379d4feffeeafbb98015ae2890c00dd42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049f78354709c6f9ec37dca4237d2a383ce369632e6f6fb5c50120dda7038734`

```dockerfile
```

-	Layers:
	-	`sha256:203be6929999cf6cc3fec059da35a79960673d82ee81bd8ed49e42d4f4dba6e9`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 3.5 MB (3545186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7701741c0d11f85db17438523a85205d313596045d28277b84891a8d6fe86ca0`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:b6d346d94a4b87fea70cde80c5c889d52c4b8c46c97f57e3cb0aae3412c941fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198719904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcde16f34d4945ca78672d93ad0f3c87139f83a4d243aab3d2dc352e5bd1742`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04b8254ccefb9495219f42b7326380f6e892f8759bba53e20af24b23b0fa64e`  
		Last Modified: Fri, 31 Jan 2025 02:36:07 GMT  
		Size: 582.9 KB (582923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d00f0515249f7814db09c6275d0c504068f71848bb12536e670138cf7d8c2`  
		Last Modified: Fri, 31 Jan 2025 02:36:10 GMT  
		Size: 104.9 MB (104853870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557839a72e8af97b27424aaafb4d1d8ead9785755dbf0bbd474321d8698b9cb1`  
		Last Modified: Fri, 31 Jan 2025 02:36:06 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:7b2c8ef97abbb67e2f6a151e115095faf0e30ba3af5bdaa10387db7a531b924c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39972a3b0c0cd738f7bfaca292475d79fd0b14283b1c8ed8dc5f70f27d0ced54`

```dockerfile
```

-	Layers:
	-	`sha256:09a8cc407db5cebf6d5af8ac37bbae91f6b0038d4e6a4bc4e621f0618c0f1abc`  
		Last Modified: Fri, 31 Jan 2025 02:36:07 GMT  
		Size: 3.5 MB (3545512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae7728e35e5ee57453f633e22e5c3d4aa85df2c6e600245d4f64944df94a9a9`  
		Last Modified: Fri, 31 Jan 2025 02:36:06 GMT  
		Size: 16.9 KB (16935 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:cb79b79a645d4d0e4b937cec4d398a70e165960c5f0a24ec66673684a3143d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204559972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa307b1536e48b7bed7c8db7c1e5708888ef04d2917eca40816d989479cfe0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b19f6957ca7ae3ee3247396433d9cd26957f1959062f1573076801c92e3314`  
		Last Modified: Fri, 31 Jan 2025 01:32:08 GMT  
		Size: 53.8 MB (53826711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948541f3f2dedc142267828b326b04dc5743dc1a6f033fd23b1304f2de545f9`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7797501b77dbe21eacf7bb6ec41647e6509ea93dd3b6a92f5e0e495f7184be`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54440bd65474232b89206f2340dc1d3b5b075d96d214750d498edeea1ab87fec`  
		Last Modified: Fri, 31 Jan 2025 03:38:54 GMT  
		Size: 104.9 MB (104853872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704630d0a26b4d87df361310f057a09921c6fcc02c5c490564a9ea15682102c2`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b684a6d6a898feee66377f968207c3a23b32403445f246fbc42b2315af689bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5f442eb160ddc463ee8046aba2c653cccf5ad4d8555188a52def3381ac7e9`

```dockerfile
```

-	Layers:
	-	`sha256:5637bc8d517b88367869cf1010dbb3ed7328af1a0f046bfa3a680fef4cd4ca0f`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 3.5 MB (3542981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc57da5de6f078a06a631e63fb4e993c07dc8a3b6388f73c89bc5f451ce525ff`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 16.9 KB (16940 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.37`

```console
$ docker pull orientdb@sha256:d1d6997df5782a20483b1b652dc7d1ced800ebc0daa6b1af6bbf26a3ebef1c9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:3663ef76923c9a40cba65c82b54309bcf86e148b573f4d961272aa2e79540d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174370370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929682e5d7fb319f69a87082e8eba63acac8211b835cc39614aed83d06aa24a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 14 Jan 2025 21:39:38 GMT
ARG RELEASE
# Tue, 14 Jan 2025 21:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 14 Jan 2025 21:39:38 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ed528459e0f4728c1e9e4235261901d2cb103c9713aca0396e15d7e20de0ac`  
		Last Modified: Tue, 04 Feb 2025 05:25:43 GMT  
		Size: 72.9 MB (72928990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37` - unknown; unknown

```console
$ docker pull orientdb@sha256:49ad80ffca4d1ab41f268db58496040468cb5f5d4b3e917aa726ec6e61b23fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d41a1a19b4080669b70dde3324c37e36514a89a7255c5c7a67872c0f53ced3`

```dockerfile
```

-	Layers:
	-	`sha256:099d290d537309f8e7b2d606cf46a4535808e5df7325f2b88fe25371a29950f1`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 3.4 MB (3414530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfeed755a75d35633c902a1982e0d365ef0d6aaeee53602d43e5eed03cbe71c`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.37` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c48336e78ecc2aee498077dd66f5a39648eaded27872f21166def144afc223b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166793628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488738b8aebe1c0b00f3f5fb2d051640a8580a546c852ea3caa4f27b5697ab93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f93a80dde6e9684cad938824cb418dd4c7525b2edbf7c763cb87fba459fdfb`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 582.9 KB (582896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430943af2548b8079e445ad27ccab8722d54b62d3f427fcbe7b5a9fed61d9289`  
		Last Modified: Fri, 31 Jan 2025 02:35:16 GMT  
		Size: 72.9 MB (72928993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37` - unknown; unknown

```console
$ docker pull orientdb@sha256:55d5db862ee73a23327a245193587c8cf5d8c297f39ff255282254714565ea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925c780bca99c543a31d9a853554c9a9d2050eaf28b2d5028bb31660f9858cb`

```dockerfile
```

-	Layers:
	-	`sha256:62c02e2c148a0004afc0015dd4e115034f81c9466b21733ac2a170051bc27307`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 3.4 MB (3414864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29c07ce2988899b7d25b784adba4591a9556443450d3234bf562384c2aeaf1a`  
		Last Modified: Fri, 31 Jan 2025 02:35:13 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.37` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:8aef8a45eaa020126a64ad5e8ed00cb524049d2d78b83f3d81ff46de2f9491b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172633726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e569751a045f029f3691934d55516a724b354e1567524fd66f12b3b1cc43944`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b19f6957ca7ae3ee3247396433d9cd26957f1959062f1573076801c92e3314`  
		Last Modified: Fri, 31 Jan 2025 01:32:08 GMT  
		Size: 53.8 MB (53826711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948541f3f2dedc142267828b326b04dc5743dc1a6f033fd23b1304f2de545f9`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7797501b77dbe21eacf7bb6ec41647e6509ea93dd3b6a92f5e0e495f7184be`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64500d73efbdca5bea78bcfc9ba51b84e771eeca97cdb15709d021deb66adc`  
		Last Modified: Fri, 31 Jan 2025 03:38:13 GMT  
		Size: 72.9 MB (72928996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37` - unknown; unknown

```console
$ docker pull orientdb@sha256:7b2779cf375b95f44fa38395d07072d0124eea4514055155d28970566987764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299dbac6fac93340a14248d4e9b5daffdb290ee4c82ab0b2e22b10b81b2bcef8`

```dockerfile
```

-	Layers:
	-	`sha256:0199562dae0f51689038af2445056eb0078667cec7669aa3b521c1f8d71a58c6`  
		Last Modified: Fri, 31 Jan 2025 03:38:11 GMT  
		Size: 3.4 MB (3412337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406235b291972c6cfa77677ebc3c427584740aa13cfe76e8a072b6fe18c9e669`  
		Last Modified: Fri, 31 Jan 2025 03:38:10 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:3.2.37-tp3`

```console
$ docker pull orientdb@sha256:83e7e28a2fde0b55278f7b90fb9e63790e983f71027c145e9c673b1ffbb7b0b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `orientdb:3.2.37-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:529879a9bb46d43c3bed28fbe3ef5990bdd3bc749e75c80c62daf524a9ef14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206296581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ed328bb9d576f5dce35da67a8a687c73ef5bacafb6da886699040d28588d7e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 14 Jan 2025 21:39:38 GMT
ARG RELEASE
# Tue, 14 Jan 2025 21:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 14 Jan 2025 21:39:38 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4749285af0b32c893a5b34c08fc0a5f29a0cc5ae45f337b8bc79f45061cd06`  
		Last Modified: Tue, 04 Feb 2025 05:25:47 GMT  
		Size: 104.9 MB (104853828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf1725b1bd7c6ee59d8359019ec6612c8504ca5335036f57d96ecb22113670`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:01a068ec84d6fcee61cc1868b971379d4feffeeafbb98015ae2890c00dd42cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049f78354709c6f9ec37dca4237d2a383ce369632e6f6fb5c50120dda7038734`

```dockerfile
```

-	Layers:
	-	`sha256:203be6929999cf6cc3fec059da35a79960673d82ee81bd8ed49e42d4f4dba6e9`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 3.5 MB (3545186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7701741c0d11f85db17438523a85205d313596045d28277b84891a8d6fe86ca0`  
		Last Modified: Tue, 04 Feb 2025 05:25:45 GMT  
		Size: 16.8 KB (16846 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.37-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:b6d346d94a4b87fea70cde80c5c889d52c4b8c46c97f57e3cb0aae3412c941fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198719904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcde16f34d4945ca78672d93ad0f3c87139f83a4d243aab3d2dc352e5bd1742`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04b8254ccefb9495219f42b7326380f6e892f8759bba53e20af24b23b0fa64e`  
		Last Modified: Fri, 31 Jan 2025 02:36:07 GMT  
		Size: 582.9 KB (582923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d00f0515249f7814db09c6275d0c504068f71848bb12536e670138cf7d8c2`  
		Last Modified: Fri, 31 Jan 2025 02:36:10 GMT  
		Size: 104.9 MB (104853870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557839a72e8af97b27424aaafb4d1d8ead9785755dbf0bbd474321d8698b9cb1`  
		Last Modified: Fri, 31 Jan 2025 02:36:06 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:7b2c8ef97abbb67e2f6a151e115095faf0e30ba3af5bdaa10387db7a531b924c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39972a3b0c0cd738f7bfaca292475d79fd0b14283b1c8ed8dc5f70f27d0ced54`

```dockerfile
```

-	Layers:
	-	`sha256:09a8cc407db5cebf6d5af8ac37bbae91f6b0038d4e6a4bc4e621f0618c0f1abc`  
		Last Modified: Fri, 31 Jan 2025 02:36:07 GMT  
		Size: 3.5 MB (3545512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae7728e35e5ee57453f633e22e5c3d4aa85df2c6e600245d4f64944df94a9a9`  
		Last Modified: Fri, 31 Jan 2025 02:36:06 GMT  
		Size: 16.9 KB (16935 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:3.2.37-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:cb79b79a645d4d0e4b937cec4d398a70e165960c5f0a24ec66673684a3143d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204559972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa307b1536e48b7bed7c8db7c1e5708888ef04d2917eca40816d989479cfe0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9c7941c1e6bb5617b9f331fe9933e2c7
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=d70b8a8e2bc9208e2a141e23f2339b8202e8b966
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.37/orientdb-tp3-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ADD gremlin-server.yaml /orientdb/config # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[8182/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b19f6957ca7ae3ee3247396433d9cd26957f1959062f1573076801c92e3314`  
		Last Modified: Fri, 31 Jan 2025 01:32:08 GMT  
		Size: 53.8 MB (53826711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948541f3f2dedc142267828b326b04dc5743dc1a6f033fd23b1304f2de545f9`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7797501b77dbe21eacf7bb6ec41647e6509ea93dd3b6a92f5e0e495f7184be`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54440bd65474232b89206f2340dc1d3b5b075d96d214750d498edeea1ab87fec`  
		Last Modified: Fri, 31 Jan 2025 03:38:54 GMT  
		Size: 104.9 MB (104853872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704630d0a26b4d87df361310f057a09921c6fcc02c5c490564a9ea15682102c2`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:3.2.37-tp3` - unknown; unknown

```console
$ docker pull orientdb@sha256:b684a6d6a898feee66377f968207c3a23b32403445f246fbc42b2315af689bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5f442eb160ddc463ee8046aba2c653cccf5ad4d8555188a52def3381ac7e9`

```dockerfile
```

-	Layers:
	-	`sha256:5637bc8d517b88367869cf1010dbb3ed7328af1a0f046bfa3a680fef4cd4ca0f`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 3.5 MB (3542981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc57da5de6f078a06a631e63fb4e993c07dc8a3b6388f73c89bc5f451ce525ff`  
		Last Modified: Fri, 31 Jan 2025 03:38:51 GMT  
		Size: 16.9 KB (16940 bytes)  
		MIME: application/vnd.in-toto+json

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:d1d6997df5782a20483b1b652dc7d1ced800ebc0daa6b1af6bbf26a3ebef1c9f
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
$ docker pull orientdb@sha256:3663ef76923c9a40cba65c82b54309bcf86e148b573f4d961272aa2e79540d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174370370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929682e5d7fb319f69a87082e8eba63acac8211b835cc39614aed83d06aa24a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 14 Jan 2025 21:39:38 GMT
ARG RELEASE
# Tue, 14 Jan 2025 21:39:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Jan 2025 21:39:38 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 14 Jan 2025 21:39:38 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ed528459e0f4728c1e9e4235261901d2cb103c9713aca0396e15d7e20de0ac`  
		Last Modified: Tue, 04 Feb 2025 05:25:43 GMT  
		Size: 72.9 MB (72928990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:49ad80ffca4d1ab41f268db58496040468cb5f5d4b3e917aa726ec6e61b23fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d41a1a19b4080669b70dde3324c37e36514a89a7255c5c7a67872c0f53ced3`

```dockerfile
```

-	Layers:
	-	`sha256:099d290d537309f8e7b2d606cf46a4535808e5df7325f2b88fe25371a29950f1`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 3.4 MB (3414530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfeed755a75d35633c902a1982e0d365ef0d6aaeee53602d43e5eed03cbe71c`  
		Last Modified: Tue, 04 Feb 2025 05:25:41 GMT  
		Size: 14.5 KB (14514 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c48336e78ecc2aee498077dd66f5a39648eaded27872f21166def144afc223b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166793628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488738b8aebe1c0b00f3f5fb2d051640a8580a546c852ea3caa4f27b5697ab93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f93a80dde6e9684cad938824cb418dd4c7525b2edbf7c763cb87fba459fdfb`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 582.9 KB (582896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430943af2548b8079e445ad27ccab8722d54b62d3f427fcbe7b5a9fed61d9289`  
		Last Modified: Fri, 31 Jan 2025 02:35:16 GMT  
		Size: 72.9 MB (72928993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:55d5db862ee73a23327a245193587c8cf5d8c297f39ff255282254714565ea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3429471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925c780bca99c543a31d9a853554c9a9d2050eaf28b2d5028bb31660f9858cb`

```dockerfile
```

-	Layers:
	-	`sha256:62c02e2c148a0004afc0015dd4e115034f81c9466b21733ac2a170051bc27307`  
		Last Modified: Fri, 31 Jan 2025 02:35:14 GMT  
		Size: 3.4 MB (3414864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29c07ce2988899b7d25b784adba4591a9556443450d3234bf562384c2aeaf1a`  
		Last Modified: Fri, 31 Jan 2025 02:35:13 GMT  
		Size: 14.6 KB (14607 bytes)  
		MIME: application/vnd.in-toto+json

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:8aef8a45eaa020126a64ad5e8ed00cb524049d2d78b83f3d81ff46de2f9491b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172633726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e569751a045f029f3691934d55516a724b354e1567524fd66f12b3b1cc43944`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 21:39:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 14 Jan 2025 21:39:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_VERSION=3.2.37
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=977653e88a7c37e8593ed0dc5ca6a554
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=be9c442524d101d29f33a3542012bfc7b7d88862
# Tue, 14 Jan 2025 21:39:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.37/orientdb-community-3.2.37.tar.gz
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
# ARGS: ORIENTDB_DOWNLOAD_SERVER=
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/* # buildkit
# Tue, 14 Jan 2025 21:39:38 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 21:39:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 14 Jan 2025 21:39:38 GMT
WORKDIR /orientdb
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2424/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
EXPOSE map[2480/tcp:{}]
# Tue, 14 Jan 2025 21:39:38 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b19f6957ca7ae3ee3247396433d9cd26957f1959062f1573076801c92e3314`  
		Last Modified: Fri, 31 Jan 2025 01:32:08 GMT  
		Size: 53.8 MB (53826711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948541f3f2dedc142267828b326b04dc5743dc1a6f033fd23b1304f2de545f9`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7797501b77dbe21eacf7bb6ec41647e6509ea93dd3b6a92f5e0e495f7184be`  
		Last Modified: Fri, 31 Jan 2025 01:32:06 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64500d73efbdca5bea78bcfc9ba51b84e771eeca97cdb15709d021deb66adc`  
		Last Modified: Fri, 31 Jan 2025 03:38:13 GMT  
		Size: 72.9 MB (72928996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `orientdb:latest` - unknown; unknown

```console
$ docker pull orientdb@sha256:7b2779cf375b95f44fa38395d07072d0124eea4514055155d28970566987764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299dbac6fac93340a14248d4e9b5daffdb290ee4c82ab0b2e22b10b81b2bcef8`

```dockerfile
```

-	Layers:
	-	`sha256:0199562dae0f51689038af2445056eb0078667cec7669aa3b521c1f8d71a58c6`  
		Last Modified: Fri, 31 Jan 2025 03:38:11 GMT  
		Size: 3.4 MB (3412337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406235b291972c6cfa77677ebc3c427584740aa13cfe76e8a072b6fe18c9e669`  
		Last Modified: Fri, 31 Jan 2025 03:38:10 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json
