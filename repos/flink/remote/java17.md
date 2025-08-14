## `flink:java17`

```console
$ docker pull flink@sha256:fe89bd5869bb13c4771dbc1b451b4b5686361d3743403fa9b592d33fcf043b98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java17` - linux; amd64

```console
$ docker pull flink@sha256:13876a4355015fb5a4a476ad3b38c64e027b369d10076103675b4ff696ab7ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.2 MB (660152821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8ebece44b3dc6200126d86cd79b2b2e42728a67ae3d7640b37b266e3ba2f1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 29 Jul 2025 11:47:15 GMT
ARG RELEASE
# Tue, 29 Jul 2025 11:47:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 29 Jul 2025 11:47:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 29 Jul 2025 11:47:15 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 29 Jul 2025 11:47:15 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 29 Jul 2025 11:47:15 GMT
CMD ["/bin/bash"]
# Tue, 29 Jul 2025 11:47:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Jul 2025 11:47:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jul 2025 11:47:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.1.0/flink-2.1.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.1.0/flink-2.1.0-bin-scala_2.12.tgz.asc GPG_KEY=7A14EF9AD986EF0D56B2E73F6AF817E6C59EC690 CHECK_GPG=true
# Tue, 29 Jul 2025 11:47:15 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 29 Jul 2025 11:47:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jul 2025 11:47:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
WORKDIR /opt/flink
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:47:15 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 29 Jul 2025 11:47:15 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670547904903aa6ce1e0f44562e27d151d319243c129b927d7c8515ecb66c07`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 16.2 MB (16150701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6898721bb2fa374368fa1fca91e491a141b71400687bfd48a9b159bb585eac3f`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 47.0 MB (46986154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28927af8b0bd97d0ded0af3f583daa8c97528ed8958c8b7ff00e46565ab99ff`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0543ed4affc53446f4fff9e9d582c304542c3ab4422b57c3c7af62779c6f84`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2785d451a18a0c62074f6a7077418088b2489a4ef5548e973a74e425a0adab`  
		Last Modified: Tue, 12 Aug 2025 18:39:50 GMT  
		Size: 1.2 MB (1169599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511a9d4bd7dbbe438038b6224de55ca3cd55f0c8cd6ce6035988ec9d8766f7d`  
		Last Modified: Tue, 12 Aug 2025 18:39:52 GMT  
		Size: 900.5 KB (900494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efc0c47cddce6fbfc5708b8524022578ac97655401089c0f01b03258b554944`  
		Last Modified: Tue, 12 Aug 2025 18:39:51 GMT  
		Size: 4.6 KB (4592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e59fc703c8b60c2cba1abdf5731981f1d562cca457ee79660125dbf5120ebb1`  
		Last Modified: Tue, 12 Aug 2025 17:53:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25350d7b23f3df28b9d635457ca148f150515c2bb0711721c683f9db6826827`  
		Last Modified: Tue, 12 Aug 2025 19:04:23 GMT  
		Size: 565.4 MB (565399467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0061ec297011068b79ba5e88bff42e4869e94e9030664348b5144762be913a5c`  
		Last Modified: Tue, 12 Aug 2025 18:44:27 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:504ef8185d144b8eae673c2d73d14298af836b0be650288e975c3c20fe27b83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd367c2f4d107d3b7c20bad8f1aa372910c0241afeed38bb0a9c38f821fa0481`

```dockerfile
```

-	Layers:
	-	`sha256:24e5841aba747aa21b11083e4abdb8f38971991c8670b430b6ff29a8eaa92448`  
		Last Modified: Tue, 12 Aug 2025 19:01:32 GMT  
		Size: 4.0 MB (3988434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bb9bf2f8f6dc06dd3fa7044ed8b4ed05b18a2ab1ca69307429432888505df3`  
		Last Modified: Tue, 12 Aug 2025 19:01:33 GMT  
		Size: 31.1 KB (31075 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java17` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:5efbdb9cf3c0fe02bc82181c1d9571347e234ddb539665005178726b4bb2a900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.2 MB (657190708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121a1a1c99d1676b22437fe1d19650ba59e3fd560e22bd6a77b585d4a91646c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 29 Jul 2025 11:47:15 GMT
ARG RELEASE
# Tue, 29 Jul 2025 11:47:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 29 Jul 2025 11:47:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 29 Jul 2025 11:47:15 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 29 Jul 2025 11:47:15 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 29 Jul 2025 11:47:15 GMT
CMD ["/bin/bash"]
# Tue, 29 Jul 2025 11:47:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Jul 2025 11:47:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jul 2025 11:47:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV GOSU_VERSION=1.11
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.1.0/flink-2.1.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.1.0/flink-2.1.0-bin-scala_2.12.tgz.asc GPG_KEY=7A14EF9AD986EF0D56B2E73F6AF817E6C59EC690 CHECK_GPG=true
# Tue, 29 Jul 2025 11:47:15 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 29 Jul 2025 11:47:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jul 2025 11:47:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
WORKDIR /opt/flink
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Jul 2025 11:47:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:47:15 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 29 Jul 2025 11:47:15 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199b54d0379497df50867982d570bbd000004bfbf27017cd65c6f9eab785cc29`  
		Last Modified: Tue, 12 Aug 2025 18:37:19 GMT  
		Size: 46.5 MB (46481606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab45f69caeebdcfc0dcab7f12f318e6a8722b5101f1bf4043e99c86a6fbd7894`  
		Last Modified: Tue, 12 Aug 2025 18:37:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c74bc8d670c7b95bbe286937b0313a59d6ab9dd2b022249a7391012ef0a5da`  
		Last Modified: Tue, 12 Aug 2025 18:37:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23abf6da9673def47fa117171c9740a0e183a30aedcd50fdeca538dde27ca71`  
		Last Modified: Tue, 12 Aug 2025 22:22:55 GMT  
		Size: 1.0 MB (1041816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c43c0b999f6b0a8aaed94d6fc1dfa2595071ce1f54dedf9c3dd27c8de548`  
		Last Modified: Tue, 12 Aug 2025 22:22:54 GMT  
		Size: 835.4 KB (835381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7cb457dcb77f65a0a1f02b8b4630b858fcc79db6f448e66c4bfcb78017aa4a`  
		Last Modified: Tue, 12 Aug 2025 22:22:52 GMT  
		Size: 4.6 KB (4626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194b25ae1f587a6edd2369bd6e750f49e9a2f4e3ab1e1a1dd874df1a1392d42c`  
		Last Modified: Tue, 12 Aug 2025 22:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aa6963f311080b9321b6a21df495181a2fffa05691444b77b181791e7fdf18`  
		Last Modified: Wed, 13 Aug 2025 02:33:15 GMT  
		Size: 565.4 MB (565399470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad4472dd4f295d26a0d1eb9f5d2d643abda1346120f9868f270bbad8204880b`  
		Last Modified: Tue, 12 Aug 2025 22:22:53 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:91950866be943d62050d6e83d199251caa86e6407adf869d2e7152b5dc7c70f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7986c841cc28e83397c11a3694e50571d974a09159b3b6cb2f46f12b68a0d591`

```dockerfile
```

-	Layers:
	-	`sha256:209ea5da0b938d0d7e8c031185524b73d8ba466a79916fa7dc2a02024e5e821a`  
		Last Modified: Wed, 13 Aug 2025 01:01:45 GMT  
		Size: 4.0 MB (3988215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc3741bc4a4a8dc0e6fc0007155d64ea7172702ca286d77427ab09c99cd65d8`  
		Last Modified: Wed, 13 Aug 2025 01:01:46 GMT  
		Size: 31.3 KB (31320 bytes)  
		MIME: application/vnd.in-toto+json
