## `flink:scala_2.12-java21`

```console
$ docker pull flink@sha256:4282e57c91f708e0ef40f5fb10eefb0a431b2f9804542c9cd63d69e2af719fbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java21` - linux; amd64

```console
$ docker pull flink@sha256:7bfab6e320d5925e0120ca338536744a25308002d7e35ace504bc8e8010a9b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.7 MB (666726466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06b3a9596335120bdfb22dcfe122bfd2ee11389d77d261e4702169c973bb441`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 18 Mar 2025 11:08:35 GMT
ARG RELEASE
# Tue, 18 Mar 2025 11:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Mar 2025 11:08:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Mar 2025 11:08:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Mar 2025 11:08:35 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Tue, 18 Mar 2025 11:08:35 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:08:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Mar 2025 11:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 11:08:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV GOSU_VERSION=1.11
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.0.0/flink-2.0.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.0.0/flink-2.0.0-bin-scala_2.12.tgz.asc GPG_KEY=F8E419AA0B60C28879E876859DFF40967ABFC5A4 CHECK_GPG=true
# Tue, 18 Mar 2025 11:08:35 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 18 Mar 2025 11:08:35 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 11:08:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
WORKDIR /opt/flink
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 11:08:35 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 18 Mar 2025 11:08:35 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882ea02fb5c855bf43fdc95ed1014a31bed0f381b9c67d0c48fa6f4739b1b37`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 16.1 MB (16146129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca298b922759e55496c02c3046c177b262e098e2f246425d6ac38dcef5556b`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 52.9 MB (52891233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca81fa2d6cd8292d9a604b62d9bb2d5e109095de9d716b30ac6f8b00547bf63`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f097bb5d471697950a9be820f9ea4aee721a780ff33e2d096c0e549e0b5281f`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55173a9b9436cd2d23d782ce83e5d61ba32b09b80883638c20f00f8917617f2`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 1.2 MB (1169810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a08aabaf45d08f05810a665f2a3009c60a55a81cced94936a41489d9fdc63a`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 900.5 KB (900496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bd0d4c67611f88e53d1f26666035cba1b4ad51817b50d203b655e970817ae0`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 4.6 KB (4595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e47229cbcdac440a4d4a0c2efc9bf5498ee59e6785df6438996c5662ae0976`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc704904967d7ac74262ca73fb85c22ced544a31b88cd454ea78c1368ccd1c09`  
		Last Modified: Mon, 05 May 2025 17:03:33 GMT  
		Size: 566.1 MB (566076767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604b4e70a61b1300831f107d02ddb65b709947f4106eb3931cf6d92166f5afd4`  
		Last Modified: Mon, 05 May 2025 17:03:24 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java21` - unknown; unknown

```console
$ docker pull flink@sha256:dca19b0758451eb506a6620c365894751875aafaa9e41eb65193b307dca343f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cce19a1d3a114ac6d6fcf6e3821a0a14e899522dc6eb134a30a5ca3b5e2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:923c2170b7f18fd31aba29785719797177b679090cc60797a1d630e1f94b9f0b`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 3.8 MB (3812995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281bf66237070f90dbaf4cee151e76c8b8491264ff7f0f7ac8ebce71a5763bbe`  
		Last Modified: Mon, 05 May 2025 17:03:23 GMT  
		Size: 29.3 KB (29259 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java21` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:cfad589b7212ad7adee674f6b957f5a0c28c5936e7f59869dfa9886407609d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663448014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9771174bf81c1c9547fcafb5bda3c27fed1acf537b47565a335e0aaadcf353`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 18 Mar 2025 11:08:35 GMT
ARG RELEASE
# Tue, 18 Mar 2025 11:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Mar 2025 11:08:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Mar 2025 11:08:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Mar 2025 11:08:35 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Tue, 18 Mar 2025 11:08:35 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:08:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Mar 2025 11:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 11:08:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV GOSU_VERSION=1.11
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.0.0/flink-2.0.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.0.0/flink-2.0.0-bin-scala_2.12.tgz.asc GPG_KEY=F8E419AA0B60C28879E876859DFF40967ABFC5A4 CHECK_GPG=true
# Tue, 18 Mar 2025 11:08:35 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 18 Mar 2025 11:08:35 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 11:08:35 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
WORKDIR /opt/flink
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 11:08:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 11:08:35 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 18 Mar 2025 11:08:35 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc2e83745f5161ac5876e1e145987a65feb3f11b8d6957c1e6011f3cb9d42a8`  
		Last Modified: Mon, 05 May 2025 16:58:07 GMT  
		Size: 52.1 MB (52070754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac615b4401d254f31aceacac2a102ab32b6eee92e74b4df225dd7d441c7adf2e`  
		Last Modified: Mon, 05 May 2025 16:58:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e772fc7223005edf5117652fbb5f4ba65fad1fa4035b6b61068823847fdfbc`  
		Last Modified: Mon, 05 May 2025 16:58:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2fe5deba99824c3131336c8dfc53f7d1cbab51fa68a2cb7819002ebac17a1`  
		Last Modified: Mon, 05 May 2025 20:46:58 GMT  
		Size: 1.0 MB (1041831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8673682e9134b2c952afc2cc5a6053dfb4e133c6889eda32e40940d3e85942fb`  
		Last Modified: Mon, 05 May 2025 20:46:58 GMT  
		Size: 835.4 KB (835385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80437e13fedb49e259f055a9568cf83fbe4702cf2d4f6f7df91426cb16f41b7b`  
		Last Modified: Mon, 05 May 2025 20:46:58 GMT  
		Size: 4.6 KB (4633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde2825f0c4d9d3dd53e1831fa1b6839a87b5afba65cce96b42a2015adb2616b`  
		Last Modified: Mon, 05 May 2025 20:46:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e11ba942b3fc93c6e21ac6b0d1a65bdd11a055bc6ecf4d0e1763d0cb283ed`  
		Last Modified: Mon, 05 May 2025 20:47:10 GMT  
		Size: 566.1 MB (566076770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d0e46fd47bf33618ef5d00e7a20b2c4e092b6b134168639e1e0ff4569c9f3`  
		Last Modified: Mon, 05 May 2025 20:46:59 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java21` - unknown; unknown

```console
$ docker pull flink@sha256:c24410ea31414e50239f1c38bb7c9912a9e07f8e5052c6bdd482cc3b0848d9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f236b0d2a5d477240034a233bd2af84f6506d0a7ddfce6803c94f815dcde774`

```dockerfile
```

-	Layers:
	-	`sha256:6e303a30e4f1825b825241118b950f2e6b26dffbdf0c9d8c89fce470fc18103a`  
		Last Modified: Mon, 05 May 2025 20:46:58 GMT  
		Size: 3.8 MB (3812704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6298113f39a7df2a794f1d932fa2f32a47e274728503ad3c7bf33d0b7b07d0`  
		Last Modified: Mon, 05 May 2025 20:46:57 GMT  
		Size: 29.4 KB (29432 bytes)  
		MIME: application/vnd.in-toto+json
