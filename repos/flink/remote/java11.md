## `flink:java11`

```console
$ docker pull flink@sha256:bf8d9c2cb4c193a57e6d04b2d85518f827064dcaf60dabe216b940d939d81d20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:fa99a110b58367e7d54bb2438d145e4037531322a825f688b0c1a5c427dc5f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.4 MB (660401248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7defdffc511760bcc3385deae2d0ec704be6a9354e2a87726b43f8640454b4`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93562cc6f9bc192c13f2b83501a048f58b2eae6db305fc14c3eb783ccf271c`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 16.2 MB (16150617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3e1ddc9434423fb5ee9cc9563841d70dd98f93b48c6db377c94edaf971db9`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 47.2 MB (47234732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29deefaacc1b08c2cd6dd4da058658cbc1cccd46ffb4365bf9265265c5a0f7e`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee05d3a8171244d8a0a91dcc24cc8f88a022f84a6332f1c53cbd3277f23c216`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b405349a60066d7e26516eb244f3f47c30310ed23f13ed70710418e8ce2f894`  
		Last Modified: Tue, 02 Sep 2025 01:32:54 GMT  
		Size: 1.2 MB (1169618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f976a6c9668c761d36496049ba6537cea3cdb36380145bba3560d283b0c0311c`  
		Last Modified: Tue, 02 Sep 2025 01:32:54 GMT  
		Size: 900.5 KB (900489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e981c22dd86762471823d5a17cfc5b18db160ba70a67cf1550a56cbd76dbdfa8`  
		Last Modified: Tue, 02 Sep 2025 01:32:54 GMT  
		Size: 4.6 KB (4587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ea7d72d4f92bfb6bf579de94687f92b607d3558162d7286530d56d52184a6`  
		Last Modified: Tue, 02 Sep 2025 01:32:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08151d9d043c95f219f7187915363cd4213c8f3d114a95f8139b744ffa248f8`  
		Last Modified: Tue, 02 Sep 2025 01:45:56 GMT  
		Size: 565.4 MB (565399452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31357d06229c787fa8cc644c2205b8d5d3939c5d150fefbbbce57f4674522db`  
		Last Modified: Tue, 02 Sep 2025 01:32:54 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:a2e128ec8aadc712f174a607f2029b9091419d1cbe88d71fd27a0c6392a43f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad22393b0072c36b581d48407578b8ab072a7ca56e8a765b913ac9d0e06f35e`

```dockerfile
```

-	Layers:
	-	`sha256:626d3516e823672a6fe3c03e099fb8de8550d862134aecb21fa73771f58f41f1`  
		Last Modified: Tue, 02 Sep 2025 04:01:30 GMT  
		Size: 4.0 MB (3999752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9a3d5e04f5746c148cd8926f7ec6ee52d4ffae80b226766a09d44fe7b842c3`  
		Last Modified: Tue, 02 Sep 2025 04:01:31 GMT  
		Size: 29.3 KB (29262 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java11` - linux; arm64 variant v8

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
		Last Modified: Thu, 02 Oct 2025 02:16:53 GMT  
		Size: 565.4 MB (565399466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb4b9bf46b4d6fa4b9a677f30a61065606e1077b7a40ea016c8e98c6931231`  
		Last Modified: Thu, 02 Oct 2025 02:16:58 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

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
