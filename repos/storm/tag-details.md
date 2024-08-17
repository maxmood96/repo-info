<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:2.6`](#storm26)
-	[`storm:2.6-jre17`](#storm26-jre17)
-	[`storm:2.6.3`](#storm263)
-	[`storm:2.6.3-jre17`](#storm263-jre17)
-	[`storm:latest`](#stormlatest)

## `storm:2.6`

```console
$ docker pull storm@sha256:2857a93cf91c2b78b22327839b33edcddf01505e130eabb182ee7da2b2728a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6` - linux; amd64

```console
$ docker pull storm@sha256:2268f0de84651710a28bd607072bfd00c2c6823e675696b1f768d26e0dee5791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562562807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f099011f4fc5b1e5f19c48ca3a8d877f9b7cd919ea7fc49910b1674245f550`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1446bd8cee8f27f4c8bda23153d6e37cb9cdcff70593cdd1adcf4ceca726f1dc`  
		Last Modified: Sat, 17 Aug 2024 01:12:19 GMT  
		Size: 47.2 MB (47199108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac061cc6e1044c785cf2248ed48fce7f1f78d7ebcc3b9ef5c0542e2f4153c05`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfeb172632de8cd209bc3782f7da0cb2e11055d9ca34616d49eae145fc92ea3`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d00e698885cec41ea01ff9a9cb2e1284a6228b6b6168c77a243ad29310f71d3`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6e1a785da97a827788d8db3383a60e2d4bc56b31769155ad2623333d82891f`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 15.6 MB (15568139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99ad25d5f73afff3cf1c19798505420d1307235bd14c394f02c94c1ffa2fa8`  
		Last Modified: Sat, 17 Aug 2024 02:03:29 GMT  
		Size: 455.5 MB (455457458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7c3a1314bd66b0aa562b0781ec25e2dab171dff418781fda8f2e0903e815d4`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:bef5d56ae800f378406be1223924f75b1a7fc27c217cb147df905fe7f62bbedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59ebdadde7d581395853003d4087623ccb8f3eec4abfc1f359aa1c1cae973ac`

```dockerfile
```

-	Layers:
	-	`sha256:c2656a5438e69eca18b8eaf8c35d00befa7095cb8c5bf39ab179828290af29ff`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 4.4 MB (4386550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bc67dcc9acd7eb26849218f55f94c8ef7ed9a3348fdfbe344b63432f8f6603`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:51cbcd94278a7c142ddbd36168fa119273051c4a6ec32f9cb460fc1eff920638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560074565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e18fd4cfd3cb64d72943655a71af3504c65a9bee2ef43d012abd162842ff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b88ddb4ecf5fe246bba6257227ea360765bf7e5e84b39bd3714c3139887b03`  
		Last Modified: Sat, 17 Aug 2024 01:35:13 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e182d345c31d609002a84f011563d867f930b0a47a22a00917ffbad20b4c2e`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36eb2eff38509e12ca963f9f32593dc436f59d4f4ed19d96cf4e58a4755e467f`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1034b0611d3f9e5ba81dadbf4bffed1bdccbb09853ed1bc01f0353bf038845f`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6a08a6616de2afc023e5637400c414545b901e0d37c287458d5d5ae18604bd`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 15.4 MB (15350162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca83cdbde2e155cfab3907f338380b0c4ae412f3f86df1bad479db156f54f0`  
		Last Modified: Sat, 17 Aug 2024 08:52:03 GMT  
		Size: 455.5 MB (455457501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a9029d9361567c7e0710cc749505f6afafa12a9ae8f9151e995524ddeb217`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:3ecbae98ced4048e004f52abfca8d23054c390a7207ac5b80c87d28201879f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9413a3679e89252257155fcdf7fedccd332e917390f28c9351932760f6ffd39b`

```dockerfile
```

-	Layers:
	-	`sha256:cf0ed57d7c42f684765461708f3b50efbcfe5e2df09ecd8fc7003cd72efdecfa`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 4.4 MB (4387674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8894dee9fee7627bdec65a86ce7aad36f4a02c7a16becae587ade9df23308`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6-jre17`

```console
$ docker pull storm@sha256:d04b0951cb640b92dd860d49deee21a1fe0fc142c01ee880dd184f5711c5f83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6-jre17` - linux; amd64

```console
$ docker pull storm@sha256:fcbdaf7d1281cc4d30acb0fd8620c014d062f2ede1ebb26d968694b130410e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562643746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6474aed17091ae23a7950ff33eb71b39bb6e22bde8a61fb71cc3e719769021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 23 Jul 2024 08:01:11 GMT
ARG RELEASE
# Tue, 23 Jul 2024 08:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Jul 2024 08:01:11 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 23 Jul 2024 08:01:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 08:01:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 23 Jul 2024 08:01:11 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
WORKDIR /apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Tue, 23 Jul 2024 08:01:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f3240f14b29df5bc95bc46182be5743c59dcd9622a24ab9c977c50e3112a5e`  
		Last Modified: Sat, 17 Aug 2024 01:13:41 GMT  
		Size: 47.3 MB (47280219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b595e1190ec8667726b2bf5ee7d325cd07181c0b309a5100d0162213115a7cb`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197e18a2a290f7c94f0e1ee91964278e287248b72f64580646c08f7fae19af12`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683694b61a5bcd412d3ab65f4b2e930901dc96ad25935049e8550ba9aa3cb7a5`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799270d2a39d6c677162d96ddacb3ffd9c223eb8bbd6dae0337f07bfe650264`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 15.6 MB (15567970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9567d983c22f5778b0d4af3c1b17dd7a2acdb6725bd4717547cec712aac99260`  
		Last Modified: Sat, 17 Aug 2024 02:03:27 GMT  
		Size: 455.5 MB (455457455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc95415a5732eb0a7145cc5c88577f908e09e43b838ad8152aa61874a71889d`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:159146558a8886c194949b59ed673c4f0452bea94d1a1c724370a4c34c36da75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66977c934fed5ef8431b58c0c5587dc0406f64011bd1cde63c9c3db014689bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b83e1df08b7bd59a8114cb5a1696d5684bc65a85edf94e5655c241ada5ebbfff`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 4.4 MB (4386278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f1dcadc949d51c079203807af0a3e63e7d87fb07573cbdde412af9c53c32a5`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 25.8 KB (25809 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:09df44cc4e7c1d4e37205668cbc30a2e3c62a66081909da51c96d6000d82e75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561263830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe28487fc6798a83a4a647f002e573725b3fe14bcee85e3c1af97670f1a7617a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 23 Jul 2024 08:01:11 GMT
ARG RELEASE
# Tue, 23 Jul 2024 08:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Jul 2024 08:01:11 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Tue, 23 Jul 2024 08:01:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 08:01:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 23 Jul 2024 08:01:11 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
WORKDIR /apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Tue, 23 Jul 2024 08:01:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f61f79738faea794be69163a840a5fe9134932adf08d15e3d5ebb38924ed9`  
		Last Modified: Sat, 17 Aug 2024 01:36:25 GMT  
		Size: 46.7 MB (46746363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c7f0bf0755dc5879a47b869ca41b59f0bf14893cb8f129d64b37687b61dc79`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0e0a5bd6de285f3d8b20e89ba1ffdf12683a5db287ebf9c8bf487734a12e1d`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06211b1876d49a0cd2dd0bbd57a90f92f413f2860882fb57b1524850919eebd5`  
		Last Modified: Sat, 17 Aug 2024 08:53:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9fb662a3809fe120d691bdafe6f32d5c962754ddab5ede45171043dc0efc49`  
		Last Modified: Sat, 17 Aug 2024 08:53:24 GMT  
		Size: 15.4 MB (15350303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8efba2f09441803f507fa5a44139346412c89845a8b59642aaae7b30fb0892`  
		Last Modified: Sat, 17 Aug 2024 08:53:32 GMT  
		Size: 455.5 MB (455457497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da812641b30443e12752072db3b6cda3deabb99973470eeb40c6219aa77b8dfc`  
		Last Modified: Sat, 17 Aug 2024 08:53:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:06f6a72bbb1fef31f5356afa5f9263016f7d8d699038bb7b7bd13c779a890431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd139273deb8fc7d445fec694a509ef90ffa1d050b9fff5fe0cff8c778db5a1`

```dockerfile
```

-	Layers:
	-	`sha256:e36ac3bb4eff47eaba76ef82f84c35aca0ee77d1dbf2d63d7fb4a53a77e161a3`  
		Last Modified: Sat, 17 Aug 2024 08:53:23 GMT  
		Size: 4.4 MB (4387390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd8073d65c15211c0c41ff417b14e1ed3536dfc0417f2ffc3068c041dc422a2`  
		Last Modified: Sat, 17 Aug 2024 08:53:22 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.3`

```console
$ docker pull storm@sha256:2857a93cf91c2b78b22327839b33edcddf01505e130eabb182ee7da2b2728a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.3` - linux; amd64

```console
$ docker pull storm@sha256:2268f0de84651710a28bd607072bfd00c2c6823e675696b1f768d26e0dee5791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562562807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f099011f4fc5b1e5f19c48ca3a8d877f9b7cd919ea7fc49910b1674245f550`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1446bd8cee8f27f4c8bda23153d6e37cb9cdcff70593cdd1adcf4ceca726f1dc`  
		Last Modified: Sat, 17 Aug 2024 01:12:19 GMT  
		Size: 47.2 MB (47199108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac061cc6e1044c785cf2248ed48fce7f1f78d7ebcc3b9ef5c0542e2f4153c05`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfeb172632de8cd209bc3782f7da0cb2e11055d9ca34616d49eae145fc92ea3`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d00e698885cec41ea01ff9a9cb2e1284a6228b6b6168c77a243ad29310f71d3`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6e1a785da97a827788d8db3383a60e2d4bc56b31769155ad2623333d82891f`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 15.6 MB (15568139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99ad25d5f73afff3cf1c19798505420d1307235bd14c394f02c94c1ffa2fa8`  
		Last Modified: Sat, 17 Aug 2024 02:03:29 GMT  
		Size: 455.5 MB (455457458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7c3a1314bd66b0aa562b0781ec25e2dab171dff418781fda8f2e0903e815d4`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3` - unknown; unknown

```console
$ docker pull storm@sha256:bef5d56ae800f378406be1223924f75b1a7fc27c217cb147df905fe7f62bbedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59ebdadde7d581395853003d4087623ccb8f3eec4abfc1f359aa1c1cae973ac`

```dockerfile
```

-	Layers:
	-	`sha256:c2656a5438e69eca18b8eaf8c35d00befa7095cb8c5bf39ab179828290af29ff`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 4.4 MB (4386550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bc67dcc9acd7eb26849218f55f94c8ef7ed9a3348fdfbe344b63432f8f6603`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.3` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:51cbcd94278a7c142ddbd36168fa119273051c4a6ec32f9cb460fc1eff920638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560074565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e18fd4cfd3cb64d72943655a71af3504c65a9bee2ef43d012abd162842ff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b88ddb4ecf5fe246bba6257227ea360765bf7e5e84b39bd3714c3139887b03`  
		Last Modified: Sat, 17 Aug 2024 01:35:13 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e182d345c31d609002a84f011563d867f930b0a47a22a00917ffbad20b4c2e`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36eb2eff38509e12ca963f9f32593dc436f59d4f4ed19d96cf4e58a4755e467f`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1034b0611d3f9e5ba81dadbf4bffed1bdccbb09853ed1bc01f0353bf038845f`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6a08a6616de2afc023e5637400c414545b901e0d37c287458d5d5ae18604bd`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 15.4 MB (15350162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca83cdbde2e155cfab3907f338380b0c4ae412f3f86df1bad479db156f54f0`  
		Last Modified: Sat, 17 Aug 2024 08:52:03 GMT  
		Size: 455.5 MB (455457501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a9029d9361567c7e0710cc749505f6afafa12a9ae8f9151e995524ddeb217`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3` - unknown; unknown

```console
$ docker pull storm@sha256:3ecbae98ced4048e004f52abfca8d23054c390a7207ac5b80c87d28201879f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9413a3679e89252257155fcdf7fedccd332e917390f28c9351932760f6ffd39b`

```dockerfile
```

-	Layers:
	-	`sha256:cf0ed57d7c42f684765461708f3b50efbcfe5e2df09ecd8fc7003cd72efdecfa`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 4.4 MB (4387674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8894dee9fee7627bdec65a86ce7aad36f4a02c7a16becae587ade9df23308`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.3-jre17`

```console
$ docker pull storm@sha256:d04b0951cb640b92dd860d49deee21a1fe0fc142c01ee880dd184f5711c5f83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.3-jre17` - linux; amd64

```console
$ docker pull storm@sha256:fcbdaf7d1281cc4d30acb0fd8620c014d062f2ede1ebb26d968694b130410e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562643746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6474aed17091ae23a7950ff33eb71b39bb6e22bde8a61fb71cc3e719769021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 23 Jul 2024 08:01:11 GMT
ARG RELEASE
# Tue, 23 Jul 2024 08:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Jul 2024 08:01:11 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 23 Jul 2024 08:01:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 08:01:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 23 Jul 2024 08:01:11 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
WORKDIR /apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Tue, 23 Jul 2024 08:01:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f3240f14b29df5bc95bc46182be5743c59dcd9622a24ab9c977c50e3112a5e`  
		Last Modified: Sat, 17 Aug 2024 01:13:41 GMT  
		Size: 47.3 MB (47280219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b595e1190ec8667726b2bf5ee7d325cd07181c0b309a5100d0162213115a7cb`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197e18a2a290f7c94f0e1ee91964278e287248b72f64580646c08f7fae19af12`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683694b61a5bcd412d3ab65f4b2e930901dc96ad25935049e8550ba9aa3cb7a5`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8799270d2a39d6c677162d96ddacb3ffd9c223eb8bbd6dae0337f07bfe650264`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 15.6 MB (15567970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9567d983c22f5778b0d4af3c1b17dd7a2acdb6725bd4717547cec712aac99260`  
		Last Modified: Sat, 17 Aug 2024 02:03:27 GMT  
		Size: 455.5 MB (455457455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc95415a5732eb0a7145cc5c88577f908e09e43b838ad8152aa61874a71889d`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:159146558a8886c194949b59ed673c4f0452bea94d1a1c724370a4c34c36da75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66977c934fed5ef8431b58c0c5587dc0406f64011bd1cde63c9c3db014689bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b83e1df08b7bd59a8114cb5a1696d5684bc65a85edf94e5655c241ada5ebbfff`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 4.4 MB (4386278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f1dcadc949d51c079203807af0a3e63e7d87fb07573cbdde412af9c53c32a5`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 25.8 KB (25809 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.3-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:09df44cc4e7c1d4e37205668cbc30a2e3c62a66081909da51c96d6000d82e75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561263830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe28487fc6798a83a4a647f002e573725b3fe14bcee85e3c1af97670f1a7617a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 23 Jul 2024 08:01:11 GMT
ARG RELEASE
# Tue, 23 Jul 2024 08:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jul 2024 08:01:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Jul 2024 08:01:11 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Tue, 23 Jul 2024 08:01:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 08:01:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 08:01:11 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 23 Jul 2024 08:01:11 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
WORKDIR /apache-storm-2.6.3
# Tue, 23 Jul 2024 08:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Tue, 23 Jul 2024 08:01:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Jul 2024 08:01:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f61f79738faea794be69163a840a5fe9134932adf08d15e3d5ebb38924ed9`  
		Last Modified: Sat, 17 Aug 2024 01:36:25 GMT  
		Size: 46.7 MB (46746363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c7f0bf0755dc5879a47b869ca41b59f0bf14893cb8f129d64b37687b61dc79`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0e0a5bd6de285f3d8b20e89ba1ffdf12683a5db287ebf9c8bf487734a12e1d`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06211b1876d49a0cd2dd0bbd57a90f92f413f2860882fb57b1524850919eebd5`  
		Last Modified: Sat, 17 Aug 2024 08:53:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9fb662a3809fe120d691bdafe6f32d5c962754ddab5ede45171043dc0efc49`  
		Last Modified: Sat, 17 Aug 2024 08:53:24 GMT  
		Size: 15.4 MB (15350303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8efba2f09441803f507fa5a44139346412c89845a8b59642aaae7b30fb0892`  
		Last Modified: Sat, 17 Aug 2024 08:53:32 GMT  
		Size: 455.5 MB (455457497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da812641b30443e12752072db3b6cda3deabb99973470eeb40c6219aa77b8dfc`  
		Last Modified: Sat, 17 Aug 2024 08:53:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:06f6a72bbb1fef31f5356afa5f9263016f7d8d699038bb7b7bd13c779a890431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd139273deb8fc7d445fec694a509ef90ffa1d050b9fff5fe0cff8c778db5a1`

```dockerfile
```

-	Layers:
	-	`sha256:e36ac3bb4eff47eaba76ef82f84c35aca0ee77d1dbf2d63d7fb4a53a77e161a3`  
		Last Modified: Sat, 17 Aug 2024 08:53:23 GMT  
		Size: 4.4 MB (4387390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd8073d65c15211c0c41ff417b14e1ed3536dfc0417f2ffc3068c041dc422a2`  
		Last Modified: Sat, 17 Aug 2024 08:53:22 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:latest`

```console
$ docker pull storm@sha256:2857a93cf91c2b78b22327839b33edcddf01505e130eabb182ee7da2b2728a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:2268f0de84651710a28bd607072bfd00c2c6823e675696b1f768d26e0dee5791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562562807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f099011f4fc5b1e5f19c48ca3a8d877f9b7cd919ea7fc49910b1674245f550`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1446bd8cee8f27f4c8bda23153d6e37cb9cdcff70593cdd1adcf4ceca726f1dc`  
		Last Modified: Sat, 17 Aug 2024 01:12:19 GMT  
		Size: 47.2 MB (47199108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac061cc6e1044c785cf2248ed48fce7f1f78d7ebcc3b9ef5c0542e2f4153c05`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfeb172632de8cd209bc3782f7da0cb2e11055d9ca34616d49eae145fc92ea3`  
		Last Modified: Sat, 17 Aug 2024 01:12:13 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d00e698885cec41ea01ff9a9cb2e1284a6228b6b6168c77a243ad29310f71d3`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6e1a785da97a827788d8db3383a60e2d4bc56b31769155ad2623333d82891f`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 15.6 MB (15568139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e99ad25d5f73afff3cf1c19798505420d1307235bd14c394f02c94c1ffa2fa8`  
		Last Modified: Sat, 17 Aug 2024 02:03:29 GMT  
		Size: 455.5 MB (455457458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7c3a1314bd66b0aa562b0781ec25e2dab171dff418781fda8f2e0903e815d4`  
		Last Modified: Sat, 17 Aug 2024 02:03:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:bef5d56ae800f378406be1223924f75b1a7fc27c217cb147df905fe7f62bbedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59ebdadde7d581395853003d4087623ccb8f3eec4abfc1f359aa1c1cae973ac`

```dockerfile
```

-	Layers:
	-	`sha256:c2656a5438e69eca18b8eaf8c35d00befa7095cb8c5bf39ab179828290af29ff`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 4.4 MB (4386550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bc67dcc9acd7eb26849218f55f94c8ef7ed9a3348fdfbe344b63432f8f6603`  
		Last Modified: Sat, 17 Aug 2024 02:03:21 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:51cbcd94278a7c142ddbd36168fa119273051c4a6ec32f9cb460fc1eff920638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560074565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e18fd4cfd3cb64d72943655a71af3504c65a9bee2ef43d012abd162842ff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jul 2024 05:47:29 GMT
ARG RELEASE
# Fri, 26 Jul 2024 05:47:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Jul 2024 05:47:29 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 26 Jul 2024 05:47:29 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 26 Jul 2024 05:47:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 26 Jul 2024 05:47:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Fri, 26 Jul 2024 05:47:29 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ARG DISTRO_NAME=apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
# ARGS: DISTRO_NAME=apache-storm-2.6.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
WORKDIR /apache-storm-2.6.3
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.6.3/bin
# Fri, 26 Jul 2024 05:47:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b88ddb4ecf5fe246bba6257227ea360765bf7e5e84b39bd3714c3139887b03`  
		Last Modified: Sat, 17 Aug 2024 01:35:13 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e182d345c31d609002a84f011563d867f930b0a47a22a00917ffbad20b4c2e`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36eb2eff38509e12ca963f9f32593dc436f59d4f4ed19d96cf4e58a4755e467f`  
		Last Modified: Sat, 17 Aug 2024 01:35:07 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1034b0611d3f9e5ba81dadbf4bffed1bdccbb09853ed1bc01f0353bf038845f`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6a08a6616de2afc023e5637400c414545b901e0d37c287458d5d5ae18604bd`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 15.4 MB (15350162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca83cdbde2e155cfab3907f338380b0c4ae412f3f86df1bad479db156f54f0`  
		Last Modified: Sat, 17 Aug 2024 08:52:03 GMT  
		Size: 455.5 MB (455457501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a9029d9361567c7e0710cc749505f6afafa12a9ae8f9151e995524ddeb217`  
		Last Modified: Sat, 17 Aug 2024 08:51:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:3ecbae98ced4048e004f52abfca8d23054c390a7207ac5b80c87d28201879f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9413a3679e89252257155fcdf7fedccd332e917390f28c9351932760f6ffd39b`

```dockerfile
```

-	Layers:
	-	`sha256:cf0ed57d7c42f684765461708f3b50efbcfe5e2df09ecd8fc7003cd72efdecfa`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 4.4 MB (4387674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8894dee9fee7627bdec65a86ce7aad36f4a02c7a16becae587ade9df23308`  
		Last Modified: Sat, 17 Aug 2024 08:51:53 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json
