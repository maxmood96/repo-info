## `storm:latest`

```console
$ docker pull storm@sha256:4162ddadee2d88a812ddd08d96cd7ab99275f5bc1be1a5e7b7dfa4895d920347
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:f616c233ac547aee85a418dc7031b9dbcd93d1f5759ffc1cadd0fd75ef1f987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562564050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a11e271887bdb7d4a18c1f26ed2e665df163d144720952103efc58bc5c1729a`
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
# Fri, 26 Jul 2024 05:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 05:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:85c96e28aca79c12aba4fc24b218d1c756ca57916bf9fd69e501a1a032e0c2d4`  
		Last Modified: Fri, 23 Aug 2024 19:26:32 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89279e1afa303d4b89f7c33e39bd6c780607f9c8aa1f7fa7b6642e2d02566f8`  
		Last Modified: Fri, 23 Aug 2024 20:07:13 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d614a7bd22817b210232f951630cd0bb35390eddcc26d5f9934dbff9275c8dd`  
		Last Modified: Fri, 23 Aug 2024 20:07:14 GMT  
		Size: 15.6 MB (15569115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d1e094d384a69afd4fce8813dccf39298d556443e1fe1fdb06ba0c54d74745`  
		Last Modified: Fri, 23 Aug 2024 20:07:20 GMT  
		Size: 455.5 MB (455457484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc98afd7c7670e13a4439a3c357022351ba4835bf3ae9541fc89e73e7fb1e349`  
		Last Modified: Fri, 23 Aug 2024 20:07:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:a7d4fd621a749602e07a172b43c27dffcff8782cf7de5e66ef1bac3fbb90f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1458b29bb612a3d3f449a0a140f25d3ce43491ed93bc0744b3163935f64a93ae`

```dockerfile
```

-	Layers:
	-	`sha256:5802422e07139bbad4165fe7879f78a37ba7fa9bc374a13129d97a629ec45d28`  
		Last Modified: Fri, 23 Aug 2024 20:07:13 GMT  
		Size: 4.4 MB (4386550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd38590a93da17c08a8bbbf8510da69917d758947ec079e7b8b556043d3287d`  
		Last Modified: Fri, 23 Aug 2024 20:07:13 GMT  
		Size: 26.0 KB (25953 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:4f57c0e5dd73e1972e4c9a0be5e2bd6022545341f7bbc309857c133d0a805c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560075392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92362731064af4745678664f69cdb26238cb068a003a367448e83039f38f5ef9`
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
# Fri, 26 Jul 2024 05:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Jul 2024 05:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 05:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Jul 2024 05:47:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:a425539f0beac0df59a737e3762a22071b6121f3c1b0f95ac8323c4c33bb2f47`  
		Last Modified: Fri, 23 Aug 2024 19:44:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a28afef8d117c178ab43ea5f47354d6eb0c8d13da0e8aa2f99d2cda3fad357`  
		Last Modified: Sat, 24 Aug 2024 01:25:01 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cd4024e5f6e8bc20c3b1cda169797c440e303f04054af63f18dfb649c1d3a3`  
		Last Modified: Sat, 24 Aug 2024 01:25:03 GMT  
		Size: 15.4 MB (15350773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77735d2f3edb1cab4a27e296580b047e95c9a6d6d07ece618eac265ee640d1e7`  
		Last Modified: Sat, 24 Aug 2024 01:25:11 GMT  
		Size: 455.5 MB (455457468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d2a0abf5230cecc4e12f319bd5d68f940743b33b7bb91ae2264bd949f938`  
		Last Modified: Sat, 24 Aug 2024 01:25:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:b06f2b033769a049ac2aa9e35aae2124a4d1273fbd8c46e80d988b3bb98fce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c0fdc68dff79f093c7096b5ea7c5dab019cf5c9843096e7247189344feeae0`

```dockerfile
```

-	Layers:
	-	`sha256:6c95bdea6d34ada9e11f71a87d32a5e68b12944b4eab59bdd3dd4ac0045d3f9b`  
		Last Modified: Sat, 24 Aug 2024 01:25:01 GMT  
		Size: 4.4 MB (4387674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e76cfd6fa0c63fc8ed054f1e36d48fc5bf5333d9a616498863a664f756d78b`  
		Last Modified: Sat, 24 Aug 2024 01:25:01 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json
