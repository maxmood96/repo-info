## `flink:latest`

```console
$ docker pull flink@sha256:fe370c459da5a71da6b6e298925c24ae1ca64a65d6916a9e80b1991ede035cd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:latest` - linux; amd64

```console
$ docker pull flink@sha256:f870ca7331e136011d6a86a5223c0c5f9a96f650f381268a237354c498193085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.2 MB (660152672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d9a4ce2f3ccb41b75abae748cd63ae1adb23098f9fe26ffd3209c614bbe0e2`
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a8b9e652f47dc5aae4db79deb296bc65f3697a15a864fc909054ac494c90a`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 16.2 MB (16150578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3929ce9ef98d521214361456dc3601b66f098801031407f6deeeec81a92929f`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 47.0 MB (46986099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df735f481adca6219ee0da74f1af97ec6e7649e2f83eb571ef24cb12912ab99`  
		Last Modified: Mon, 01 Sep 2025 23:08:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74104e4bf83056c8c3e61124227f5aea73d12c332dad0007db77bbbe2bcaf628`  
		Last Modified: Tue, 02 Sep 2025 01:36:53 GMT  
		Size: 1.2 MB (1169644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6784e85e621e3f6fac8954cf640750767da7d2bb69b4ffcb14df051c81ebb0`  
		Last Modified: Tue, 02 Sep 2025 01:36:53 GMT  
		Size: 900.5 KB (900494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5b0a0d9bb0219a0bd06e05757280f2e9352af6b9f02115a476b94016fd7e6f`  
		Last Modified: Tue, 02 Sep 2025 01:36:53 GMT  
		Size: 4.6 KB (4584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cb3ec819e2492ea6a8a811f6234317594b664b4b7ccddae097aaa16aa274bc`  
		Last Modified: Tue, 02 Sep 2025 01:36:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114e9048233e119942c65c196a2bbc84c018ec09d524edb8490355249c53a727`  
		Last Modified: Tue, 02 Sep 2025 04:02:59 GMT  
		Size: 565.4 MB (565399518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612c86f448268d327221926984224c20326230244442d257bc9df4ab271b0554`  
		Last Modified: Tue, 02 Sep 2025 01:36:53 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:latest` - unknown; unknown

```console
$ docker pull flink@sha256:5ae758792e53dc97f0d9e8f1b28f56c07b405564ead33c807860d5e45a929053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71b61853c59dc55799ee251b7d57e53bbb95331ebbb8f9925ca874b5347acbb`

```dockerfile
```

-	Layers:
	-	`sha256:813fa6dafd6198328cfdebdcdbb571a2e4686d83a93f5fcb798dee510edf2826`  
		Last Modified: Tue, 02 Sep 2025 04:01:29 GMT  
		Size: 4.0 MB (3988450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2760fb546ba7bd5a54236774561a016c4f11ed81264a45b6b232a4ec8c11c1f`  
		Last Modified: Tue, 02 Sep 2025 04:01:30 GMT  
		Size: 31.1 KB (31075 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:latest` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:585dd1f95accba28571dd0233992e37b5e3a432af2560bef5aec34ce845549c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.2 MB (657216490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305097432f3f0c758654a606dd29a6f6a7331a575c0430486223c8d9057393ee`
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
	-	`sha256:befe395d0b7aaf8cb686108def2873392acbd5c9af9d33844dd856b838218c5d`  
		Last Modified: Thu, 02 Oct 2025 02:18:04 GMT  
		Size: 1.0 MB (1041759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69714ca579552b9aa652cbf4038b7f5fa0d608252fd558dce3e0f5fb033e9383`  
		Last Modified: Thu, 02 Oct 2025 02:18:04 GMT  
		Size: 835.4 KB (835382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9a7b4403969b39f56a1281feab47acfea73fd57c0eb7acac0ba7b0c19b2527`  
		Last Modified: Thu, 02 Oct 2025 02:18:04 GMT  
		Size: 4.6 KB (4624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4673f8131908e886d85360cb01e45b7de1735f48cee213dac996f5db466e5d`  
		Last Modified: Thu, 02 Oct 2025 02:18:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528341c31b1a85f445bd08230ae6b1291f2a34a88ec2788d516f582fb480f2cb`  
		Last Modified: Thu, 02 Oct 2025 03:34:47 GMT  
		Size: 565.4 MB (565399506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160f0a17ba0a067c337a28a75288c744887fe934333d6eb7c5f0fc19c62367a9`  
		Last Modified: Thu, 02 Oct 2025 02:18:04 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:latest` - unknown; unknown

```console
$ docker pull flink@sha256:ffb063459b2715a81b6ab6bb6e200600d72b0d20d948b8b48b14c71561ef0b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49d0c2b1f6ddacadf75d29ff45ce9a7aec22dafa1182a918afc3860ff7d5645`

```dockerfile
```

-	Layers:
	-	`sha256:fc204e052e853f397dd37287774492ab9d4ab7c3166fa94e930e214685e4d3ff`  
		Last Modified: Thu, 02 Oct 2025 04:02:01 GMT  
		Size: 4.0 MB (3988231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87eb5a8a5a04d4df14b8211f97c31b7e2ce8f09249b4ac7db175583a4d1fd9fa`  
		Last Modified: Thu, 02 Oct 2025 04:02:02 GMT  
		Size: 31.3 KB (31320 bytes)  
		MIME: application/vnd.in-toto+json
