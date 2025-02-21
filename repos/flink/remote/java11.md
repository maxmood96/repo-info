## `flink:java11`

```console
$ docker pull flink@sha256:ba5d23bfc3e0e5c31d6304827ea4a10942a074aa0c8d8d27f3cea97bb3fb5dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:67da855c2a4b098b1013e6ccb50dbd0c751cbb0548e2f711e525bb9833146fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.6 MB (577572577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ad748ac6a725f92ce9c6f2de3a6445e49abb6ad6e70fff116b41011daf32e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENV GOSU_VERSION=1.11
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.20.1/flink-1.20.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.20.1/flink-1.20.1-bin-scala_2.12.tgz.asc GPG_KEY=5575E80D59BBB73C15A479B88C1FC56D16B0029D CHECK_GPG=true
# Thu, 13 Feb 2025 13:14:49 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 13 Feb 2025 13:14:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 13:14:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
WORKDIR /opt/flink
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 13:14:49 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 13 Feb 2025 13:14:49 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2218709e815fb56b0b64c187c009b0c907a7935bc70e1133db22c79cd58e71ee`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 16.1 MB (16135155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7988bfb5529fb85284fe5b1b20470912746d60c808fa72d6854fa5e964a4753`  
		Last Modified: Tue, 04 Feb 2025 04:39:14 GMT  
		Size: 47.2 MB (47216614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854889cc3907acabb01aa052b8f112d7bdff0b071fd1b8ab2cdccc59b516167`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf2a4e8b353be69b442f45259691d65ef85a8dd97c02a339a0e128f05088536`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01aa2d991929497b6cfa96a6ac82b193f5f072b9888b949c24df3327e408959a`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 1.2 MB (1169621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea7dd3efa48b9dce491b84961248908129dc7c2813b8d8dc48a3678c13b317c`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 900.5 KB (900495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd92cde96d95346159cc709b05845833c708d4b33ec734799126aabd327a9fad`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 4.6 KB (4592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d790f3e4b4248a33a464b3b791fc641c7a775418235a5f03da1d52931f260fa2`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56792b352ae8cf0e157a479f7fc86630296ab1d8f64782d4dcc517d0a23c0cc`  
		Last Modified: Tue, 18 Feb 2025 19:31:43 GMT  
		Size: 482.6 MB (482605337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1b4d8d5ed2eac3ee9a00cad95bea02c5dd89f321e9f27de52326ef00d2e6c`  
		Last Modified: Tue, 18 Feb 2025 19:31:37 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:fc0a6d0b206991b08f954c47f15dfabf634c8c03b9dfebea0376f0a6d8246f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049b721e1d90364c3f4061e31de8d5082e00fd086e2834c894a742fc993322fc`

```dockerfile
```

-	Layers:
	-	`sha256:9562b80a6374538202114fe7b10b20c3e3d918649d8daaa2c03b705af2708616`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 3.8 MB (3833957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501ea08c7658438908087d2d390e3ee5886fbcaa982676fe78947daaf1ef5300`  
		Last Modified: Tue, 18 Feb 2025 19:31:36 GMT  
		Size: 32.8 KB (32792 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f5f67867826d9cef076b91da9ee3f7ea24f097043bf3462911f642e6765eaa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573478589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1f6f62079a7bd3ac864115a6c00c4c5b51ca1fbf8790ed3f02e4e46dd24041`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENV GOSU_VERSION=1.11
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-1.20.1/flink-1.20.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-1.20.1/flink-1.20.1-bin-scala_2.12.tgz.asc GPG_KEY=5575E80D59BBB73C15A479B88C1FC56D16B0029D CHECK_GPG=true
# Thu, 13 Feb 2025 13:14:49 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 13 Feb 2025 13:14:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 13:14:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
WORKDIR /opt/flink
# Thu, 13 Feb 2025 13:14:49 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="$FLINK_HOME/conf/flink-conf.yaml";   if [ ! -e "$FLINK_HOME/conf/flink-conf.yaml" ]; then     CONF_FILE="${FLINK_HOME}/conf/config.yaml";     /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"         "-repKV" "rest.address,localhost,0.0.0.0"         "-repKV" "rest.bind-address,localhost,0.0.0.0"         "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"         "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"         "-rmKV" "taskmanager.host=localhost";   else     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' "$CONF_FILE";     sed -i '/taskmanager.host: localhost/d' "$CONF_FILE";   fi; # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 13:14:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 13:14:49 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 13 Feb 2025 13:14:49 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a52ffb175ad1dcd8d364fe67acb246aab94c398d959d8d166ec5f141d4b8c3`  
		Last Modified: Tue, 04 Feb 2025 09:20:15 GMT  
		Size: 45.6 MB (45575892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad623ccfcd77de0cc124fb4db0bf8ddd65fab1fd731cc5749533bcc9d6d9806e`  
		Last Modified: Tue, 04 Feb 2025 09:20:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb340c54cb7dc17dcd4b8bee473c99474a4ffcb686470f5d4866eba12637ff4`  
		Last Modified: Tue, 04 Feb 2025 09:20:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaa22e1bddb8ffa672cf1fe841bdecfe2f96038cc7a84c513128060aa1772e4`  
		Last Modified: Tue, 18 Feb 2025 19:37:11 GMT  
		Size: 1.0 MB (1041688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2edc0d72f495141b132c86bc77a2130966983c2986fbcf5b73865def6a7f9a`  
		Last Modified: Tue, 18 Feb 2025 19:37:11 GMT  
		Size: 835.4 KB (835382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb78125f0dd8fe493d1b83c86610552871de6e403b61902fb6211babf9e25e1`  
		Last Modified: Tue, 18 Feb 2025 19:37:11 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b080ec53f6952451a740ad5156c310473a778922e754ac2ed3f766dc9ba0476`  
		Last Modified: Tue, 18 Feb 2025 19:37:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619567efdc0cea74cb581736b6a2beaeffb1769bf59bfc51c326cd084d1d7d89`  
		Last Modified: Tue, 18 Feb 2025 19:37:22 GMT  
		Size: 482.6 MB (482605347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0842a78b90e996b14bac8ba513be5828639bf8ed02519ed72df478dc7ddff863`  
		Last Modified: Tue, 18 Feb 2025 19:37:12 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:82917e26663bc2c45f3f7e4710db7d36abf958454efe9a7c829c5163cd322ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ed161028fc4f188b4e550a21c80e566d125fd770972b1fe0ae5bec225d1b6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf99c3d7227191989938879d678cf27115001c3b6f4d39ce2c43c606852553ed`  
		Last Modified: Tue, 18 Feb 2025 19:37:11 GMT  
		Size: 3.8 MB (3834356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77740f835a22aa6f2f71ae4e3a01af7981e36f1fbc9cb7c588e3dbbedb7d4f2d`  
		Last Modified: Tue, 18 Feb 2025 19:37:10 GMT  
		Size: 33.0 KB (33036 bytes)  
		MIME: application/vnd.in-toto+json
