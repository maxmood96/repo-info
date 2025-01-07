## `flink:latest`

```console
$ docker pull flink@sha256:2ec7f6d5591444334f63b66ddd49c7ae02551cb0a27c0988790fa43caa49716f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:latest` - linux; amd64

```console
$ docker pull flink@sha256:bae6cc6e2a5e1d79dde6cd6fb8d5c4a63a8840aaa3499d4c9834c721b4911585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578630615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dc91b683b6b4ced973f192fc83fc3b8e7ad7d81b84bf424493b4016a1585c3`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:2c9f253e30bf10597ab51cfeae198ac65b228e577750e871c097150cc79a060d`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 16.1 MB (16142360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8233e39bf60fa5622425c07f933fcf0d9b21271c01769cecb8142d19a6d3c`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 47.2 MB (47216714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59d22db63f3eb3d77e5b705449730b93d844bcfa1ce1f13df22d49f13d15606`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80a9c727cee83bf408beb00d113d06d03954eb063419370a72b7844400e2d79`  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3337ead35a37e6996a7f099b1e6baa0432994ffc5e7cbaf9d5a707d78c1844`  
		Last Modified: Thu, 24 Oct 2024 01:55:17 GMT  
		Size: 1.2 MB (1169212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e543b721f946a7895a4dfae9b5b67adc2bb12b23bd3d481b7b98989d4a164b`  
		Last Modified: Thu, 24 Oct 2024 01:55:17 GMT  
		Size: 900.5 KB (900497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecebf073acfbb667d472e3ca96be3953e60083c19f383c1392ff45ab71f8ce6e`  
		Size: 4.6 KB (4594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21be4ec8974253b1750f12130c6716acceabbe5b6a1d777e1ba1b1f44f78a072`  
		Last Modified: Thu, 24 Oct 2024 01:55:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71629a01e27f83bedf44ea26f109c3d5e24ff185e716153791d6daead769908`  
		Last Modified: Thu, 24 Oct 2024 01:55:28 GMT  
		Size: 483.7 MB (483656730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f5f48c9f11e33845989303be9f4f1122f604abd76f19a57d05b7778bd1780`  
		Last Modified: Thu, 24 Oct 2024 01:55:18 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:latest` - unknown; unknown

```console
$ docker pull flink@sha256:e1a8459170e473f2380e5c302ac1ccb77c9ae24932b22bb97a41282c27c28fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3872348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fa2259216831482ed0f03ef0c5570d1fe7ef4efc044487301e695c79fe9fcd`

```dockerfile
```

-	Layers:
	-	`sha256:1264156bbd9cf498cd8d98ce0e240c7fa7aff6cf8300022c3a81cef9e18ff018`  
		Last Modified: Thu, 24 Oct 2024 01:55:17 GMT  
		Size: 3.8 MB (3839557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44203b1282078d5a8ad008afda08f261c4f2e5d1903e150d7eaa8b37f1e2182`  
		Size: 32.8 KB (32791 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:latest` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:b034a33049a0b122f7ef9e408587bac408313e18443f5cf620e31e344b108b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.5 MB (574540137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56a560e4c8a813a17d815c1a08202e6ad3797ca9863f9723d600508fa59ef98`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4b49837842cfab8a95fec666778763869dffc44881af662c920632ae031b5`  
		Last Modified: Thu, 24 Oct 2024 01:06:21 GMT  
		Size: 45.6 MB (45576593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ec09f4527c9ff858afbd6c055995c0e8a4d9d97ea97cf12b1b94149cf94c9d`  
		Last Modified: Thu, 24 Oct 2024 01:06:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d5bbc6a56336b0b3fcb22659e14fab1d3b2fdc016b66655dcb9b28a075bb68`  
		Last Modified: Thu, 24 Oct 2024 01:06:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a972ff5f0ec4445379dafd0a48cdc46f1f647c8198fec20b9cff96597837db81`  
		Last Modified: Thu, 24 Oct 2024 01:59:37 GMT  
		Size: 1.0 MB (1041497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8238a91b28f4b912e9aba8fae5ef500d8e01f340e81e6fa42cbf427a2f7a30`  
		Last Modified: Thu, 24 Oct 2024 01:59:37 GMT  
		Size: 835.4 KB (835383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1982fc3170489edc4c49f99bc1f45c7c8a9ee6880f54f9a2f29bef2baa4ee38a`  
		Last Modified: Thu, 24 Oct 2024 02:07:26 GMT  
		Size: 4.6 KB (4632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b939a8516ca7a56763039fe0f03db2ea269160fa25c22e49a0428031137706d`  
		Last Modified: Thu, 24 Oct 2024 02:07:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ff77ce2031467e6d4e9c53de3d87c4ed7c79fb01b039d819042a834a7d5525`  
		Last Modified: Thu, 24 Oct 2024 02:07:37 GMT  
		Size: 483.7 MB (483656755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e5588cf2ed4144e5e691e84a726036773ba1d7840fdb87987992a81f92610`  
		Last Modified: Thu, 24 Oct 2024 02:07:26 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:latest` - unknown; unknown

```console
$ docker pull flink@sha256:42560450e326ee1da714ae8fceb0ae27882024c2df87cb376bfd62d6fe0166f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3872992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d754e24156e60ad2c502136205aee1e731f26a283302e4d5fd034d80a3e37cce`

```dockerfile
```

-	Layers:
	-	`sha256:ce82f8bbfea2188c9ad323f63495e321f9a9babe78855bb6009e84f9f2f91875`  
		Last Modified: Thu, 24 Oct 2024 02:07:26 GMT  
		Size: 3.8 MB (3839955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43750286ec201d85a16e43ae59bff75c263d36a2550bad4ef637bf98ab78b04`  
		Last Modified: Thu, 24 Oct 2024 02:07:25 GMT  
		Size: 33.0 KB (33037 bytes)  
		MIME: application/vnd.in-toto+json
