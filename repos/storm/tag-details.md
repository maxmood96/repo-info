<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:2.6`](#storm26)
-	[`storm:2.6-jre17`](#storm26-jre17)
-	[`storm:2.6.4`](#storm264)
-	[`storm:2.6.4-jre17`](#storm264-jre17)
-	[`storm:latest`](#stormlatest)

## `storm:2.6`

```console
$ docker pull storm@sha256:a7392831a762c8060a432fd516e761843d885442ff5f8292d82bde55552ede4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6` - linux; amd64

```console
$ docker pull storm@sha256:3517e151d91880831873616a831a1b25d72d0e9bedf5d237d0755579d88ae82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.1 MB (575055766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c98ea9afa09d667323436822266b3a74144d353059aecbc31bb41f2a637d1a`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148e20661324912f73010e19ed856c35c14f93ce46db7f17d05e5a5bfceedb`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ee163fa13caaa1c8cfafc7a132bfbb8a17892e05a939a2528ff1ca454968d7`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 15.9 MB (15883501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246043daeb9f2e44e1a6a8fd6a4fa90f44615742fa4813fbfca5c5aca53649e`  
		Last Modified: Sat, 12 Oct 2024 00:56:48 GMT  
		Size: 467.6 MB (467584752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b72b5f4ef2c7b515343cda2dd5626f2d679c29500768baa07f453b20de2b6`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:822104a22aa3d5cab3956811f1804ff12fcd939e579e191b2265c55a80d0013c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40588f4ef07be671b51687271aa78f2a31fdf5a3ab0aed1822c54e62d1993d48`

```dockerfile
```

-	Layers:
	-	`sha256:2f522f6005c7c3b87cd41ee57db9c386582601a31b4064df2558847135d6b32a`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 4.5 MB (4473299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11960f18914cc2e0e91ea72f1b29e428ae15f92a305520a9fdfb7f6c487b0581`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 26.0 KB (25990 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:c0425187c1ba38908ec50fbb08dfac6e34b50bbb836c8a33b16424197f54801a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.6 MB (572580508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f44330f5cc53624b4137b88dfc6620024ac26d13d89063f6a0b5a23d940bc9`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a1f6703825bc1ab890a74dbcf6461f732a29cb694c6d7c8c6ad9977ab58df`  
		Last Modified: Wed, 02 Oct 2024 01:26:57 GMT  
		Size: 45.6 MB (45557310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ff191c9dd4f08b1ad924a59b3c126887f036a38c7bad1aae8e12272bbbf93`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85053618bd30c13b6f45f967fb5b27aa26228d70e12cee43591fce42647d7417`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065da0ad0a8405806a7ca77f91b4a228a85b627fd3ca83545769c099bb36988d`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73500d056ba2bcbec3cd44eee8c585c5e9d0b1d2f9050433e6574696ce6cf4a`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 15.7 MB (15683764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3936487f699522430046909021ab76e4b60e799a00eb633eefdc5c571c79ddb5`  
		Last Modified: Wed, 02 Oct 2024 04:20:13 GMT  
		Size: 467.6 MB (467584714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14edcd393f818d54f93fd5ea8ea9c0d2adf4abfdf04c31127fe446b2f3b0fe62`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:881260bc446eeaabf8aba8c8e5b9e502a2b111a1fa184215942e284c1604ba79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a71bf0bff807070d8c4f53b236b4cc29e0a1105ddab22d7214e49b0bbdf41`

```dockerfile
```

-	Layers:
	-	`sha256:c0bf8c2e429983616625c1003ad557287c544c3825c1bc58f88c18c1edaf96bb`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 4.5 MB (4474411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227e4007951a4168537adf6a5077022f2cf9dbf4c151010c45f9af41c82cfbfa`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6-jre17`

```console
$ docker pull storm@sha256:16dfdd0bdc3a02cc703cad4332bcb5bd59860ddad57ea4edef6ae9b69f12ca57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6-jre17` - linux; amd64

```console
$ docker pull storm@sha256:887066e729a3839642ff6d1797966600c5ef502ff9429e9228334949939593c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.1 MB (575137164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8999138cf447887bfb072c27068ee5bea955264c3d18bb5ba34b435cf5ae7b0c`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5bfb8d4474120f18cd4e2e21c2fb6e7d9144d3bfb8f8fdf9016d706eebb88`  
		Last Modified: Fri, 11 Oct 2024 23:57:59 GMT  
		Size: 47.3 MB (47280244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14688e11a21ea2eaa960947d01105ba680fe07492d6eac637d88f964f9396719`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057686f76905cbfe0bc06f7c1af90d04d9dd676958004abc9661ee80c48c23db`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ef863426d8480307c0aaa630a68140822d24c1fd3532778a08b01b8f2b9b38`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b0b555c7a62f2362069871db14d518f858cba0877d57391c3eb1ce3c689c1f`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 15.9 MB (15883477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdb9b3bffa159e5075df10fa2c2486042c627fdf042e811671dbb46544777f`  
		Last Modified: Sat, 12 Oct 2024 00:56:51 GMT  
		Size: 467.6 MB (467584974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b72b5f4ef2c7b515343cda2dd5626f2d679c29500768baa07f453b20de2b6`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:eb3fdf5dbe71fbc30bfe010a2481879dcd3fba0cf4c3b8f6ad2352d2680da1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbea82cc5c687c72d1c8f5d96fe228f3867a77576f5cecb0689ffe635fdf1af`

```dockerfile
```

-	Layers:
	-	`sha256:961f126e2fefe6d8f0e8fef809cc975ae3d79f2814c5aab86c59a6b3f794dac7`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 4.5 MB (4459258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dedbb4418c59e4567efc767bcbb411f20a02f38391bcb637799bb80007dc951`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 25.8 KB (25847 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:55ffb2bcb4909b880dce8700181fde3d4b2fe3084d96f2965c10116b2f906455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.8 MB (573769627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7000ed57fe0c9339f17bac00b34cbd555ce8bd1e1cd812cd220ccb630a105f6`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef2dea2cc9c0dbe3c64710e5ffdcfb21a0f8380212beac56d44e94e1a2802c`  
		Last Modified: Wed, 02 Oct 2024 01:28:02 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ec3778b444f1bb64b53a5f58cb73e31648e1389c755d55b65d2c634c1cd2f`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ca8e8b83ad911aeec2a1f3687e6b549782de3f86048819e24bbc9604a9fd`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9faeb5fab600f5c17cce6e346cf4aebecd7017bb422050d4fe0e51f13e35dcd`  
		Last Modified: Wed, 02 Oct 2024 04:21:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51caaf0969fdb0b0325056b90b5c54dfcff19d831c03ce41ac3da92d012ae63b`  
		Last Modified: Wed, 02 Oct 2024 04:21:37 GMT  
		Size: 15.7 MB (15683735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a57b308fbfdea08e237054b12f537e1c96e4cdfac4439790df8607fdbc85bae`  
		Last Modified: Wed, 02 Oct 2024 04:21:54 GMT  
		Size: 467.6 MB (467584809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57efedfbcb0378359af3143405bd907cc55bfe1070862648795dc33bd862619e`  
		Last Modified: Wed, 02 Oct 2024 04:21:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:0a3bc3bfc85048e5dd8eb637b5d1dc6f7c4f52d70aea41bd205476cf69f389e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22634ce8f2ec616055343d19b5cc73cc9349c09e3d7280174d93ef3a7ef1b7ed`

```dockerfile
```

-	Layers:
	-	`sha256:ebe15261393d274a949175fb5dadce3a3ea78bab3769af39148a1e233d401bd3`  
		Last Modified: Wed, 02 Oct 2024 04:21:36 GMT  
		Size: 4.5 MB (4459739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9a416bfc1d3853525240c387be1d5940f205941e49d81fd6fa31ec521e3fe3`  
		Last Modified: Wed, 02 Oct 2024 04:21:35 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.4`

```console
$ docker pull storm@sha256:a7392831a762c8060a432fd516e761843d885442ff5f8292d82bde55552ede4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.4` - linux; amd64

```console
$ docker pull storm@sha256:3517e151d91880831873616a831a1b25d72d0e9bedf5d237d0755579d88ae82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.1 MB (575055766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c98ea9afa09d667323436822266b3a74144d353059aecbc31bb41f2a637d1a`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148e20661324912f73010e19ed856c35c14f93ce46db7f17d05e5a5bfceedb`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ee163fa13caaa1c8cfafc7a132bfbb8a17892e05a939a2528ff1ca454968d7`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 15.9 MB (15883501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246043daeb9f2e44e1a6a8fd6a4fa90f44615742fa4813fbfca5c5aca53649e`  
		Last Modified: Sat, 12 Oct 2024 00:56:48 GMT  
		Size: 467.6 MB (467584752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b72b5f4ef2c7b515343cda2dd5626f2d679c29500768baa07f453b20de2b6`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4` - unknown; unknown

```console
$ docker pull storm@sha256:822104a22aa3d5cab3956811f1804ff12fcd939e579e191b2265c55a80d0013c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40588f4ef07be671b51687271aa78f2a31fdf5a3ab0aed1822c54e62d1993d48`

```dockerfile
```

-	Layers:
	-	`sha256:2f522f6005c7c3b87cd41ee57db9c386582601a31b4064df2558847135d6b32a`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 4.5 MB (4473299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11960f18914cc2e0e91ea72f1b29e428ae15f92a305520a9fdfb7f6c487b0581`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 26.0 KB (25990 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.4` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:c0425187c1ba38908ec50fbb08dfac6e34b50bbb836c8a33b16424197f54801a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.6 MB (572580508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f44330f5cc53624b4137b88dfc6620024ac26d13d89063f6a0b5a23d940bc9`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a1f6703825bc1ab890a74dbcf6461f732a29cb694c6d7c8c6ad9977ab58df`  
		Last Modified: Wed, 02 Oct 2024 01:26:57 GMT  
		Size: 45.6 MB (45557310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ff191c9dd4f08b1ad924a59b3c126887f036a38c7bad1aae8e12272bbbf93`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85053618bd30c13b6f45f967fb5b27aa26228d70e12cee43591fce42647d7417`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065da0ad0a8405806a7ca77f91b4a228a85b627fd3ca83545769c099bb36988d`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73500d056ba2bcbec3cd44eee8c585c5e9d0b1d2f9050433e6574696ce6cf4a`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 15.7 MB (15683764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3936487f699522430046909021ab76e4b60e799a00eb633eefdc5c571c79ddb5`  
		Last Modified: Wed, 02 Oct 2024 04:20:13 GMT  
		Size: 467.6 MB (467584714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14edcd393f818d54f93fd5ea8ea9c0d2adf4abfdf04c31127fe446b2f3b0fe62`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4` - unknown; unknown

```console
$ docker pull storm@sha256:881260bc446eeaabf8aba8c8e5b9e502a2b111a1fa184215942e284c1604ba79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a71bf0bff807070d8c4f53b236b4cc29e0a1105ddab22d7214e49b0bbdf41`

```dockerfile
```

-	Layers:
	-	`sha256:c0bf8c2e429983616625c1003ad557287c544c3825c1bc58f88c18c1edaf96bb`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 4.5 MB (4474411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227e4007951a4168537adf6a5077022f2cf9dbf4c151010c45f9af41c82cfbfa`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.4-jre17`

```console
$ docker pull storm@sha256:16dfdd0bdc3a02cc703cad4332bcb5bd59860ddad57ea4edef6ae9b69f12ca57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.4-jre17` - linux; amd64

```console
$ docker pull storm@sha256:887066e729a3839642ff6d1797966600c5ef502ff9429e9228334949939593c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.1 MB (575137164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8999138cf447887bfb072c27068ee5bea955264c3d18bb5ba34b435cf5ae7b0c`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5bfb8d4474120f18cd4e2e21c2fb6e7d9144d3bfb8f8fdf9016d706eebb88`  
		Last Modified: Fri, 11 Oct 2024 23:57:59 GMT  
		Size: 47.3 MB (47280244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14688e11a21ea2eaa960947d01105ba680fe07492d6eac637d88f964f9396719`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057686f76905cbfe0bc06f7c1af90d04d9dd676958004abc9661ee80c48c23db`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ef863426d8480307c0aaa630a68140822d24c1fd3532778a08b01b8f2b9b38`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b0b555c7a62f2362069871db14d518f858cba0877d57391c3eb1ce3c689c1f`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 15.9 MB (15883477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdb9b3bffa159e5075df10fa2c2486042c627fdf042e811671dbb46544777f`  
		Last Modified: Sat, 12 Oct 2024 00:56:51 GMT  
		Size: 467.6 MB (467584974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b72b5f4ef2c7b515343cda2dd5626f2d679c29500768baa07f453b20de2b6`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:eb3fdf5dbe71fbc30bfe010a2481879dcd3fba0cf4c3b8f6ad2352d2680da1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbea82cc5c687c72d1c8f5d96fe228f3867a77576f5cecb0689ffe635fdf1af`

```dockerfile
```

-	Layers:
	-	`sha256:961f126e2fefe6d8f0e8fef809cc975ae3d79f2814c5aab86c59a6b3f794dac7`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 4.5 MB (4459258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dedbb4418c59e4567efc767bcbb411f20a02f38391bcb637799bb80007dc951`  
		Last Modified: Sat, 12 Oct 2024 00:56:45 GMT  
		Size: 25.8 KB (25847 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.4-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:55ffb2bcb4909b880dce8700181fde3d4b2fe3084d96f2965c10116b2f906455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.8 MB (573769627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7000ed57fe0c9339f17bac00b34cbd555ce8bd1e1cd812cd220ccb630a105f6`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef2dea2cc9c0dbe3c64710e5ffdcfb21a0f8380212beac56d44e94e1a2802c`  
		Last Modified: Wed, 02 Oct 2024 01:28:02 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ec3778b444f1bb64b53a5f58cb73e31648e1389c755d55b65d2c634c1cd2f`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ca8e8b83ad911aeec2a1f3687e6b549782de3f86048819e24bbc9604a9fd`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9faeb5fab600f5c17cce6e346cf4aebecd7017bb422050d4fe0e51f13e35dcd`  
		Last Modified: Wed, 02 Oct 2024 04:21:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51caaf0969fdb0b0325056b90b5c54dfcff19d831c03ce41ac3da92d012ae63b`  
		Last Modified: Wed, 02 Oct 2024 04:21:37 GMT  
		Size: 15.7 MB (15683735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a57b308fbfdea08e237054b12f537e1c96e4cdfac4439790df8607fdbc85bae`  
		Last Modified: Wed, 02 Oct 2024 04:21:54 GMT  
		Size: 467.6 MB (467584809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57efedfbcb0378359af3143405bd907cc55bfe1070862648795dc33bd862619e`  
		Last Modified: Wed, 02 Oct 2024 04:21:36 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.4-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:0a3bc3bfc85048e5dd8eb637b5d1dc6f7c4f52d70aea41bd205476cf69f389e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22634ce8f2ec616055343d19b5cc73cc9349c09e3d7280174d93ef3a7ef1b7ed`

```dockerfile
```

-	Layers:
	-	`sha256:ebe15261393d274a949175fb5dadce3a3ea78bab3769af39148a1e233d401bd3`  
		Last Modified: Wed, 02 Oct 2024 04:21:36 GMT  
		Size: 4.5 MB (4459739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9a416bfc1d3853525240c387be1d5940f205941e49d81fd6fa31ec521e3fe3`  
		Last Modified: Wed, 02 Oct 2024 04:21:35 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:latest`

```console
$ docker pull storm@sha256:a7392831a762c8060a432fd516e761843d885442ff5f8292d82bde55552ede4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:3517e151d91880831873616a831a1b25d72d0e9bedf5d237d0755579d88ae82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.1 MB (575055766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c98ea9afa09d667323436822266b3a74144d353059aecbc31bb41f2a637d1a`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148e20661324912f73010e19ed856c35c14f93ce46db7f17d05e5a5bfceedb`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ee163fa13caaa1c8cfafc7a132bfbb8a17892e05a939a2528ff1ca454968d7`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 15.9 MB (15883501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246043daeb9f2e44e1a6a8fd6a4fa90f44615742fa4813fbfca5c5aca53649e`  
		Last Modified: Sat, 12 Oct 2024 00:56:48 GMT  
		Size: 467.6 MB (467584752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b72b5f4ef2c7b515343cda2dd5626f2d679c29500768baa07f453b20de2b6`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:822104a22aa3d5cab3956811f1804ff12fcd939e579e191b2265c55a80d0013c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40588f4ef07be671b51687271aa78f2a31fdf5a3ab0aed1822c54e62d1993d48`

```dockerfile
```

-	Layers:
	-	`sha256:2f522f6005c7c3b87cd41ee57db9c386582601a31b4064df2558847135d6b32a`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 4.5 MB (4473299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11960f18914cc2e0e91ea72f1b29e428ae15f92a305520a9fdfb7f6c487b0581`  
		Last Modified: Sat, 12 Oct 2024 00:56:40 GMT  
		Size: 26.0 KB (25990 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:c0425187c1ba38908ec50fbb08dfac6e34b50bbb836c8a33b16424197f54801a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.6 MB (572580508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f44330f5cc53624b4137b88dfc6620024ac26d13d89063f6a0b5a23d940bc9`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a1f6703825bc1ab890a74dbcf6461f732a29cb694c6d7c8c6ad9977ab58df`  
		Last Modified: Wed, 02 Oct 2024 01:26:57 GMT  
		Size: 45.6 MB (45557310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ff191c9dd4f08b1ad924a59b3c126887f036a38c7bad1aae8e12272bbbf93`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85053618bd30c13b6f45f967fb5b27aa26228d70e12cee43591fce42647d7417`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065da0ad0a8405806a7ca77f91b4a228a85b627fd3ca83545769c099bb36988d`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73500d056ba2bcbec3cd44eee8c585c5e9d0b1d2f9050433e6574696ce6cf4a`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 15.7 MB (15683764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3936487f699522430046909021ab76e4b60e799a00eb633eefdc5c571c79ddb5`  
		Last Modified: Wed, 02 Oct 2024 04:20:13 GMT  
		Size: 467.6 MB (467584714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14edcd393f818d54f93fd5ea8ea9c0d2adf4abfdf04c31127fe446b2f3b0fe62`  
		Last Modified: Wed, 02 Oct 2024 04:20:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:881260bc446eeaabf8aba8c8e5b9e502a2b111a1fa184215942e284c1604ba79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a71bf0bff807070d8c4f53b236b4cc29e0a1105ddab22d7214e49b0bbdf41`

```dockerfile
```

-	Layers:
	-	`sha256:c0bf8c2e429983616625c1003ad557287c544c3825c1bc58f88c18c1edaf96bb`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 4.5 MB (4474411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227e4007951a4168537adf6a5077022f2cf9dbf4c151010c45f9af41c82cfbfa`  
		Last Modified: Wed, 02 Oct 2024 04:20:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json
