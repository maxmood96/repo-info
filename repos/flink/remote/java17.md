## `flink:java17`

```console
$ docker pull flink@sha256:a3d7de567219a3b3912a89b6ac0479cf28a9e887609f1c292c9908597d1b61e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java17` - linux; amd64

```console
$ docker pull flink@sha256:9ade15fc1df2cb37b52f20e493d031fa1d89c04cb454e1d598694767a535269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.6 MB (662598938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4dbfd2981b0e68437d0467bfb640d66a8fadd171ea67285f5b6322a84da9b80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:57 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Nov 2025 18:42:59 GMT
ENV GOSU_VERSION=1.11
# Thu, 06 Nov 2025 18:42:59 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in hkps://keys.openpgp.org $(shuf -e                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 06 Nov 2025 18:42:59 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.1.1/flink-2.1.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.1.1/flink-2.1.1-bin-scala_2.12.tgz.asc GPG_KEY=5EAD34D67F105064591085E4AA69A48B2A51091D CHECK_GPG=true
# Thu, 06 Nov 2025 18:42:59 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 06 Nov 2025 18:42:59 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 18:42:59 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 06 Nov 2025 18:42:59 GMT
WORKDIR /opt/flink
# Thu, 06 Nov 2025 18:43:12 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Thu, 06 Nov 2025 18:43:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 18:43:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:43:12 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 06 Nov 2025 18:43:12 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0431e2b78802434fc25f5b541c227e6568e5aaabbe9a08d2b307d844050a8`  
		Last Modified: Thu, 06 Nov 2025 18:44:02 GMT  
		Size: 1.2 MB (1169680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a1326160e8facf90be7937359723d23722ab455a0034dfa53c1c7248a06c15`  
		Last Modified: Thu, 06 Nov 2025 18:44:01 GMT  
		Size: 900.5 KB (900492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff391b72a0d4f2706520c467bd331789b9342b6ed84ddfa5d6ff18f2664cc34e`  
		Last Modified: Thu, 06 Nov 2025 18:44:02 GMT  
		Size: 4.6 KB (4590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c158f2634fb46a33472154cc32ef7c899de9d346cdb2836a2e2ec8ea0e121`  
		Last Modified: Thu, 06 Nov 2025 18:44:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c32e2eebabf7fe387f7cf0a774ad339a690d5a2c46206158a0dae036dfcc09`  
		Last Modified: Thu, 06 Nov 2025 20:04:15 GMT  
		Size: 567.8 MB (567846217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d262bc5d04afe8dfede8b59ccdd2fd3667216eef58ddeb9c3547d5349f136`  
		Last Modified: Thu, 06 Nov 2025 18:44:02 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:cef1d0320dba3809dd683cc9d7ca1edc901c914f69d796904726413ff285ca11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec6bd4b35d308b4f0075ee4b5c3c3815c9171790c2d36bbc5224cbf75a18d57`

```dockerfile
```

-	Layers:
	-	`sha256:ff24c362cf3e4f1b8d1fa91a923faf1ce97da760c885ed41d11c355490299a12`  
		Last Modified: Thu, 06 Nov 2025 20:01:47 GMT  
		Size: 4.0 MB (3988450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2838230744177a3ac9251b520bbe37dc10d1da68b39ef0dd82c06ff9616134a3`  
		Last Modified: Thu, 06 Nov 2025 20:01:49 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java17` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:a62428ad4eeb08733b8ca4917153b517fec15e909cb698615a586a8a878b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.7 MB (659663343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ea5b702eb5499eebabc734bf90998c1c59b5e4d1806e9d78a20b6c11bd5025`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:28 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Nov 2025 18:42:29 GMT
ENV GOSU_VERSION=1.11
# Thu, 06 Nov 2025 18:42:29 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in hkps://keys.openpgp.org $(shuf -e                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true # buildkit
# Thu, 06 Nov 2025 18:42:29 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.1.1/flink-2.1.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.1.1/flink-2.1.1-bin-scala_2.12.tgz.asc GPG_KEY=5EAD34D67F105064591085E4AA69A48B2A51091D CHECK_GPG=true
# Thu, 06 Nov 2025 18:42:29 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 06 Nov 2025 18:42:29 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 18:42:30 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 06 Nov 2025 18:42:30 GMT
WORKDIR /opt/flink
# Thu, 06 Nov 2025 18:43:12 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Thu, 06 Nov 2025 18:43:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 06 Nov 2025 18:43:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:43:12 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 06 Nov 2025 18:43:12 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ad4c4e9ff5317838ed1e0930c6f5a9f54211d8d101be000751ab8a909eedba`  
		Last Modified: Thu, 06 Nov 2025 18:44:06 GMT  
		Size: 1.0 MB (1041842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca93d00ea41fc7e94e31581487f1a64558a059238257a4c1d5e4618361740be`  
		Last Modified: Thu, 06 Nov 2025 18:44:06 GMT  
		Size: 835.4 KB (835385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86db3a097894c56e16ccaa3c739df9dd973d18cbccacd14bc9131bacf07d3c12`  
		Last Modified: Thu, 06 Nov 2025 18:44:06 GMT  
		Size: 4.6 KB (4636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b730e5b35366f56c7a0125a6e3453ba4c78e0adbefe06148f11efc5d8f37f`  
		Last Modified: Thu, 06 Nov 2025 18:44:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91ce9f5b1d0d333871debcb966c7e6cb06626eed9b990f2adb0fe622ea8f0e5`  
		Last Modified: Thu, 06 Nov 2025 20:18:40 GMT  
		Size: 567.8 MB (567846261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa5fc237dab10a90a701b895b346b1215d740fcabf84dc0dfe81d221837d12`  
		Last Modified: Thu, 06 Nov 2025 18:44:05 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:69730d81ec64b73953bac3d14e5e4c6f6a2907fc97c85679f58aa83aa6e99ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1872671515e87512506559e6aeedffa59940053818bf96536201d6f111684aac`

```dockerfile
```

-	Layers:
	-	`sha256:3069059cf3f0e98db2e02007b60ae1b8a11d827b4e3d61d9374839af5894f2d7`  
		Last Modified: Thu, 06 Nov 2025 20:01:53 GMT  
		Size: 4.0 MB (3988231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8179a184f442beefeaf3ffa2a7404bcbdbe0fe0cdefa59ad97a541af65084fa`  
		Last Modified: Thu, 06 Nov 2025 20:01:54 GMT  
		Size: 30.9 KB (30879 bytes)  
		MIME: application/vnd.in-toto+json
