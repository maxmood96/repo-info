## `flink:java11`

```console
$ docker pull flink@sha256:197a2bc857fe778d18da9452943bbf315fad2fac1c466b9e5446a06dd038d102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:43d43f0de40d35b0a6e429db25f150d8b891996f7014f0964136c7857dfa857e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.1 MB (661058117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c95c05af56c42fface87e2888e4f05e40f18ca4953491432f38f0b320275a4`
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbf9d38b8963870654889412ae6385de1e2058c079b2eae676102b6122b7278`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 16.1 MB (16146121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6054288259a06dc634ffb704b64774ea7817cdba3b2639503f8282cf065645`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 47.2 MB (47222883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6153ab12dae90f103d2870b399994c4d18def38e451dda4d458cf39426c527`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe33075ab966c12aac41547c30551bd04dc68a304472fde873e2e12e6dc4b9`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b54c9de4c0cd83550cc789f8e1edc44cfd15223f55592996125255465cc84f`  
		Last Modified: Mon, 05 May 2025 17:04:35 GMT  
		Size: 1.2 MB (1169786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5c19f4a8147bdeed2f6725717f3900a752b96f7ab21657d734b7cc4c1e671`  
		Last Modified: Mon, 05 May 2025 17:04:34 GMT  
		Size: 900.5 KB (900497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02176f30a4a30aa92f8dfc7330f647c4b7e262b0e4c62bd27bbaff4b8a75828f`  
		Last Modified: Mon, 05 May 2025 17:04:34 GMT  
		Size: 4.6 KB (4595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a89dbe860157025d3ebd7549aa64a52e8fe38514eb2776ad89ee460f38e14`  
		Last Modified: Mon, 05 May 2025 17:04:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a24e046405f4993f20f3b3372ea352c6ff34503e340986567a564d77821f07b`  
		Last Modified: Mon, 05 May 2025 17:04:45 GMT  
		Size: 566.1 MB (566076799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6115b201235952fc7e1e5bc3a66f3e25b6ff6801c188a4e8e4d1caec33aee964`  
		Last Modified: Mon, 05 May 2025 17:04:35 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:84e04e5c1db8641b2bb96b44499f4f3ce6412e0c88c663acd319cebd8e85ed85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4b0a69bf634f1313fa145aa238a7f2827e571cbf77d603612dd64f9acbd2f3`

```dockerfile
```

-	Layers:
	-	`sha256:38461561d8cc17e0ec20ce0e27424e32bafd7f39388b920075018d3310ef5b42`  
		Last Modified: Mon, 05 May 2025 17:04:35 GMT  
		Size: 3.8 MB (3823611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01301cff22c5c6bd5e5dc9aa4c79b7a44d9902b73c295a204b0844a68cc8400c`  
		Last Modified: Mon, 05 May 2025 17:04:34 GMT  
		Size: 29.3 KB (29263 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:5705cf1b1b83dae6b57097ef870ddefbb9489135ff5842de9da26696375dbf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.0 MB (656962368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bb9628968e10046fd4fde36b06a71535ab0dd46a7bdc3c89412bd95a5f5c86`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a9ccad43d6175df33a31d9ef705aee0a7e79c37234a6583a2c9f97ff08f56`  
		Last Modified: Wed, 23 Apr 2025 16:34:15 GMT  
		Size: 45.6 MB (45585061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752dc0481ce94de9a181f6af59bbde60866f257bef89c202420b0a8617885ca3`  
		Last Modified: Wed, 23 Apr 2025 16:34:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115162747e532e8811a154d137b2281cafe2b8cd2e40d6b91e10d9a9bed48de7`  
		Last Modified: Wed, 23 Apr 2025 16:34:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8352dcedee4651201ff999487d296c2063494ed8452075c59cc2d3d2c6401188`  
		Last Modified: Wed, 23 Apr 2025 17:16:02 GMT  
		Size: 1.0 MB (1041827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773236a465369e22d3ceac0570dcaaa2d36211cf32931da32506c57712d246de`  
		Last Modified: Wed, 23 Apr 2025 17:16:02 GMT  
		Size: 835.4 KB (835385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967b3df016ece80290fdf7feb16961b716f5efbf8e4927901700d7373837d5c`  
		Last Modified: Wed, 23 Apr 2025 17:16:02 GMT  
		Size: 4.6 KB (4635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f4d9a7e9a14224280a3dbeb21b025f8d8a57186a74b5203a3e18f8c1fc084`  
		Last Modified: Wed, 23 Apr 2025 17:16:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27b87d61a7d18595e56ff7d925250c3c0722c5e6914bdb593efa588510c90de`  
		Last Modified: Wed, 23 Apr 2025 17:16:16 GMT  
		Size: 566.1 MB (566076842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc237b41f1e6e812b950aca9fd34e5870280e9c0a8af50f3e3cab1df2231c1b8`  
		Last Modified: Wed, 23 Apr 2025 17:16:03 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:ad9678995cbc9b6fdebef65c585ea098c81dc123981c6956958b98cfdbae0a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354449fc16f1185c047833078915c8754fe89b58e5b1ce8ee68afd566748869c`

```dockerfile
```

-	Layers:
	-	`sha256:9ae54ed5e78f5a2abb5d9bb9e7ceedf401c3cf5d3f90ee0b9ef911eaca121564`  
		Last Modified: Wed, 23 Apr 2025 17:16:03 GMT  
		Size: 3.8 MB (3823938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cbdc9428fc8b15b9eedddd71f2af16ce844fb7aabc72033b4c89d483aa305e`  
		Last Modified: Wed, 23 Apr 2025 17:16:02 GMT  
		Size: 29.4 KB (29436 bytes)  
		MIME: application/vnd.in-toto+json
