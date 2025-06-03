## `flink:java11`

```console
$ docker pull flink@sha256:f3d77461a31d08f2a82c4d7a95653c8ee6cf39e3eb86830b3553ee5d66213cc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:cac048881d6d8ebd4564a4fb5e1803ee2843029fa193377f6e9b7107a14254b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.1 MB (661058353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85d2b9c3ed035ab7512c46dc18bd0c7d87929ecbf1c04b9a8a7c57e7bc4eaea`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42b19062e0bc641a46e34df78df73631446721b333c7b88f4c9d5503d3064e1`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 16.1 MB (16146391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd36994d61a14a97e81fa0ba8d11ad2a81a89dbc17cc5cb600c774ea66c17807`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 47.2 MB (47222562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3f7338f8013bc923d626833da378f498b67cb62a18956e09fe43da7df2f4e`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95f7c712ff3bb67001daeb6b5a7a047e263936db7afadc0b453823392afb78e`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39e9acc8048156bb5c11ddc2c7d58fb3ce558ee5a0639061f82dd8a2d25dbe2`  
		Last Modified: Tue, 03 Jun 2025 14:59:46 GMT  
		Size: 1.2 MB (1169669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a51f655547b608e3d7e094208754af9af90a09010882d1a5443e0443f7f37b`  
		Last Modified: Tue, 03 Jun 2025 14:59:44 GMT  
		Size: 900.5 KB (900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94ed2fe68f61625b8e94e6ee589780551745e98968cd0d6fb12f2f67febabe4`  
		Last Modified: Tue, 03 Jun 2025 14:59:42 GMT  
		Size: 4.6 KB (4585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cde2578beeedae168d154d356f8688f957efbe66d3eb7ab4dc02880fbcc787`  
		Last Modified: Tue, 03 Jun 2025 14:59:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0235f35125f2bde14997d6316288338daad0bd2baa30c7507ae79e11c1fb12`  
		Last Modified: Tue, 03 Jun 2025 14:58:56 GMT  
		Size: 566.1 MB (566076836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb89251a4fa80cb2ad9e99243163b702e93184bf65fc849b4797865116040f67`  
		Last Modified: Tue, 03 Jun 2025 14:58:39 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:6f23aa81321995a392182b753073a897b02cdb7a98408396802393197b067e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb07922c43707459a1a0f984f60995549715ccc6dff637a0bba13f537c663683`

```dockerfile
```

-	Layers:
	-	`sha256:98a93045e078d2fe030157c64b1f612b6f3ba2a309b8aefb780807d55f4ee20d`  
		Last Modified: Tue, 03 Jun 2025 15:24:57 GMT  
		Size: 3.9 MB (3853258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:489d29438261f5bc29b136785045bc2f00c9b47fe904af1bc79182ac3301dcad`  
		Last Modified: Tue, 03 Jun 2025 15:24:57 GMT  
		Size: 29.3 KB (29263 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:6c7d31c3ef96a86f9d7e1d64317e318acd5797d2d5eb4ce0cfbabac8b1311410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.0 MB (656963811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8323b80a0e2d7f8622ccbcb7e8e2c2b1240cd68c9b8cd889aaf3e7c5e6a3be`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 18 Mar 2025 11:08:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7e26e3b7b1fa7347f5fc61494deeb7d8590c6dd8859be548f1af7bee117a6`  
		Last Modified: Tue, 03 Jun 2025 13:37:18 GMT  
		Size: 45.6 MB (45585113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb458c2fb343ac08df2174bebb03229610ede8dd7323589ec018476e303944f`  
		Last Modified: Tue, 03 Jun 2025 13:37:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc4225a392a9d972a86cc8a8f73f5521d7550ea658d20bccae8fed9d8c103df`  
		Last Modified: Tue, 03 Jun 2025 13:37:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d091457ed1e4be9e8788cc72e03241605d288753e512699068682cf363e6f`  
		Last Modified: Tue, 03 Jun 2025 13:44:29 GMT  
		Size: 1.0 MB (1041784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdf4253badcf67d0f4d3bd80a06bac803592268490ff5ef94a5af2fa5c3807b`  
		Last Modified: Tue, 03 Jun 2025 13:44:29 GMT  
		Size: 835.4 KB (835383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335f1acbcba18ee3f19fa37f6084d2d3bc314df6dfbe69ba8ce78819eb0ad3c`  
		Last Modified: Tue, 03 Jun 2025 15:25:02 GMT  
		Size: 4.6 KB (4630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b430c5034c2565f13c495ae6a50bc3327fef00be8ad5d96a64f6abe417feaba1`  
		Last Modified: Tue, 03 Jun 2025 15:25:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e14642bf40eb654d4dc91658f6f2553e38ae81a74458ccd437b5ed2aa0a3`  
		Last Modified: Tue, 03 Jun 2025 15:25:11 GMT  
		Size: 566.1 MB (566076662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336602aa05ae2d10bdabdd1c421165a272678656c93447eb3bb081e78f165b29`  
		Last Modified: Tue, 03 Jun 2025 15:25:04 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:f94e5fed416e9416df880b2fda3f327e21cffa4e4b9e43d85c14730d43d3c9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3883020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7078d7b4772cf7c895a739e84a3daf219748d87819402f89961dc7ca8270b572`

```dockerfile
```

-	Layers:
	-	`sha256:59bd5c7b673f5e4c0645fd1b1f47742d1d787d224f2cad2801b4f2024b9cc878`  
		Last Modified: Tue, 03 Jun 2025 15:25:35 GMT  
		Size: 3.9 MB (3853585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903531a706b051b6bbda61145630fdad61cd894a126ad52fe15399be6636abea`  
		Last Modified: Tue, 03 Jun 2025 15:25:34 GMT  
		Size: 29.4 KB (29435 bytes)  
		MIME: application/vnd.in-toto+json
