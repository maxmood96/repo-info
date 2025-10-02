## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:baccdefb8ae0af45440ab10d447d935462ba85cabb389a55e4e88d77af0f3177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:b7a62351b66b7580aac9357da4a04370679ab8a44a330b24e8cc233b7cd371dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.4 MB (660400627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9a33b3503b0264021db2b0de2424202fe1a1022850b17c708f44b209669753`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a55b01e3ac44fd314137f34c2089a82e6266936a8a7a2e28ce60499bd91791`  
		Last Modified: Thu, 02 Oct 2025 05:02:00 GMT  
		Size: 16.2 MB (16150303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9269535487ff5096d1b8f79569dc6a48e458ed6299ef8d26b93484f4a6099`  
		Last Modified: Thu, 02 Oct 2025 05:02:00 GMT  
		Size: 47.2 MB (47234507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143bcd82887c63307c54c7ebf47bd746a41eb1935e6fa9830782506eda729916`  
		Last Modified: Thu, 02 Oct 2025 05:01:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910c18e65e8e04c327bdfa3f60362798005d218d8f3b932bc57ce41dd3178149`  
		Last Modified: Thu, 02 Oct 2025 05:01:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216d66d47362c7a88bb36cb248e0219d09f81d882a8b794c3c57ae6754f295b3`  
		Last Modified: Thu, 02 Oct 2025 08:29:26 GMT  
		Size: 1.2 MB (1169618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f84738a8246ebd10826b951d498c1ea290899b260c9f9c1c3c11fd0fa26ba`  
		Last Modified: Thu, 02 Oct 2025 08:29:26 GMT  
		Size: 900.5 KB (900493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34354c59416656b1f42bbf021afc4e49fc8415f55b8719f8e2a03749125300c7`  
		Last Modified: Thu, 02 Oct 2025 08:29:27 GMT  
		Size: 4.6 KB (4584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d343ea86871b41ab956504f75c1910463d80f17b8e87aff3efb2f12afc0ff09`  
		Last Modified: Thu, 02 Oct 2025 08:29:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c410554a7d33b2f9d67e3f5a454d07aa52034927b45c5e4672608eebb344af`  
		Last Modified: Thu, 02 Oct 2025 11:21:14 GMT  
		Size: 565.4 MB (565399481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f8ed6a9a1e00f1123a051fc92654409cc9b80a5ad4bae9de7e27e831c3cbe5`  
		Last Modified: Thu, 02 Oct 2025 08:29:28 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:50c76ed7cd6e47a5af46f8167f75304ca26f2633c57ca0f10d049bf9777cbd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496d130c22c876e4e055231553f0da5b5088ce5172df80cc0b1ee31fabd4b8c4`

```dockerfile
```

-	Layers:
	-	`sha256:0667569249aee2c135aa204b7440e99e8b6c1e352cc34ee7aee2537175d80558`  
		Last Modified: Thu, 02 Oct 2025 10:02:11 GMT  
		Size: 4.0 MB (3999752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4cb337191d4ba1dc7c368d207ce52ade5db8c29f19690d6da19ac94154404f`  
		Last Modified: Thu, 02 Oct 2025 10:02:12 GMT  
		Size: 29.3 KB (29263 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:22700676218ae918920537a83b151d8489287d7b110890c1f0c659f173ab8dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.3 MB (656324547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d283e0aadfbdaf7b151724231c85c2f46ab0870ee30f620d7bfdf0e04826b7ef`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3ffc450262d40bd69e810ad68aba0e443988988213880286ca5d67f4f2809d`  
		Last Modified: Thu, 02 Oct 2025 02:14:19 GMT  
		Size: 16.1 MB (16065702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ecc889789aa6512710235fb583548e0e0cb1148732c67b36efa987dadc7bd`  
		Last Modified: Thu, 02 Oct 2025 02:14:22 GMT  
		Size: 45.6 MB (45589603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2347c2613c838f9e8c89f178a7e1167d895fe0a88140df109802a1af28fc25`  
		Last Modified: Thu, 02 Oct 2025 01:57:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb9efb25153c5a0d0ac1e229f8f7786f74ac8f78f9641e046874b49907f744`  
		Last Modified: Thu, 02 Oct 2025 01:57:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7dd0e1106d97753d817e50dff7e68b48b27332b56935c7d658d9269d1f98bc`  
		Last Modified: Thu, 02 Oct 2025 02:16:59 GMT  
		Size: 1.0 MB (1041847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e6c874a271c137f10f005cd18eeddb249de5749beb43a862917b20745debd3`  
		Last Modified: Thu, 02 Oct 2025 02:16:59 GMT  
		Size: 835.4 KB (835374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa29ee129f3815aef01d765c05594288aad858d2d67ff9cb6024479d8ea78d73`  
		Last Modified: Thu, 02 Oct 2025 02:16:59 GMT  
		Size: 4.6 KB (4626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ca7e882168e7239ef723c9a7c9412b6c9f9570b4bf8965d488af7235c2361e`  
		Last Modified: Thu, 02 Oct 2025 02:16:59 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14764766a8755668e49cf3a634b9849663f653e686ad2287fdd13e05a2707233`  
		Last Modified: Thu, 02 Oct 2025 13:08:27 GMT  
		Size: 565.4 MB (565399466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb4b9bf46b4d6fa4b9a677f30a61065606e1077b7a40ea016c8e98c6931231`  
		Last Modified: Thu, 02 Oct 2025 02:16:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:c3872c4cfdfe5572b4fc594e8c1c21de581d8c0518a7169e1b57cbe14566dfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822a360a334404436eee1c42317f4f5135c90be7868c8e251586a6fc5269b28`

```dockerfile
```

-	Layers:
	-	`sha256:cd136c2ced23b9d54c3e5164fbde4c148513d1336b94c3040b805eaad27925a3`  
		Last Modified: Thu, 02 Oct 2025 04:02:10 GMT  
		Size: 4.0 MB (4000079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ce0b0a2a774961f41eafb6a121b047e95a17e40737de73aca7456543d5dcaa`  
		Last Modified: Thu, 02 Oct 2025 04:02:11 GMT  
		Size: 29.4 KB (29436 bytes)  
		MIME: application/vnd.in-toto+json
