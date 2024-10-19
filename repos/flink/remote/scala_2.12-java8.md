## `flink:scala_2.12-java8`

```console
$ docker pull flink@sha256:17affa89b57de6da8441cef7e70acbbd4251d43bf2242d2e6d51cbb95b889571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:38e97007c82a3f731b5ac74c98277a13852da5074c861fc81ad9b324b058009b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.3 MB (573290899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbdc73c205218c69ae6c027e1946c8b5e9a9fb01018baf54927340c078f48b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 01 Aug 2024 06:57:14 GMT
ARG RELEASE
# Thu, 01 Aug 2024 06:57:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 06:57:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 06:57:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 01 Aug 2024 06:57:14 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 01 Aug 2024 06:57:14 GMT
CMD ["/bin/bash"]
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Aug 2024 06:57:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Aug 2024 06:57:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV GOSU_VERSION=1.11
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.20.0/flink-1.20.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.20.0/flink-1.20.0-bin-scala_2.12.tgz.asc GPG_KEY=B2D64016B940A7E0B9B72E0D7D0528B28037D8BC CHECK_GPG=true
# Thu, 01 Aug 2024 06:57:14 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 01 Aug 2024 06:57:14 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Aug 2024 06:57:14 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
WORKDIR /opt/flink
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 06:57:14 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 01 Aug 2024 06:57:14 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b4b528c27ad0dad298b615000c14c9ef1029d22bb5e6b0a009747cf9bae3f7`  
		Last Modified: Sat, 19 Oct 2024 02:06:26 GMT  
		Size: 12.9 MB (12887671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cd908fbe686cfbaaf4f1b069ad34844e140047e8c788815c88560a30463ab`  
		Last Modified: Sat, 19 Oct 2024 02:06:26 GMT  
		Size: 41.9 MB (41884513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23bcb14dba14d913736c3681fe46399aabbf65d803959b0c70aa1b06fe587cb`  
		Last Modified: Sat, 19 Oct 2024 02:06:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eef977f45ca9f3db505cab5faecbd52c0d2182c360ec18569de4959ea6ba75f`  
		Last Modified: Sat, 19 Oct 2024 02:06:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b6ab2bf9e11529ed7293b787d302d4a25dff2fa748e0206d812981908ede31`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 4.4 MB (4416586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc3b8d49943bce89f2360e6946bc1a7c7b42878b8de7e4f09bcd3b6f6d3e1a`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 900.5 KB (900496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0be8c69ef29ae8f74fcaadf32632ad17860ddecfac599d54bd01281fe687391`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 4.6 KB (4594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ab39c100d086cc9bcd9d292a3b100db54664da7ea6fbb5c7f71afc2add5032`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd460f1339c854bf37ddd2008992e572bb3cd58e247e1641c56bf761a8e3cee6`  
		Last Modified: Sat, 19 Oct 2024 02:54:17 GMT  
		Size: 483.7 MB (483656734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a2ec243d50bb543fbf6244b903ab4f08a445d285e3c3d1c076ba9fa9123a91`  
		Last Modified: Sat, 19 Oct 2024 02:54:11 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:e754085b9aad5558c857a95c1d08f8b2fac3058dffb42e4b22f6448b9e281c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65d03921f2d62fff8d32223190276776ce56356f93d0a4e3ba364b395a4bb76`

```dockerfile
```

-	Layers:
	-	`sha256:582785af5fb04a6ff6b7c9861267fcfa731fe224696e93c259fd98c97cc93d01`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 3.9 MB (3854559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f376e73cc8b2bb5a06f886bb4d3fed3508b026d4b8cece10714e29dab5ee40`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 31.0 KB (30952 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:8061c39adada669968988b27bf5185cb53a52e994cf35316dae539b327e24b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.8 MB (570834016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a6fa3f80f2bf1d0693785c79c94e26b07a4fca27e6264bf03fd0331bb73ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 01 Aug 2024 06:57:14 GMT
ARG RELEASE
# Thu, 01 Aug 2024 06:57:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 06:57:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 06:57:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 01 Aug 2024 06:57:14 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 01 Aug 2024 06:57:14 GMT
CMD ["/bin/bash"]
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Aug 2024 06:57:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Aug 2024 06:57:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV GOSU_VERSION=1.11
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.20.0/flink-1.20.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.20.0/flink-1.20.0-bin-scala_2.12.tgz.asc GPG_KEY=B2D64016B940A7E0B9B72E0D7D0528B28037D8BC CHECK_GPG=true
# Thu, 01 Aug 2024 06:57:14 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 01 Aug 2024 06:57:14 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Aug 2024 06:57:14 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
WORKDIR /opt/flink
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 06:57:14 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 01 Aug 2024 06:57:14 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8956c17b5cb49fb363d000d1ef52b7e7d40104676509065e611b12ce07f7f533`  
		Last Modified: Tue, 17 Sep 2024 01:38:02 GMT  
		Size: 40.9 MB (40856826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c29f9e296ba55a8100506c3227ffb1ce6c4581a6dbaa53fcce2ee7fd25f8a`  
		Last Modified: Tue, 17 Sep 2024 01:37:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23036c470dbb54e460536d9d124cff09d479ab97e2f503525a26081e336091b`  
		Last Modified: Tue, 17 Sep 2024 01:37:58 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1246d796842a131488d5ee8177ddc09383863e79870bdb967b7fc4608ebed58`  
		Last Modified: Tue, 17 Sep 2024 05:04:01 GMT  
		Size: 4.3 MB (4265361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60562f7d9db2222ab14b6bef691ba131364549a67c0ce05556def00169c661a`  
		Last Modified: Tue, 17 Sep 2024 05:04:01 GMT  
		Size: 835.4 KB (835382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c955dcb0d3e84bb0067e17b2957f912caa1021f2124a1d20b279a0ce48c344b`  
		Last Modified: Tue, 17 Sep 2024 05:04:00 GMT  
		Size: 4.6 KB (4628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23a74d9e5d0b9bf4078587a538c5692a4704bd1f36946b7c021a51631ceae4`  
		Last Modified: Tue, 17 Sep 2024 05:04:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192d03515b5bbcfd1d65308adb3500611c9ea591cc1bc7d462c37b10499882a8`  
		Last Modified: Tue, 17 Sep 2024 05:04:11 GMT  
		Size: 483.7 MB (483656879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f319d08a62daf2c1f738a3014597c9e45a36dd78c762f69ff0a96f3fc7b844b`  
		Last Modified: Tue, 17 Sep 2024 05:04:01 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:2477f9c236115b541db28e92b9de804a10b4d6572b9ecd6bb66ef556d5e0e8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3779403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d956f214013263a82cbb004996f6ff71d8799475d9693ec5938487ecb3c8210e`

```dockerfile
```

-	Layers:
	-	`sha256:de24349df4918e395e5e2edbd7d708b7c5fbdf805cd5d867249e00e0ce657bba`  
		Last Modified: Tue, 17 Sep 2024 05:04:01 GMT  
		Size: 3.7 MB (3748110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b82ed74f212a6dbfb4ebbbcb39dd3c1af3af348af7f8576f15746f3efa08c3`  
		Last Modified: Tue, 17 Sep 2024 05:04:00 GMT  
		Size: 31.3 KB (31293 bytes)  
		MIME: application/vnd.in-toto+json
