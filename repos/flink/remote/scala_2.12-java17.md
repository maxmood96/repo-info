## `flink:scala_2.12-java17`

```console
$ docker pull flink@sha256:b46dcc4c70cde81859ef0daa2210a4c2f7bb3f96eb0fee5c9a1229f95176551e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java17` - linux; amd64

```console
$ docker pull flink@sha256:c91fe6e5bd049be5e53fe55c06e0cf0f7a0f92d5d42945ac5fd64ca6b1935178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.4 MB (578360034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4622e01227b033be870eba8e59f17f016b37235c80021c3cff877109f4c64bfb`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 08:00:24 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 07:44:36 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 07:29:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 07:22:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11d7deee5b938b87695c41d3ddfb436c01c634941786752462bbc561f79931`  
		Last Modified: Tue, 04 Feb 2025 09:03:18 GMT  
		Size: 1.2 MB (1169612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c5a7c6e086e3e96d3d132d4700a217d993f0f212de544f621a6e293b18d42`  
		Last Modified: Tue, 04 Feb 2025 11:28:09 GMT  
		Size: 900.5 KB (900494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f97ac9a9b4c7ed4df6f7859e5da969cba3d2c12f13decf93f4edb9f980a540`  
		Last Modified: Tue, 04 Feb 2025 11:39:39 GMT  
		Size: 4.6 KB (4591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8da476e892f85832c33ce801c6aff6e08dd0d2b052110629e348e56b7e37a1`  
		Last Modified: Tue, 04 Feb 2025 11:49:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275f47d6861fd689a55c42866f21fc1e1c80f921b51c821a8b1960876e19f55`  
		Last Modified: Tue, 04 Feb 2025 14:21:51 GMT  
		Size: 483.7 MB (483656755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77c3b37df2e400a290c9d09f1d5ebc42b4fe13e83a7555cac61e6f675a875e5`  
		Last Modified: Tue, 04 Feb 2025 10:20:02 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java17` - unknown; unknown

```console
$ docker pull flink@sha256:71318f55357a76377d4eddf2e0e3772a7681af4eb585d364c00344e6f7841b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599843077686002b670fa711b3daa8d017aa1dda13eeaf287b5f915791de7fc6`

```dockerfile
```

-	Layers:
	-	`sha256:6d52bebe2dbbd1073c2b452e583ea05b66cf2a432786cb7d2fb509e1f3224b57`  
		Last Modified: Sat, 08 Feb 2025 02:48:51 GMT  
		Size: 3.8 MB (3819023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c28fbe88aca65a4643c7527ddf7d381a2c8aa9fa379e4c070e4b411c7af16d4`  
		Last Modified: Sat, 08 Feb 2025 02:48:57 GMT  
		Size: 31.0 KB (30969 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java17` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:5ab2fea0f3434fbc94fe279f3a06cf343e46fc344c17968dd3b9b79e33f1e11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.4 MB (575417633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06425fa1dff31798cfb6d9b2ee1fc98e44284c2cdf4c69320d763c7372e82ab`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 01 Aug 2024 06:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 11:06:23 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 13:23:17 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 13:40:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 13:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8712b52da0b93bcbbc10498ddd2cfe4218064945d9151f133c1e94f23c0b9f`  
		Last Modified: Wed, 05 Feb 2025 01:04:47 GMT  
		Size: 1.0 MB (1041615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114472e61bfffa46dc225aee219ca93d4a0eba59a6270d51cd48f5f81b768d50`  
		Last Modified: Wed, 05 Feb 2025 03:43:47 GMT  
		Size: 835.4 KB (835383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90acc1e026fc4847e438b1ff6f81b4ddf063f3186ff22a187b6a2073e7dff2d`  
		Last Modified: Wed, 05 Feb 2025 02:38:18 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68906f1758b209c675e315217004bf3bb1167098b2790e3b47d441d5a955b693`  
		Last Modified: Wed, 05 Feb 2025 07:46:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37c468c35a4e870b14d7e0b1e2d77795ffed29fff89ed6d937d3f1af8479704`  
		Last Modified: Wed, 05 Feb 2025 01:05:21 GMT  
		Size: 483.7 MB (483656793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ab5a4ddb2ab2270fe1bea675ec27ae4422b913b333eddcd75cbb51a8a0a4ae`  
		Last Modified: Wed, 05 Feb 2025 03:43:42 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java17` - unknown; unknown

```console
$ docker pull flink@sha256:17b7fa06b6f7364834368d1b848c71d4203b7eeb98334dec2a6439983d054338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a4f4dc1b71b012c3c0689ad618a608565bc0f795928e93add7499186210ca2`

```dockerfile
```

-	Layers:
	-	`sha256:63062cf2b391cee9de5ec9d9d22acb79c0fac9a0c59fe85b249ac59ea0588806`  
		Last Modified: Sat, 08 Feb 2025 02:51:25 GMT  
		Size: 3.8 MB (3818732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625d3f4de98c5479ddf8ba9b7bf259e0d8b5c82b7246751b313ff45d4b0e1be5`  
		Last Modified: Sat, 08 Feb 2025 02:51:31 GMT  
		Size: 31.1 KB (31145 bytes)  
		MIME: application/vnd.in-toto+json
