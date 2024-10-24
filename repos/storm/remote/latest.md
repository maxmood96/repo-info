## `storm:latest`

```console
$ docker pull storm@sha256:772552d1d90a21e13a166728fa63c3cec2530ff67d7cc4f7ff5d4aae66f995e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:4a7fe5274a98a46e22084b8a399729fbbdb71d35efaedd23b4454f94fdf09e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573921352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8796755c3de2b9a88d00efc27658d312d021c16450dc2ee1440397977ae8d0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Mon, 21 Oct 2024 06:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 21 Oct 2024 06:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 06:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 21 Oct 2024 06:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Mon, 21 Oct 2024 06:24:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 21 Oct 2024 06:24:32 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 21 Oct 2024 06:24:32 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ARG DISTRO_NAME=apache-storm-2.7.0
# Mon, 21 Oct 2024 06:24:32 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
WORKDIR /apache-storm-2.7.0
# Mon, 21 Oct 2024 06:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.0/bin
# Mon, 21 Oct 2024 06:24:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d226423ace4f7e2a9a147b94766dfe94a7b10da42c2bc79cb22cbd0400b6bb24`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 17.0 MB (16965885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46866a8ee5fb664782ffd2090bf4d1ca1239cd09a0667151ed30f685087527aa`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 47.2 MB (47216864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6b874ebfb34b6cc3d90ffd878c534e09c6fb1bd41aa433f562d58a0e98b29a`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67a6c702afab78cebd1afe63a1e9b4fa04421336ddd51b08db9f458a907fb2a`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a1c04d6eefae42f20296f3882aff44e25e2bb9b3f7876bc76754c924c5e3e`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c2551840925b0f48e0dbd1feb28a67868b5d85b30f938e6212e1a2f0adbffb`  
		Last Modified: Thu, 24 Oct 2024 02:01:21 GMT  
		Size: 12.4 MB (12383087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d19f606d8d27eed359ad7bd9519f2b6152cf51bbf5ae85cc91ed5a1c611a76e`  
		Last Modified: Thu, 24 Oct 2024 02:01:27 GMT  
		Size: 467.6 MB (467601007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4644159fab7747131cb540bbd1f4fe9353862ac8e995c2a8e29a2d4b8cadf14b`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:301df2096acef1dfa305a9704903314907ea22cabfd1652ef1ddf400e37ad37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5f0c1f3ef6e95599c7103a49b0e6264001af9845b7d43d21b1c419e74e14ab`

```dockerfile
```

-	Layers:
	-	`sha256:120d7422f1e79faa6126b8e1fc4f8deb98496a87fd0f83a7de25fbcd79da5ee7`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 4.6 MB (4579710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b800ee922151df725c7684c7d2650c6c2433a681e17f5d98ffdcc049721753d3`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:a976bce09be383c391bc0bf932a525edcc9935c5cf74de28bc669506009ff38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.2 MB (571199001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a067fd612f3dbbf02ea34e98115c8b87508b737e1552aacd4854c85380fd34`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
# Mon, 21 Oct 2024 06:24:32 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 21 Oct 2024 06:24:32 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ARG DISTRO_NAME=apache-storm-2.7.0
# Mon, 21 Oct 2024 06:24:32 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
WORKDIR /apache-storm-2.7.0
# Mon, 21 Oct 2024 06:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.0/bin
# Mon, 21 Oct 2024 06:24:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 21 Oct 2024 06:24:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9167b640d3e58541cc8442550c4e9c19ce0e06adc5f1ca5fafc951f607c9c559`  
		Last Modified: Sat, 19 Oct 2024 05:34:18 GMT  
		Size: 45.6 MB (45557065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ce5c76e592832a6cb77d5cdc9fc7184b02f84f78ddc1b7d3817d4ed574ff2`  
		Last Modified: Sat, 19 Oct 2024 05:34:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4c73365827b09d264ead8baf5838bad8c2d4fab6e2a09e2914f3a7cf70a67`  
		Last Modified: Sat, 19 Oct 2024 05:34:15 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6ebf0675bd7602ecca1c472b3c34d433a2fdef44244a7060501c9090f16449`  
		Last Modified: Sat, 19 Oct 2024 10:43:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4146236e3f690cefb237f1831d905bf9a5f8997fff3fb20f15e64b7d65459`  
		Last Modified: Sat, 19 Oct 2024 10:43:46 GMT  
		Size: 15.4 MB (15354849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13492abb618122330818e65002ae4bb2e307d313f45b5a41641f107097bbf71`  
		Last Modified: Mon, 21 Oct 2024 18:48:17 GMT  
		Size: 467.6 MB (467601199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1983bb7ecf86ecfcc080d3fcef8c3cc80ed700657125b6a6c468a4a470d71ef2`  
		Last Modified: Mon, 21 Oct 2024 18:48:06 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:762d7b0706f40e91b72511a5d84a50530c45cfc7669a6114987a3c6a37041af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1f4e50ef643a4a4f8a05be97d2d7c8b9243e8aa49d4c5e6aa87a039d256544`

```dockerfile
```

-	Layers:
	-	`sha256:821e768b1565fdf9259115fa9c212add4e78cc0bf165e11bd3f78ed7c59e4a37`  
		Last Modified: Mon, 21 Oct 2024 18:48:07 GMT  
		Size: 4.6 MB (4580834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc1688ad138f2929892a7e8c3764c9c8a97f3cb509b00541fc59f9863dfe027`  
		Last Modified: Mon, 21 Oct 2024 18:48:06 GMT  
		Size: 26.1 KB (26119 bytes)  
		MIME: application/vnd.in-toto+json
