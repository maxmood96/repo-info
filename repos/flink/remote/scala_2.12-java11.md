## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:447b9a9ead2b3d26bbf0bc58176bc3cef9a7d9f31d6ce49bb7aba34a07148e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:4306e0705aa16fc5820c7522ff5e42827f22f56dae2949c0bf2d85369d6d693f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579492448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813842380ce6a6e2051359ae4f6aec92d7bf5c5901561f1250b319dd0a16ac59`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de010df86e464633cd8fc0d6653a32c477057f52cdc21db32f42587d4ecf990`  
		Last Modified: Wed, 24 Jul 2024 01:28:31 GMT  
		Size: 47.2 MB (47198401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc617fbf73ced29c867e5e7574eb53b1cd7c424c8bc3094289379b9b8be4be69`  
		Last Modified: Wed, 24 Jul 2024 01:28:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117c654ea9f12f1b410ae28652c6402a174c0c490c97b0a28521083068dbaf34`  
		Last Modified: Thu, 25 Jul 2024 17:29:05 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd179c206f4dd8d7eaad1f7b51a012609d9590eb7aed75887cfc78c9974038b`  
		Last Modified: Fri, 02 Aug 2024 14:33:13 GMT  
		Size: 4.4 MB (4416726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a916617ecdcd608674a7984066c23505579531396ab52e4e9a27f37c80539b57`  
		Last Modified: Fri, 02 Aug 2024 14:33:13 GMT  
		Size: 900.5 KB (900498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c3ba7c191c0d2dbed2dee5cce9856cebcff8c7623475086702fbf82f380018`  
		Last Modified: Fri, 02 Aug 2024 14:33:14 GMT  
		Size: 4.6 KB (4592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894d50404eb5c28f0c23d06af346c49a83d2cead87777c519b7baccbd6f4d93`  
		Last Modified: Fri, 02 Aug 2024 14:33:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56035a87cb4b99f28b80ab69547331d6f8d6f51ceacf0c222ba44bdf73c6e6`  
		Last Modified: Fri, 02 Aug 2024 14:33:22 GMT  
		Size: 483.7 MB (483656892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717974f3798a1699c40d9d7a24afa50571f179cc0cfd99a9f16bf369947c89ff`  
		Last Modified: Fri, 02 Aug 2024 14:33:14 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:9ed5c5d5209ab812664d3a538e1324c7b956b8b4e8980f151e0847cc61decf30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4619cba4889447cc92235554e426a2915be35fb9976dd55a7a379a9fd2dcee`

```dockerfile
```

-	Layers:
	-	`sha256:cbd3a702043069a70217f85fe1a355ab685c2c4d6fd8b1361a506a8bfa2c7247`  
		Last Modified: Fri, 02 Aug 2024 14:33:14 GMT  
		Size: 3.7 MB (3729204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28259594f48a6d95f2212a533f95576555978040999f37da3bb667f9c23aabb9`  
		Last Modified: Fri, 02 Aug 2024 14:33:13 GMT  
		Size: 32.8 KB (32796 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:ccf11bd704567d678b40d94f1334874ee48d3e579924ea3baad6ee565c763cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.5 MB (575537797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fec687d50d0bfa4342da4c21dcaac2c4ef5cb406178b3124de683ec5a37f6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d58831d522892ce028e096d708f4963a33b2dc3b558164d3313f356dabd19d`  
		Last Modified: Wed, 24 Jul 2024 00:51:51 GMT  
		Size: 45.6 MB (45556956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa827b9912bf9e3d5ef6d2883b57eeed2f37a2c5ce1991e48a9d95dd21a9157`  
		Last Modified: Wed, 24 Jul 2024 00:51:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540541fd55f683cce44751b8b0d963a525ce593430a6ab7d691a1a562de60ab9`  
		Last Modified: Thu, 25 Jul 2024 17:45:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98cda28af32f706884a6dc6c18ab849b1b2c85945a1b097abf89e628fc61c58`  
		Last Modified: Thu, 25 Jul 2024 21:41:04 GMT  
		Size: 4.3 MB (4265440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef4ddb89289a6311f7636c929cedc736505d67cd59152debf1ee25e9fcf4318`  
		Last Modified: Thu, 25 Jul 2024 21:41:04 GMT  
		Size: 835.4 KB (835384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3786882990a481f360c8ec2f44fc29ac12598bd44b43e3de516a11aca5510870`  
		Last Modified: Thu, 01 Aug 2024 18:03:43 GMT  
		Size: 4.6 KB (4631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfaf5f5824c7b6366e84fa7af8b25c4bf03dbfabc43af7113c8b2fb800275c3`  
		Last Modified: Thu, 01 Aug 2024 18:03:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d7da066a854919d975baf70d8029d04fd9ebb4be012c3716e0e9839c90e093`  
		Last Modified: Thu, 01 Aug 2024 18:03:55 GMT  
		Size: 483.7 MB (483656882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33789501195e4811044c406515af343a58199739c4409d9ab199413533383f66`  
		Last Modified: Thu, 01 Aug 2024 18:03:44 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:11c00e7d69f02f1d423f6849c7cdddc379d9b0b0a17fe77d6ec454d0fa8d30e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12bec76f496d65702ac4047385dbe415b5cd91261279a3da369b4af40d44708`

```dockerfile
```

-	Layers:
	-	`sha256:970fd608f8eba54f4846a5c5d689f8472d729ad93907270a2e18dd53f54be6e7`  
		Last Modified: Thu, 01 Aug 2024 18:03:44 GMT  
		Size: 3.7 MB (3729602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bde849fa712e2d5ddf5a30b1a58a115ee69a5b432ba34e06aea67ab1893e42`  
		Last Modified: Thu, 01 Aug 2024 18:03:43 GMT  
		Size: 33.2 KB (33209 bytes)  
		MIME: application/vnd.in-toto+json
