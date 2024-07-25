## `flink:scala_2.12-java8`

```console
$ docker pull flink@sha256:ea06b81ca4e45043be0345459c00bc37b006bd2bf3406f84e084fbf4f6213b5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:7a385601cc71b2f6af3cdfb07bcfdf865afab5fe0df041971e51ca76ce4cac08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573684761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe423706a40be325255c2d99e534b93c2a40109be25894ca08f0e4280e9d825`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 17 Jun 2024 19:26:44 GMT
ARG RELEASE
# Mon, 17 Jun 2024 19:26:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 17 Jun 2024 19:26:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 17 Jun 2024 19:26:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 17 Jun 2024 19:26:44 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 17 Jun 2024 19:26:44 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 19:26:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Jun 2024 19:26:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Jun 2024 19:26:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENV GOSU_VERSION=1.11
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.19.1/flink-1.19.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.19.1/flink-1.19.1-bin-scala_2.12.tgz.asc GPG_KEY=6378E37EB3AAEA188B9CB0D396C2914BB78A5EA1 CHECK_GPG=true
# Mon, 17 Jun 2024 19:26:44 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 17 Jun 2024 19:26:44 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Jun 2024 19:26:44 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
WORKDIR /opt/flink
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Jun 2024 19:26:44 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Mon, 17 Jun 2024 19:26:44 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aa4c2b7311ae2bf5d45bc877436e46ebc859b01d2cf63b66a3be9fa6ab8867`  
		Last Modified: Thu, 25 Jul 2024 17:27:24 GMT  
		Size: 41.9 MB (41884565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdf9faa7f7d71b1e6168b61d171833e8e9dc3d56c7cc5100108961303ec9f8b`  
		Last Modified: Thu, 25 Jul 2024 17:27:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e47ff4909e5589dd954ed48c76db5fcd454897fb4a03b27c06e73bbbcfeb0`  
		Last Modified: Thu, 25 Jul 2024 17:27:20 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649306ce6e9511891326232699af46e312ed3232b892a3fd236271c3f3d344c`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 4.4 MB (4416676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76405da2d5a31dd95f13705dc131ebc34d4301767dcbafb05affaf117898dee8`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 900.5 KB (900494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308fbb259e1e602cabd63b5d0b27e116904334c6c8387bbf13b093a596e24130`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 4.6 KB (4593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa64f9e420db0b459f50335b9173303f6f0bd0c42e2357c30bc2cf22ee20f7`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9c0863cc558fe7af1b90672a0cc98bcf56db165226aa9604593847fa93a9d5`  
		Last Modified: Thu, 25 Jul 2024 20:09:37 GMT  
		Size: 483.2 MB (483163125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6dac5fb8166dd2c284a294c142aeeb5d1b8ec007e652004e5e9b036b2ac514`  
		Last Modified: Thu, 25 Jul 2024 20:09:31 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:9ba7773609b243d3c4b3a22b1ae0a3373d68c60f7dc4b0e9b73c21eab4189bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47908e32bc33a192dc3b65038bc8a9917752689520fa0121447bda072d724bc5`

```dockerfile
```

-	Layers:
	-	`sha256:db7632630f8c1ecf519a0de95415433799515e5d18c8a72f52f874f44956d359`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 3.7 MB (3747780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36cff149df6e36a3733351fa632d3740835a60fa187b99d948fe9e6217d2b479`  
		Last Modified: Thu, 25 Jul 2024 20:09:30 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:61e362333ef0cf4e9ffbc999385907cd5c3d58fcbba2941f165883fbb57e3698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570336559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e050b71ab03332ee8257332c0f85bbd6499df50f422da9b35b4c907b9213f468`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 17 Jun 2024 19:26:44 GMT
ARG RELEASE
# Mon, 17 Jun 2024 19:26:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 17 Jun 2024 19:26:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 17 Jun 2024 19:26:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 17 Jun 2024 19:26:44 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 17 Jun 2024 19:26:44 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENV GOSU_VERSION=1.11
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.19.1/flink-1.19.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.19.1/flink-1.19.1-bin-scala_2.12.tgz.asc GPG_KEY=6378E37EB3AAEA188B9CB0D396C2914BB78A5EA1 CHECK_GPG=true
# Mon, 17 Jun 2024 19:26:44 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 17 Jun 2024 19:26:44 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Jun 2024 19:26:44 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
WORKDIR /opt/flink
# Mon, 17 Jun 2024 19:26:44 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Jun 2024 19:26:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Jun 2024 19:26:44 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Mon, 17 Jun 2024 19:26:44 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a65c37a73318ad8851dffc22f21e69a43d90d30b0331807250d98c3e6553f5`  
		Last Modified: Tue, 02 Jul 2024 04:34:43 GMT  
		Size: 40.9 MB (40850737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e043158e8c2903abe32b5e521dd3bde83f3edf6e963630b1fd624a06ccc52a9f`  
		Last Modified: Tue, 02 Jul 2024 04:34:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319a9bb656dedf4e82fb418f6ba561fd3fcc988c3dd94f55fa963f8c3b0c60f2`  
		Last Modified: Tue, 02 Jul 2024 04:34:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5a7720d1d699580249cab6bcf72325b9dc72f0987650ac04f2ef82c2c8ca09`  
		Last Modified: Tue, 02 Jul 2024 11:15:50 GMT  
		Size: 4.3 MB (4265355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548548f70b5fb6f14251160b249f68db2387da64f4e61fc2f7208b6157d18599`  
		Last Modified: Tue, 02 Jul 2024 11:15:50 GMT  
		Size: 835.4 KB (835381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7c1496f7887186d3ee2376c27fd406ab11c77bede178c07e6ee5dd64e5f96`  
		Last Modified: Tue, 02 Jul 2024 11:15:49 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f6dbae4f08acd6f5165f8b70471559119999afdcce3d9ab2fdd5577faa6589`  
		Last Modified: Tue, 02 Jul 2024 11:15:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae2f845ace543148b3bebeac25d67b0daa34ffbcf6817c8573ae2b908111e4`  
		Last Modified: Tue, 02 Jul 2024 11:16:00 GMT  
		Size: 483.2 MB (483163119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed650cfc5b46f3f99579aea532a62af8b3d196c72b9ef0951684e46d83adc8`  
		Last Modified: Tue, 02 Jul 2024 11:15:51 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:d1731e2e57ae40db1c4beba65549bb032585b681a1c63fcc4f2c2bd44be56e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1372f5b048b9c173bc6dc0668627017106baff6f8083f00a8183c634024cf7ee`

```dockerfile
```

-	Layers:
	-	`sha256:8b580939ae765fc7c94d63100c23aba8399f3f3ccb62540fa7775eb07c9a5c57`  
		Last Modified: Tue, 02 Jul 2024 11:15:50 GMT  
		Size: 3.7 MB (3706980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850740160c1ec478b1853f271b6b0fd74cc7de2824c31c69cafad0aee4a04755`  
		Last Modified: Tue, 02 Jul 2024 11:15:49 GMT  
		Size: 31.3 KB (31286 bytes)  
		MIME: application/vnd.in-toto+json
