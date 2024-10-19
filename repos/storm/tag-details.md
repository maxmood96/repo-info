<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:2.6`](#storm26)
-	[`storm:2.6-jre17`](#storm26-jre17)
-	[`storm:2.6.4`](#storm264)
-	[`storm:2.6.4-jre17`](#storm264-jre17)
-	[`storm:latest`](#stormlatest)

## `storm:2.6`

```console
$ docker pull storm@sha256:d7d7dd7fae85f5f4baaff00d060827074dd7817afba10e0e4627f7c94e890579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6` - linux; amd64

```console
$ docker pull storm@sha256:13c796a1c8fbb100256a50dd2c5aa6002b70bbef4fa961081f621949b0e49168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573880390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d7a8267db10f412b84ac4170b983084106987262226f57404712556b1f747a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d714900c64c62dd5ca14871c7f2f4bfe027545a9b640a086c56f6fc0b1d8d79`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 13.8 MB (13767610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e47721f6b4df82dedcc0a3c73f528f9159e49f9f4b0d938b3eb369bde1a15f`  
		Last Modified: Sat, 19 Oct 2024 02:06:38 GMT  
		Size: 47.2 MB (47197797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3263419687c5d27113ae33f4faba0c1b7e1adbce037bd8063f327c36283ca`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bc1cde785a34f357eb3258598b703c517fe13abcca4621f2a039f4cdfee56c`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d9c29740213f491f436b184598281f2dfed759af968f7e029bfe543330826`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747d0c1ab05c52d6a011abe937b072756f825a4714bf8da14ad3cf5396d209a3`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 15.6 MB (15575648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b341ed501370f8214981a61fefca38812ba8b3f479b43e8f0bfafb4a8c13d6`  
		Last Modified: Sat, 19 Oct 2024 03:00:34 GMT  
		Size: 467.6 MB (467584995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da2fcfb3e3c9ef5e66642219e765bfffc2d8e0f45aa124c66f92c2d916f6ef2`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:5737957b41b2507fde04ba5a5dda207fb3bf2a615c260ed802560e2e1033045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b67fe33ae81024d4eeedfd009eb9b423fb06a053d40096d2df6600bbe03de9`

```dockerfile
```

-	Layers:
	-	`sha256:eaf7255950bc2831349189580e824682e25a33f1c6540451fb760b97e226ce1f`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 4.6 MB (4579710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3096846995549360c40a40fdce9bd4d2315ed5e4f96f259cb53c78bfe86893`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:13745e294731a03470bb6cb1ae979824f282d07ad20fed8bb9033a4e22bf1014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.3 MB (572252132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b610d5cfa0f5172ae923b7c7752ec45a70fd093a305d1ff14d79dabaa6bbdc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 13:04:35 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:04:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Sep 2024 13:04:35 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 11 Sep 2024 13:04:35 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf81e66fa50a74466657a4cd87ecbb55a60193bc2fd0d891a8cfee51b5d007e`  
		Last Modified: Wed, 16 Oct 2024 01:17:24 GMT  
		Size: 45.6 MB (45557334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954d8582d92e1ba2f3cd51b22cf7b3a63a34f350d1db2286d2681db0970f0f1`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d55cecd5117dfdb0d0cb27bfa425c664e190b08c8ca3ccb82fcee60d1fd4e`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee116aa4b1f7a47c5eb56d991b32ac03108794d5cf08fd71274c985f9d18b1c3`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa6fdc9c44561399786b604a6990129bddc55b2a37f4fa05e1a2f0365de049`  
		Last Modified: Wed, 16 Oct 2024 05:03:20 GMT  
		Size: 15.4 MB (15354777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbfb14855e75400edd83ffeb011a16361e6f72beb0ae852078544c5a1d010f`  
		Last Modified: Wed, 16 Oct 2024 05:03:28 GMT  
		Size: 467.6 MB (467584674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0428debb04dfd90c8ba41944ae5b496dd06c2e3b821acf0fec445fe5202ce`  
		Last Modified: Wed, 16 Oct 2024 05:03:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:c66f2f8cc9b4b82c7e6e7aca5544df3d982fe20a8ed2f0a3dda3befca10e181d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3778e43118e5750bb51adbe55cf2506954755c06e3d5467116f84bb250663b4f`

```dockerfile
```

-	Layers:
	-	`sha256:1da8518cb3ba6b47751d856a8592391b4ad4207962cc6f81aaec360b9457336d`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 4.5 MB (4474423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238fe92e2a993775b6f0ceefde0ebe421ea7db8994b0bc77a347f3b34b2ed1dc`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 26.1 KB (26107 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6-jre17`

```console
$ docker pull storm@sha256:e61c978bcde0a3250e2230f21b14c196e5f5496678105743b8812c3cfda7c51f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6-jre17` - linux; amd64

```console
$ docker pull storm@sha256:d393e9cac0f74fb5ac72e9107a055018dfee7775f920afd334c499a79e83ad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.0 MB (573962584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1866b225cf0c0a1c196a8910e588ef21724bfed775962168b5e74467118dca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20749b397c3a6bc19ec9ddf36b367cb00bf54de9bec9e01e79d8e7fa2fb32e7d`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 13.8 MB (13767623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0940445ae18372caa52e403c6c8ff97e436110f8061efd3290531a2e34e36b`  
		Last Modified: Sat, 19 Oct 2024 02:06:54 GMT  
		Size: 47.3 MB (47280422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309fceffb97efd41db69e8a254578c4f9ec003685a627105686cae69aa3d83c8`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f48c6d27ce9d80efa458559677e80d081d1337561bc40cae3272668a35742e`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b0f85c8fb3a6e01ef021547a514622513510e9aab7fbec35931caa32605074`  
		Last Modified: Sat, 19 Oct 2024 03:00:17 GMT  
		Size: 15.6 MB (15575495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3353a2ca389e81b787b3de6b224e2f92f960a52cc6491115b027355ef815d06`  
		Last Modified: Sat, 19 Oct 2024 03:00:23 GMT  
		Size: 467.6 MB (467584704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab7a95cb9197609947053239fae7f59800c4f40c546f7657a20039c9db1de22`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:7619d68da0513df92b00a339a9efdadad482cd13ffe1b999d86c7d1c24e7648f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb423ce5c6930b1ef0b4ba7290464acff425f7a091c3d5a47f58cc7732bf8e84`

```dockerfile
```

-	Layers:
	-	`sha256:fe783a07e7e827610e1c9e16e5b5e188db05268e15763f16954aec5abdd7a4b1`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 4.6 MB (4565669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80395fbc1489767c71efbbc42e66a6d9b151cb79bdf3fe9248babe502cfe533`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 25.9 KB (25853 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:d1200f568b0355368265171c740fd9829f68c14599544b6c558e35b2b1af2fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573441336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14f28249c6a74e15d6eab7e3a0d06b6280d32b6180796c74155a4efd1b393b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 13:04:35 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:04:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Sep 2024 13:04:35 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 11 Sep 2024 13:04:35 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abe1f00c4a59efc8b8b98a4c72f2a24678aa2ac24213badb68e8c730c7d11fa`  
		Last Modified: Wed, 16 Oct 2024 01:18:34 GMT  
		Size: 46.7 MB (46746395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa4d4c8336cbb9757f56d63c4952e4b1066c14093ab74c11112de2c61da7e9`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e548190d29ede72fe071dd39371bfe2e204f8f8a3dd19c6d316055be7a5ad60`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e13be8efb33621e4a2b9f4df0cac9aa12a96d57e83e355e8be39812837a28`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88068071a5a0d8c10ce9cf87ff997eee91d9a4641a5215ef4aad89d62efe5f4e`  
		Last Modified: Wed, 16 Oct 2024 05:05:01 GMT  
		Size: 15.4 MB (15354884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a0687136160f88d7193abb449675d92073984f8480024a362a91ce7e055b07`  
		Last Modified: Wed, 16 Oct 2024 05:05:16 GMT  
		Size: 467.6 MB (467584708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38203e10f5b83a81e479d7cc61db12778867ced2d58133738aab67b4399929f`  
		Last Modified: Wed, 16 Oct 2024 05:05:01 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:085c87e8d271dc7887bdcc8462a7f7e93d2165e070e938df1dd2f2a82c04d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bf7da206dd01ce69ecb2c3c71a7e910747657bcbf8797bd048a5f2f22117f7`

```dockerfile
```

-	Layers:
	-	`sha256:c27ffc2f9dfd72f4b3e1ca4770c0f3ea918b7d926a63529c7b43075a81efb897`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 4.5 MB (4459751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728cbffe2e3db02f9399e0b3df73ccb82e8a9604d30509fbed1a6561585cb142`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 26.0 KB (25951 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.4`

```console
$ docker pull storm@sha256:d7d7dd7fae85f5f4baaff00d060827074dd7817afba10e0e4627f7c94e890579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.4` - linux; amd64

```console
$ docker pull storm@sha256:13c796a1c8fbb100256a50dd2c5aa6002b70bbef4fa961081f621949b0e49168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573880390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d7a8267db10f412b84ac4170b983084106987262226f57404712556b1f747a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d714900c64c62dd5ca14871c7f2f4bfe027545a9b640a086c56f6fc0b1d8d79`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 13.8 MB (13767610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e47721f6b4df82dedcc0a3c73f528f9159e49f9f4b0d938b3eb369bde1a15f`  
		Last Modified: Sat, 19 Oct 2024 02:06:38 GMT  
		Size: 47.2 MB (47197797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3263419687c5d27113ae33f4faba0c1b7e1adbce037bd8063f327c36283ca`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bc1cde785a34f357eb3258598b703c517fe13abcca4621f2a039f4cdfee56c`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d9c29740213f491f436b184598281f2dfed759af968f7e029bfe543330826`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747d0c1ab05c52d6a011abe937b072756f825a4714bf8da14ad3cf5396d209a3`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 15.6 MB (15575648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b341ed501370f8214981a61fefca38812ba8b3f479b43e8f0bfafb4a8c13d6`  
		Last Modified: Sat, 19 Oct 2024 03:00:34 GMT  
		Size: 467.6 MB (467584995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da2fcfb3e3c9ef5e66642219e765bfffc2d8e0f45aa124c66f92c2d916f6ef2`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4` - unknown; unknown

```console
$ docker pull storm@sha256:5737957b41b2507fde04ba5a5dda207fb3bf2a615c260ed802560e2e1033045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b67fe33ae81024d4eeedfd009eb9b423fb06a053d40096d2df6600bbe03de9`

```dockerfile
```

-	Layers:
	-	`sha256:eaf7255950bc2831349189580e824682e25a33f1c6540451fb760b97e226ce1f`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 4.6 MB (4579710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3096846995549360c40a40fdce9bd4d2315ed5e4f96f259cb53c78bfe86893`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.4` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:13745e294731a03470bb6cb1ae979824f282d07ad20fed8bb9033a4e22bf1014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.3 MB (572252132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b610d5cfa0f5172ae923b7c7752ec45a70fd093a305d1ff14d79dabaa6bbdc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 13:04:35 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:04:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Sep 2024 13:04:35 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 11 Sep 2024 13:04:35 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf81e66fa50a74466657a4cd87ecbb55a60193bc2fd0d891a8cfee51b5d007e`  
		Last Modified: Wed, 16 Oct 2024 01:17:24 GMT  
		Size: 45.6 MB (45557334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954d8582d92e1ba2f3cd51b22cf7b3a63a34f350d1db2286d2681db0970f0f1`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d55cecd5117dfdb0d0cb27bfa425c664e190b08c8ca3ccb82fcee60d1fd4e`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee116aa4b1f7a47c5eb56d991b32ac03108794d5cf08fd71274c985f9d18b1c3`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa6fdc9c44561399786b604a6990129bddc55b2a37f4fa05e1a2f0365de049`  
		Last Modified: Wed, 16 Oct 2024 05:03:20 GMT  
		Size: 15.4 MB (15354777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbfb14855e75400edd83ffeb011a16361e6f72beb0ae852078544c5a1d010f`  
		Last Modified: Wed, 16 Oct 2024 05:03:28 GMT  
		Size: 467.6 MB (467584674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0428debb04dfd90c8ba41944ae5b496dd06c2e3b821acf0fec445fe5202ce`  
		Last Modified: Wed, 16 Oct 2024 05:03:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4` - unknown; unknown

```console
$ docker pull storm@sha256:c66f2f8cc9b4b82c7e6e7aca5544df3d982fe20a8ed2f0a3dda3befca10e181d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3778e43118e5750bb51adbe55cf2506954755c06e3d5467116f84bb250663b4f`

```dockerfile
```

-	Layers:
	-	`sha256:1da8518cb3ba6b47751d856a8592391b4ad4207962cc6f81aaec360b9457336d`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 4.5 MB (4474423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238fe92e2a993775b6f0ceefde0ebe421ea7db8994b0bc77a347f3b34b2ed1dc`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 26.1 KB (26107 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.4-jre17`

```console
$ docker pull storm@sha256:e61c978bcde0a3250e2230f21b14c196e5f5496678105743b8812c3cfda7c51f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.4-jre17` - linux; amd64

```console
$ docker pull storm@sha256:d393e9cac0f74fb5ac72e9107a055018dfee7775f920afd334c499a79e83ad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.0 MB (573962584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1866b225cf0c0a1c196a8910e588ef21724bfed775962168b5e74467118dca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20749b397c3a6bc19ec9ddf36b367cb00bf54de9bec9e01e79d8e7fa2fb32e7d`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 13.8 MB (13767623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0940445ae18372caa52e403c6c8ff97e436110f8061efd3290531a2e34e36b`  
		Last Modified: Sat, 19 Oct 2024 02:06:54 GMT  
		Size: 47.3 MB (47280422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309fceffb97efd41db69e8a254578c4f9ec003685a627105686cae69aa3d83c8`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f48c6d27ce9d80efa458559677e80d081d1337561bc40cae3272668a35742e`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b0f85c8fb3a6e01ef021547a514622513510e9aab7fbec35931caa32605074`  
		Last Modified: Sat, 19 Oct 2024 03:00:17 GMT  
		Size: 15.6 MB (15575495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3353a2ca389e81b787b3de6b224e2f92f960a52cc6491115b027355ef815d06`  
		Last Modified: Sat, 19 Oct 2024 03:00:23 GMT  
		Size: 467.6 MB (467584704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab7a95cb9197609947053239fae7f59800c4f40c546f7657a20039c9db1de22`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:7619d68da0513df92b00a339a9efdadad482cd13ffe1b999d86c7d1c24e7648f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb423ce5c6930b1ef0b4ba7290464acff425f7a091c3d5a47f58cc7732bf8e84`

```dockerfile
```

-	Layers:
	-	`sha256:fe783a07e7e827610e1c9e16e5b5e188db05268e15763f16954aec5abdd7a4b1`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 4.6 MB (4565669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80395fbc1489767c71efbbc42e66a6d9b151cb79bdf3fe9248babe502cfe533`  
		Last Modified: Sat, 19 Oct 2024 03:00:16 GMT  
		Size: 25.9 KB (25853 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.4-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:d1200f568b0355368265171c740fd9829f68c14599544b6c558e35b2b1af2fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573441336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14f28249c6a74e15d6eab7e3a0d06b6280d32b6180796c74155a4efd1b393b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 13:04:35 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:04:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Sep 2024 13:04:35 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 11 Sep 2024 13:04:35 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abe1f00c4a59efc8b8b98a4c72f2a24678aa2ac24213badb68e8c730c7d11fa`  
		Last Modified: Wed, 16 Oct 2024 01:18:34 GMT  
		Size: 46.7 MB (46746395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa4d4c8336cbb9757f56d63c4952e4b1066c14093ab74c11112de2c61da7e9`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e548190d29ede72fe071dd39371bfe2e204f8f8a3dd19c6d316055be7a5ad60`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e13be8efb33621e4a2b9f4df0cac9aa12a96d57e83e355e8be39812837a28`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88068071a5a0d8c10ce9cf87ff997eee91d9a4641a5215ef4aad89d62efe5f4e`  
		Last Modified: Wed, 16 Oct 2024 05:05:01 GMT  
		Size: 15.4 MB (15354884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a0687136160f88d7193abb449675d92073984f8480024a362a91ce7e055b07`  
		Last Modified: Wed, 16 Oct 2024 05:05:16 GMT  
		Size: 467.6 MB (467584708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38203e10f5b83a81e479d7cc61db12778867ced2d58133738aab67b4399929f`  
		Last Modified: Wed, 16 Oct 2024 05:05:01 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:085c87e8d271dc7887bdcc8462a7f7e93d2165e070e938df1dd2f2a82c04d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bf7da206dd01ce69ecb2c3c71a7e910747657bcbf8797bd048a5f2f22117f7`

```dockerfile
```

-	Layers:
	-	`sha256:c27ffc2f9dfd72f4b3e1ca4770c0f3ea918b7d926a63529c7b43075a81efb897`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 4.5 MB (4459751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728cbffe2e3db02f9399e0b3df73ccb82e8a9604d30509fbed1a6561585cb142`  
		Last Modified: Wed, 16 Oct 2024 05:05:00 GMT  
		Size: 26.0 KB (25951 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:latest`

```console
$ docker pull storm@sha256:d7d7dd7fae85f5f4baaff00d060827074dd7817afba10e0e4627f7c94e890579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:13c796a1c8fbb100256a50dd2c5aa6002b70bbef4fa961081f621949b0e49168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573880390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d7a8267db10f412b84ac4170b983084106987262226f57404712556b1f747a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d714900c64c62dd5ca14871c7f2f4bfe027545a9b640a086c56f6fc0b1d8d79`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 13.8 MB (13767610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e47721f6b4df82dedcc0a3c73f528f9159e49f9f4b0d938b3eb369bde1a15f`  
		Last Modified: Sat, 19 Oct 2024 02:06:38 GMT  
		Size: 47.2 MB (47197797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3263419687c5d27113ae33f4faba0c1b7e1adbce037bd8063f327c36283ca`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bc1cde785a34f357eb3258598b703c517fe13abcca4621f2a039f4cdfee56c`  
		Last Modified: Sat, 19 Oct 2024 02:06:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d9c29740213f491f436b184598281f2dfed759af968f7e029bfe543330826`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747d0c1ab05c52d6a011abe937b072756f825a4714bf8da14ad3cf5396d209a3`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 15.6 MB (15575648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b341ed501370f8214981a61fefca38812ba8b3f479b43e8f0bfafb4a8c13d6`  
		Last Modified: Sat, 19 Oct 2024 03:00:34 GMT  
		Size: 467.6 MB (467584995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da2fcfb3e3c9ef5e66642219e765bfffc2d8e0f45aa124c66f92c2d916f6ef2`  
		Last Modified: Sat, 19 Oct 2024 03:00:29 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:5737957b41b2507fde04ba5a5dda207fb3bf2a615c260ed802560e2e1033045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b67fe33ae81024d4eeedfd009eb9b423fb06a053d40096d2df6600bbe03de9`

```dockerfile
```

-	Layers:
	-	`sha256:eaf7255950bc2831349189580e824682e25a33f1c6540451fb760b97e226ce1f`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 4.6 MB (4579710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3096846995549360c40a40fdce9bd4d2315ed5e4f96f259cb53c78bfe86893`  
		Last Modified: Sat, 19 Oct 2024 03:00:28 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:13745e294731a03470bb6cb1ae979824f282d07ad20fed8bb9033a4e22bf1014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.3 MB (572252132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b610d5cfa0f5172ae923b7c7752ec45a70fd093a305d1ff14d79dabaa6bbdc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 13:04:35 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:04:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:04:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Sep 2024 13:04:35 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 11 Sep 2024 13:04:35 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 13:04:35 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 11 Sep 2024 13:04:35 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ARG DISTRO_NAME=apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
WORKDIR /apache-storm-2.6.4
# Wed, 11 Sep 2024 13:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.4/bin
# Wed, 11 Sep 2024 13:04:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Sep 2024 13:04:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf81e66fa50a74466657a4cd87ecbb55a60193bc2fd0d891a8cfee51b5d007e`  
		Last Modified: Wed, 16 Oct 2024 01:17:24 GMT  
		Size: 45.6 MB (45557334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954d8582d92e1ba2f3cd51b22cf7b3a63a34f350d1db2286d2681db0970f0f1`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d55cecd5117dfdb0d0cb27bfa425c664e190b08c8ca3ccb82fcee60d1fd4e`  
		Last Modified: Wed, 16 Oct 2024 01:17:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee116aa4b1f7a47c5eb56d991b32ac03108794d5cf08fd71274c985f9d18b1c3`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa6fdc9c44561399786b604a6990129bddc55b2a37f4fa05e1a2f0365de049`  
		Last Modified: Wed, 16 Oct 2024 05:03:20 GMT  
		Size: 15.4 MB (15354777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbfb14855e75400edd83ffeb011a16361e6f72beb0ae852078544c5a1d010f`  
		Last Modified: Wed, 16 Oct 2024 05:03:28 GMT  
		Size: 467.6 MB (467584674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0428debb04dfd90c8ba41944ae5b496dd06c2e3b821acf0fec445fe5202ce`  
		Last Modified: Wed, 16 Oct 2024 05:03:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:c66f2f8cc9b4b82c7e6e7aca5544df3d982fe20a8ed2f0a3dda3befca10e181d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3778e43118e5750bb51adbe55cf2506954755c06e3d5467116f84bb250663b4f`

```dockerfile
```

-	Layers:
	-	`sha256:1da8518cb3ba6b47751d856a8592391b4ad4207962cc6f81aaec360b9457336d`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 4.5 MB (4474423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238fe92e2a993775b6f0ceefde0ebe421ea7db8994b0bc77a347f3b34b2ed1dc`  
		Last Modified: Wed, 16 Oct 2024 05:03:18 GMT  
		Size: 26.1 KB (26107 bytes)  
		MIME: application/vnd.in-toto+json
