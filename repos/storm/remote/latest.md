## `storm:latest`

```console
$ docker pull storm@sha256:8a24550b8cb443f30fe16af1c575ad39ee891ec7a684669ec3a8b8356679a780
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:cb0ac030546ab37fbe25b7ab422a1316918772188cf3d5fd9c599750737bb840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.3 MB (451294468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f9a9eb5efccfbbe8eb96107c7b415c3e83a166fb7948b81e60a8b8d6ccbef0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 28 Jan 2025 06:36:36 GMT
ARG RELEASE
# Tue, 28 Jan 2025 06:36:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 06:36:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 06:36:36 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 28 Jan 2025 06:36:36 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 28 Jan 2025 06:36:36 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 06:36:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 06:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 06:36:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 06:36:36 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 28 Jan 2025 06:36:36 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ARG DISTRO_NAME=apache-storm-2.8.0
# Tue, 28 Jan 2025 06:36:36 GMT
# ARGS: DISTRO_NAME=apache-storm-2.8.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     mv "$DISTRO_NAME" apache-storm;     chown -R storm:storm apache-storm # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
WORKDIR /apache-storm
# Tue, 28 Jan 2025 06:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm/bin
# Tue, 28 Jan 2025 06:36:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfb89b812cffe9075ac4d6e698768f69598116b4e350b33f9ed1660779d46d9`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 17.0 MB (16967684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937f693baeb28063e35f986a9e15f087e7596bbf78d5ace020bd8064676efe6e`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 47.0 MB (46958393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f485e3e5c817cfb6d01272d57e5e3a9c571a7802027648b792bc547bedfe9391`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a80a545922a15bd0a0e87cce686afccd26a5d3bcdcebedf0fd50eb3151bf3c`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9268e0cb01733a3ec94cf14e7770613c914c08024f0916dc0e0a9ae341d54bda`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d3b237f88cb67743acc2033d7d625784602a7d10445d769abdb716a3f11be8`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 12.4 MB (12385568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce17ab59af60242924e42503592309d4bedfeae987afb56e676702bea0cc2004`  
		Last Modified: Wed, 23 Apr 2025 17:13:55 GMT  
		Size: 345.3 MB (345261022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4085358398cf72af71dfc372eda7d0c0fcb67c54be931f41e9342431fc12f`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:1a51e9bb7109b22bd2b966e9621b6f5fc6dd07b3986acdf352d388f2a20340c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6f487f526015df115565a56b5259386d7ecb6c4c708162e5e7172d37314050`

```dockerfile
```

-	Layers:
	-	`sha256:159b8b028288d00e1b6480f1c477e9dfc53f604e9f28d6ad10e1e8cfc4c352e5`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 4.3 MB (4279833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc719a8546ff845305d9259f4b43e64fdcd9c7dbce8c1c0d1e7beee605e129a`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 26.8 KB (26831 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:d39ffd521cdfc4c0f7a1ba0591dc35c2f315298aa39fa4c3c27b4b32376a3b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.7 MB (449733165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75a353631e2c8b81ec649563e2b0bbe717e314ba17430b2a290404828e2c601`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 28 Jan 2025 06:36:36 GMT
ARG RELEASE
# Tue, 28 Jan 2025 06:36:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 06:36:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 06:36:36 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 28 Jan 2025 06:36:36 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 28 Jan 2025 06:36:36 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 06:36:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 06:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 06:36:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 06:36:36 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 28 Jan 2025 06:36:36 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ARG DISTRO_NAME=apache-storm-2.8.0
# Tue, 28 Jan 2025 06:36:36 GMT
# ARGS: DISTRO_NAME=apache-storm-2.8.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     mv "$DISTRO_NAME" apache-storm;     chown -R storm:storm apache-storm # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
WORKDIR /apache-storm
# Tue, 28 Jan 2025 06:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm/bin
# Tue, 28 Jan 2025 06:36:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Jan 2025 06:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3fcfbd7cdd46cc6da1b7ca322a5fae240ecf8c2ddee52d3757a50fb8a7f99b`  
		Last Modified: Wed, 09 Apr 2025 07:06:47 GMT  
		Size: 46.5 MB (46463775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c3464fc3980701a0f93833a4500513bf69ed4503ced14136593b45b11bacf`  
		Last Modified: Wed, 09 Apr 2025 07:06:45 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7fa53a112f421caf5e90ad5babcb688d10f79421cd4bed4cb1ff76c73ef5d4`  
		Last Modified: Wed, 09 Apr 2025 07:06:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb0548133f1b13b6b4702423b7f9b6844241caa8e0cc582053727e2a9d47c1`  
		Last Modified: Wed, 09 Apr 2025 16:40:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16abe3ad97987a98ff3383ac4bbd536054719f74af14746cca90614dd06fc1c2`  
		Last Modified: Wed, 09 Apr 2025 16:40:09 GMT  
		Size: 12.2 MB (12170032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f79ea19e7409468e841e1e28b5d1fbde268b714d35f0717c7a7391f999c1ee8`  
		Last Modified: Wed, 09 Apr 2025 16:40:15 GMT  
		Size: 345.3 MB (345261008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a785b670d6b119a8d277a7ebdfa3715499204d1a8c96fbc3c21637f9cb3991ce`  
		Last Modified: Wed, 09 Apr 2025 16:40:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:c23f802453ecac8eef06af4863f714a32a3484ff4be4a3a5e90d6129c2f0dba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b43092fc104703051829a1227771637a241d205efbc31396d628933c8eea06`

```dockerfile
```

-	Layers:
	-	`sha256:c93e4f5cdf847a076219c9c9fe79d70c3b1853ec20b61818ea71e0eb42bcbac0`  
		Last Modified: Wed, 09 Apr 2025 16:40:08 GMT  
		Size: 4.3 MB (4280363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33af70f414bd2d8c6bbb737eedd6aff75d276731116dc74bbd18c66629066434`  
		Last Modified: Wed, 09 Apr 2025 16:40:08 GMT  
		Size: 27.0 KB (26977 bytes)  
		MIME: application/vnd.in-toto+json
