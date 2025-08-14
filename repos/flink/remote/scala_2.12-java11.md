## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:2e1abd1d99403b2a239bf526f1f5843cead49550a80517bd7fb44eea8a34f934
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:df1a25e868ea323133cd797d2a9e57da07cbe62f8b3930c6a8c102564d34d2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.4 MB (660401346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eafc3122c4a96b76f93d5022c1163765472ef91c40b8f6aa1edb52ed745a52b`
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:3861a77366b693d4c06f138e0d1897b45b6e08b0725d254b5c37dfd8b7d0e745`  
		Last Modified: Tue, 12 Aug 2025 17:24:39 GMT  
		Size: 16.2 MB (16150669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfa48bc888ed2c1c68d0dec5fc78a8ae6ad637014bad153113aeb43dfb564c`  
		Last Modified: Tue, 12 Aug 2025 17:24:41 GMT  
		Size: 47.2 MB (47234680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec2e28e23d1891406a966a928e4e4f1ef8be15efa0a12edaf237607616a0ef8`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0543ed4affc53446f4fff9e9d582c304542c3ab4422b57c3c7af62779c6f84`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1db410c7d814489611874886b03d7c67e1e853a105c8b9983f74b55b1fdaa21`  
		Last Modified: Tue, 12 Aug 2025 19:21:14 GMT  
		Size: 1.2 MB (1169611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d2ca9e01609a5f696e6a4b467c0e2aaacb11a73a348c8102364cfbcc0babd7`  
		Last Modified: Tue, 12 Aug 2025 19:21:13 GMT  
		Size: 900.5 KB (900494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7e954cd5c5442ca0d72748f7ba3da5741e85763e98adee5f46265b17ebca7`  
		Last Modified: Tue, 12 Aug 2025 19:21:13 GMT  
		Size: 4.6 KB (4591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db50a1eaaba4ce86cb294866747e3593d40469da5b064ed01f3cb9005514d5c`  
		Last Modified: Tue, 12 Aug 2025 19:21:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ad2125a0424e74c5a8a36dcaae68be90973354d241203aa2bb93dc4476da3`  
		Last Modified: Wed, 13 Aug 2025 02:25:58 GMT  
		Size: 565.4 MB (565399487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0767f1f4d65b3f14b087c959e197c5858541baebe2c8c0be4c3d62249a17f9`  
		Last Modified: Tue, 12 Aug 2025 19:21:12 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:b93d9bbac6026e112c836f5d7e3cd91fbb62fb057faea1faf57094b231941e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf92d68d7f3963a03bc3ed429fe9f45f010233dc1a1ee9dff08d5379fc26b08`

```dockerfile
```

-	Layers:
	-	`sha256:08c94752da86a81383a5f4cf147bd25f20f26bea645fd7613da5cae7d74f6b28`  
		Last Modified: Tue, 12 Aug 2025 19:01:33 GMT  
		Size: 4.0 MB (3999736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d014c13050e89ced3fc1a81aba6146b6a39b81d460156230f8532148f27ee792`  
		Last Modified: Tue, 12 Aug 2025 19:01:34 GMT  
		Size: 29.3 KB (29263 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:a76f65d48593874850bbb012e22f7c57a6d1f1060d1a66836c344341b19bf44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.3 MB (656298887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397742271d67ff68c8adb959091b1259330c80b790b8f401eee1d4687f3f685c`
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 29 Jul 2025 11:47:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:5618e0cf5548b3c1b1acb808dbd651baa9f894576ea435f1e2b6296d89cbe799`  
		Last Modified: Tue, 12 Aug 2025 18:34:44 GMT  
		Size: 45.6 MB (45589768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972144b0f2fc58b59dda462b9cae8d50f5c34458e1dfa2597c7ca9e073f3e8e7`  
		Last Modified: Tue, 12 Aug 2025 18:34:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0975f919b7d374f69245ee4b84267050962976d2a3661bb6f5895ec2ed1c829`  
		Last Modified: Tue, 12 Aug 2025 18:34:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3defc1f103d84bcc1a09549ff1ad650db0dcbff79c3b418cda47d4b75bb75ec3`  
		Last Modified: Tue, 12 Aug 2025 22:24:55 GMT  
		Size: 1.0 MB (1041829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6131b9e83ebe9572a25ef911c68cbd4b44d26180dca89dc08c78330c52094869`  
		Last Modified: Tue, 12 Aug 2025 22:24:55 GMT  
		Size: 835.4 KB (835383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e7b1e1ed5c20ac3affe3188dc6def8a5afb1266f1a8e6627c858d3fddd24df`  
		Last Modified: Tue, 12 Aug 2025 22:24:56 GMT  
		Size: 4.6 KB (4628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1b4694b5e7efd17306dca5326b2e79f739ad54beba0b34e1b40968087183b`  
		Last Modified: Tue, 12 Aug 2025 22:24:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4801a066f27b1ed1fdc037304e19913166eeff8e57c4a702e93b103040e2948a`  
		Last Modified: Wed, 13 Aug 2025 15:37:36 GMT  
		Size: 565.4 MB (565399468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45f5d43f2d98e63c8b5489e8fded8b50abfd10ba89ca532f7217bcaf1444ea5`  
		Last Modified: Tue, 12 Aug 2025 22:24:56 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:d6c11d3ea04258769d87ffe38c2500a5e1878e80824f49b86c9365ac4e809f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70065344f4c514a7b64e097c5f2c5dba91d404e9b8dfd53c49717c22a10bf6e4`

```dockerfile
```

-	Layers:
	-	`sha256:e6853be2d70a1ad55896930a99f3d6aba77fd83944fd2213202d1cd5d3bede79`  
		Last Modified: Wed, 13 Aug 2025 01:01:38 GMT  
		Size: 4.0 MB (4000063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68dcfe8806fe8b85f7b86ed1ae37ead51dd3eec3c85061f7f34d74b283ef9de6`  
		Last Modified: Wed, 13 Aug 2025 01:01:39 GMT  
		Size: 29.4 KB (29436 bytes)  
		MIME: application/vnd.in-toto+json
