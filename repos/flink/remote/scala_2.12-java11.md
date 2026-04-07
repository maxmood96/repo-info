## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:9f76a250ab4cbcfa8e6456c7900563124aeb0c5848ae28456c52b75c6f3ae988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:3efde2c13ff2238d555c5a3d2689824aad0ba523ce821cca647263ccba35a245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.5 MB (665479940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05584177359bec533a738e4f7e2cf913bb5b22bcf6fda01781ce74ca190b7026`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 01:51:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:51:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 02:46:50 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:46:51 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Tue, 07 Apr 2026 02:46:51 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 07 Apr 2026 02:46:51 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:46:51 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 07 Apr 2026 02:46:51 GMT
WORKDIR /opt/flink
# Tue, 07 Apr 2026 02:47:13 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 07 Apr 2026 02:47:13 GMT
USER flink
# Tue, 07 Apr 2026 02:47:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:47:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:47:13 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 07 Apr 2026 02:47:13 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60179fb4f9993fd09e3fb018b3d68b328716b54d0fc0ffdaf2dcb0a8b6a0115`  
		Last Modified: Tue, 07 Apr 2026 01:51:58 GMT  
		Size: 17.0 MB (16983678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee05ed179b7121f9dd36393b3039458079b1fe464d933de7ab2be1d5b46ca1f`  
		Last Modified: Tue, 07 Apr 2026 01:51:59 GMT  
		Size: 47.3 MB (47305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864c71c7f0942249c7777e158ecc41eec3124b0f2a3cc915b13416cc1b0ec645`  
		Last Modified: Tue, 07 Apr 2026 01:51:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764818ccfced7c634a25bd44cc23c9db36d1b2761535ad5783647c0a84a10c6b`  
		Last Modified: Tue, 07 Apr 2026 01:51:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d59e3a369d5363bf2c8bb138cdba17705368a664ee693936ab1a362db06d0`  
		Last Modified: Tue, 07 Apr 2026 02:47:44 GMT  
		Size: 1.3 MB (1323297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87621d63f5dea7d5d134f0e585818640667932ab3d7e331dbbaeb5482e5ecac4`  
		Last Modified: Tue, 07 Apr 2026 02:47:44 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336867696e046051b8da76e4cddf83239c8fec362266abe160b4dc84c6d24c92`  
		Last Modified: Tue, 07 Apr 2026 02:47:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29600ff0c2620e9e4c9ff8145449413fc187e4edc7bb09a2083044edc41159d`  
		Last Modified: Tue, 07 Apr 2026 02:47:56 GMT  
		Size: 570.1 MB (570128326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e6753414797206ed21c5e70051e0e9798d68b4677de5d0686afce3549fdec8`  
		Last Modified: Tue, 07 Apr 2026 02:47:45 GMT  
		Size: 2.2 KB (2238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:40a55b11314b5c793b9581feff6ba9782f6841dcea1dfffee67b9874059c50d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3434b43562e7550229102f445a20849b6e0b3d5c60766bca13f3f85bf292ec`

```dockerfile
```

-	Layers:
	-	`sha256:735d31148536f678709639ae790d8591bf102a85fc8f1ed99f53840a0c084c59`  
		Last Modified: Tue, 07 Apr 2026 02:47:44 GMT  
		Size: 3.4 MB (3406528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf1d0d522e1c931e88fcd7e8f0b682dd981a8923e11da27f1394f94d78dc40e`  
		Last Modified: Tue, 07 Apr 2026 02:47:44 GMT  
		Size: 23.8 KB (23769 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:39aed9f68e444f39d48f14dc10922784504b8638717cc2f674e70fcd64ca199a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.8 MB (662815791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632e9edfca0778d12c373dd157c2af85d0901f96bdb0d53d6c58c31dce44931`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:59 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 01:55:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 02:57:32 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:57:32 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Tue, 07 Apr 2026 02:57:32 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 07 Apr 2026 02:57:32 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:57:32 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Tue, 07 Apr 2026 02:57:32 GMT
WORKDIR /opt/flink
# Tue, 07 Apr 2026 02:57:54 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Tue, 07 Apr 2026 02:57:54 GMT
USER flink
# Tue, 07 Apr 2026 02:57:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:57:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:57:54 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Tue, 07 Apr 2026 02:57:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5aaa9423aeb98f124ecd5bfc9cc9d2b6bbfd77afdfc615a5ffe5b0aa59dba`  
		Last Modified: Tue, 07 Apr 2026 01:55:15 GMT  
		Size: 17.0 MB (16996309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9f1086d5cdb9b7d29969803d243b7509adcced52d84054228c2ffb4bc5db43`  
		Last Modified: Tue, 07 Apr 2026 01:55:16 GMT  
		Size: 45.6 MB (45623220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234868e34858674f6573dc6e546497ae3249d8e21c6452734bf3b67739daf6db`  
		Last Modified: Tue, 07 Apr 2026 01:55:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacf59819090c7ed204bc5352c78de43c279bd7c44bf71278d1faf986da74c29`  
		Last Modified: Tue, 07 Apr 2026 01:55:14 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5816663330eeb76828402f8971e74f3398cbce36eb633d15729d3c54dc0d1`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 1.2 MB (1187872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9632c481949e18f45efbb3c17dcaed3764ee4abc483d0368f8c3363640c7e3`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc4850a48c62cdf019455662d50aefcc8ab1abb081e147f015c85d337c99821`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f323d83a82bad3d7479434104cc803765a93ad6132ba21f504f6f62a4b5db7`  
		Last Modified: Tue, 07 Apr 2026 02:58:38 GMT  
		Size: 570.1 MB (570128368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7dd52b6c29e9cd974c7ea20862d9f4ff6e5ac86373452893c92992bf1dbeb2`  
		Last Modified: Tue, 07 Apr 2026 02:58:28 GMT  
		Size: 2.2 KB (2237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:scala_2.12-java11` - unknown; unknown

```console
$ docker pull flink@sha256:660054e84efd9abd0fa31d93da76b68f6fe8ecb6beeb6a26e35daf29b7d9c001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a763827cf5b0070ac6689fb7f5004bf0a429b4c2b75457dff979e86ebd3b6276`

```dockerfile
```

-	Layers:
	-	`sha256:58b663587575822d9fc1f329253072f2588c8c6a650f505b0b6f89c5876acbc9`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 3.4 MB (3407646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e623615ddee3399e633438a9637b0ba405b197e6207b8aafb81efb2dec81f379`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 23.9 KB (23927 bytes)  
		MIME: application/vnd.in-toto+json
