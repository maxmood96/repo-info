## `flink:scala_2.12-java8`

```console
$ docker pull flink@sha256:0f9eb2998dfb42fa1c89509a4185985405dd45fac053a3f88a52ac3a32afc003
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:3c93242a687bca36dbaad05efb5fae5e64ae4255717587c2ae7050fe01ecf0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.5 MB (572501809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a65bbfa48bee03a6f6d86ca363fda388bb96a777b559c3dfa0eaf2d1ec495a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 19 Mar 2024 03:11:48 GMT
ARG RELEASE
# Tue, 19 Mar 2024 03:11:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Mar 2024 03:11:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Mar 2024 03:11:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Mar 2024 03:11:48 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Tue, 19 Mar 2024 03:11:48 GMT
CMD ["/bin/bash"]
# Tue, 19 Mar 2024 03:11:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Mar 2024 03:11:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 03:11:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV GOSU_VERSION=1.11
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.19.0/flink-1.19.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.19.0/flink-1.19.0-bin-scala_2.12.tgz.asc GPG_KEY=028B6605F51BC296B56A5042E57D30ABEE75CA06 CHECK_GPG=true
# Tue, 19 Mar 2024 03:11:48 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 19 Mar 2024 03:11:48 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 03:11:48 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
WORKDIR /opt/flink
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Mar 2024 03:11:48 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 19 Mar 2024 03:11:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad8a9774f3d336c4bef8be489ea3445a1aa69933f5ead6c4b42f80a1c4ef32f`  
		Last Modified: Wed, 05 Jun 2024 04:58:44 GMT  
		Size: 41.9 MB (41877280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e281aa36619348a9333b1030c5f8a40a41189d2e58ce2cfa09aca7c9ddf30b2`  
		Last Modified: Wed, 05 Jun 2024 04:58:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93e3eea54631fb5cdaffe1eae4435563285c9db8c3ef0d73cb33662bc476488`  
		Last Modified: Wed, 05 Jun 2024 04:58:40 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1842a977707ef33a2624a7c5aabc3bea71bddfc83b6431b334dc0e9e6b8e9045`  
		Last Modified: Wed, 05 Jun 2024 06:13:45 GMT  
		Size: 4.4 MB (4416608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99362dead8a495c161e242467cb1a857569783cb86257925aa9c7b743eeb3`  
		Last Modified: Wed, 05 Jun 2024 06:13:45 GMT  
		Size: 900.5 KB (900492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6425b4b3c1ffd82c7bfd527ff8af57695faa182ce215e04acd13699abc2fa7`  
		Last Modified: Wed, 05 Jun 2024 06:13:44 GMT  
		Size: 4.6 KB (4587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97dbf73f6f4c78a4f6d8b986814a958faa695a4e919baa37d2996d33ad228b7`  
		Last Modified: Wed, 05 Jun 2024 06:13:44 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878c1635bf3aaf03d0058d947e0090829f41f39bc7323232256d03b02b8d7561`  
		Last Modified: Wed, 05 Jun 2024 06:13:52 GMT  
		Size: 482.0 MB (481955502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca29115855c10edfa28b9ff1f295a8ef4b1d12565f743291518e1bafa637553b`  
		Last Modified: Wed, 05 Jun 2024 06:13:14 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:dff79221236374f6a3f5179c483d3734a76fae802d9ca37ba0920eee2ae7d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06469c79d59077c6d0baa41cf63dbfdeb3bc02f0f75db0d441051b0bcbb633c5`

```dockerfile
```

-	Layers:
	-	`sha256:6231dfbc3b6824a5a2e3d6403182f3bb8f39d06a8544dd30fb21175ce1b98bda`  
		Last Modified: Wed, 05 Jun 2024 06:13:45 GMT  
		Size: 3.7 MB (3706649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9792d30bfb5663481c7c620e7494c46992e62649752a857748f343896d1d4f04`  
		Last Modified: Wed, 05 Jun 2024 06:13:44 GMT  
		Size: 31.0 KB (31031 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:c1d2faf4dcd34213e303254e25a31764f529426f793d64bf906bfaf9a79bf8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.2 MB (569163308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e973d892a25986bafa647a0a25422281efbdb82f7f509358dc92c5b8927687`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 19 Mar 2024 03:11:48 GMT
ARG RELEASE
# Tue, 19 Mar 2024 03:11:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Mar 2024 03:11:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Mar 2024 03:11:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Mar 2024 03:11:48 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Tue, 19 Mar 2024 03:11:48 GMT
CMD ["/bin/bash"]
# Tue, 19 Mar 2024 03:11:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Mar 2024 03:11:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 03:11:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV GOSU_VERSION=1.11
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.19.0/flink-1.19.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.19.0/flink-1.19.0-bin-scala_2.12.tgz.asc GPG_KEY=028B6605F51BC296B56A5042E57D30ABEE75CA06 CHECK_GPG=true
# Tue, 19 Mar 2024 03:11:48 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 19 Mar 2024 03:11:48 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 03:11:48 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
WORKDIR /opt/flink
# Tue, 19 Mar 2024 03:11:48 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Mar 2024 03:11:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Mar 2024 03:11:48 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 19 Mar 2024 03:11:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8ffd1866b98a447cd5ac5e11f530c8e4e0b4c3e320e58f158c2403c75a9996`  
		Last Modified: Thu, 02 May 2024 04:18:01 GMT  
		Size: 40.9 MB (40850775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c183ea9ee8e6185f12a87b90ba8f16a5753a9a6d66a79b16d5b7286bd5875`  
		Last Modified: Thu, 02 May 2024 04:17:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c7c0f4d6a870839c6546dc4f99fe0d4bb0ac6904fd708e335476bf1525f2b4`  
		Last Modified: Thu, 02 May 2024 04:17:58 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b4ec764df06bfeb07822407f41e24f67d87858b4ca85bd6d04fd410b3066f`  
		Last Modified: Thu, 16 May 2024 21:40:04 GMT  
		Size: 4.3 MB (4265621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347a961d4c70bebfc94bbbffce2ad63f78214b7867dba0e465861f2439ea2020`  
		Last Modified: Thu, 16 May 2024 21:40:04 GMT  
		Size: 835.4 KB (835381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb641eb173fe233668008692494504f7d33be733af67a7eb0bfc793203924b7`  
		Last Modified: Thu, 16 May 2024 21:40:03 GMT  
		Size: 4.6 KB (4632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfe4f5033517a2a7958ca66e1326e05f6068f74467a722e1e752abfc3c9f4da`  
		Last Modified: Thu, 16 May 2024 21:40:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4c3ab81ae502cd779f7eeebc582d5250aaa81e5edf351b3dbb01a704e3de3`  
		Last Modified: Thu, 16 May 2024 21:40:15 GMT  
		Size: 482.0 MB (481955408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92391f3392249debc8ca6147ab68acd9e22133a6635f9ac5425f46f2632be7dc`  
		Last Modified: Thu, 16 May 2024 21:40:05 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java8` - unknown; unknown

```console
$ docker pull flink@sha256:70ada78bdca6d31531bd5db3958ec526f9bf308bb7ace77ce36df8b5511ad705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69cf67e5b3c7c5216e4ca8bc1b2e6178cc16f1b5767f94366198cbbb447b92e`

```dockerfile
```

-	Layers:
	-	`sha256:94d82752e5e3fa91b719257b0609632cb5cb96e12fac1eaca50a4e37c5d74b36`  
		Last Modified: Thu, 16 May 2024 21:40:04 GMT  
		Size: 3.7 MB (3706911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2202441e4bfbfe252fb986fed7bdd5d0c8155e8e0ab4f902d64ffae4dd8bfb2`  
		Last Modified: Thu, 16 May 2024 21:40:03 GMT  
		Size: 31.9 KB (31862 bytes)  
		MIME: application/vnd.in-toto+json
