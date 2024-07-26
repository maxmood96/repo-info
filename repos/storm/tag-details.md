<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:2.6`](#storm26)
-	[`storm:2.6-jre17`](#storm26-jre17)
-	[`storm:2.6.3`](#storm263)
-	[`storm:2.6.3-jre17`](#storm263-jre17)
-	[`storm:latest`](#stormlatest)

## `storm:2.6`

```console
$ docker pull storm@sha256:49b5609cb361380e8894cf1bb2104eb6b734624df49a2cb2557e3e29f8071b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6` - linux; amd64

```console
$ docker pull storm@sha256:fb4efccb11ccfee3c6d6290ee8d9e106583ca92bd701b5c63ad11aa48ed4c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562556600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b5b4b81b2292268e2c29c24724c8712091d4f961c2f6e68339964d055342a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e099afec730878428840c0d2f264142aa67639bafa6800aef3c8e64142fa7`  
		Last Modified: Wed, 24 Jul 2024 01:28:45 GMT  
		Size: 47.2 MB (47199067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044a01badf8dcf28102bb2f45b15a1c5365bd268eeca75ab1806bb2d9eac7ca6`  
		Last Modified: Wed, 24 Jul 2024 01:28:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8566ef7b73d970e8d4d569565e9b14cee8d66b8fdb354365b224446f0a3a2c84`  
		Last Modified: Thu, 25 Jul 2024 17:29:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6b5d5dece52081692e222c0695307fad1a3e20784e5e0b300875e60f28e11`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d2ed12cd9fe9e667e432e7199cec4713891af4a5c7ebc5670b8d4ef76ad76`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 15.6 MB (15564070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27ed3c089288e04766256c43e7501bf908364bee503e0e4525c52d25131112`  
		Last Modified: Fri, 26 Jul 2024 17:57:04 GMT  
		Size: 455.5 MB (455457504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224d19760e215b1a83d9330f9762f5630cd599c486da7d6243043aa2848e4209`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:b6a95c517a049e6fc2f963bcd2529bf207009228ea01db0954cec00639748e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fcb334b0bfb0176b3570164a75b0ed8c92f7fec1fe6d068196c1add7478eec`

```dockerfile
```

-	Layers:
	-	`sha256:14ca67eda10922bbea3710b31908ece34c2341b744f1d03bae90f4353a65982b`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 4.4 MB (4386342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06e9bb282c289e2a9c3cc3fd40c776d578b49b012732542f6c166e196c83b7`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:1258e068dc89774a073b22587b72dbd7a51aa59eaff194893e9c1b84e7346c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560064617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151bee215870a3ae94646b7b6be9b2ea559e00c5f49bb3b789715f83e862704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fa0f182b10a5408a16f357489563b2063f57d1a29e3a980f22b7c7a3b504ba`  
		Last Modified: Wed, 24 Jul 2024 00:52:04 GMT  
		Size: 45.6 MB (45557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e01fb2c2ac99676381b49f4880b2b6bc2ea1137cea03d7d4c2115b157a7aec3`  
		Last Modified: Wed, 24 Jul 2024 00:51:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdedded73abbf17c0e92c96408b63ccd7eb1089cd27f30d140e78496f3263e`  
		Last Modified: Thu, 25 Jul 2024 17:45:28 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3bd03e48f6e67d07d054a5adf8f989e69867be4283be43f4942165b00e52c1`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3c6269498ae71518f668cd38f8cca271671258a8ab1f1e967d1af1ecf4114`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 15.3 MB (15342630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17fb833970e5a40d19fb3647d28b122c9c4f9cad448a8751363d6f1ff72db7`  
		Last Modified: Fri, 26 Jul 2024 17:58:15 GMT  
		Size: 455.5 MB (455457529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355bd289a2d5c760610504aaad64b184d18d3e36a946a5ae101a199862ddb108`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6` - unknown; unknown

```console
$ docker pull storm@sha256:03f1779b71be0f0a83ad23f99ae997c0261e119314abb4e3a20f024ed63be81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba675c5c6631fa67d0ebdda6a29f2e2fa9a6222b78fadf6033657ade20f0fd8`

```dockerfile
```

-	Layers:
	-	`sha256:748d4f65c583f258ec1d309356e6ee9ddd1eac8d7f0ae41f12408da8e5e934a3`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 4.4 MB (4387476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e9d3cab8a185fba8bc7ed649709e37a54e132793ece22f0b84dbfe307defb5`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6-jre17`

```console
$ docker pull storm@sha256:3e71b0325e84841d1a2f41bcb5b58a3e3b6b504a20dfc8cbe03abb6861b670a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6-jre17` - linux; amd64

```console
$ docker pull storm@sha256:1d6534e265922315e6482258e9e48e02e69eb8fa9d59321cff3010bf688ae0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562637634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801b122ea3c8ae1db33e2ec213292605f85aab8b9c2a4192af2d30604b2bcc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced013eec6cb5fa5c1146b85b09e19552a5b54474297bbaeba8a333739bbbbef`  
		Last Modified: Tue, 23 Jul 2024 01:09:03 GMT  
		Size: 47.3 MB (47280194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73663ebb99d0b0749c0e265014cd2e9a976615d5b102f5d5d69b141899661e7f`  
		Last Modified: Tue, 23 Jul 2024 01:08:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083ab7049b9d911a90609cf0790cf4715c8edc0c0ec4a7447210b0f302e562`  
		Last Modified: Thu, 25 Jul 2024 17:30:44 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d640dc901f690deb28b1a07a9215793e6fd229bc91a8b18f9d8d47621ee759cd`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e876ee7a7111d3d4bdf09b835d86250fa3c648cde2fe8a01e92c0140c0ab8d`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 15.6 MB (15564003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678710695fe1958923ff134cb78b65f88832ca249db525ee308ed3a113d26c04`  
		Last Modified: Thu, 25 Jul 2024 19:14:37 GMT  
		Size: 455.5 MB (455457474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe81fda2dee6b5e11a677169730e66ca8b0f8656e09e77bda06c473aadd225b`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:5164d1ef35958811938516764205999e0b6f907687211c0ff5cf78d5086f1073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4411884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0cecf1aba5fb1a20826fa157430afc1fb45e92a8d0437ea3ce7df7d70be373`

```dockerfile
```

-	Layers:
	-	`sha256:0d394de04df6bb29ce15b2533cb3ebe53f3cfb8030a0ad297d5b9dbb71ea2778`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 4.4 MB (4386075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc877238b91f4131594e4401d5a2d85e3b8f7f5d3e782792b760878eb1969e48`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 25.8 KB (25809 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:d0aca9c8b3bd7a5d9041ed099d7e39fe535b083b162a647fd6b1bafa6ce4cf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561253476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33657f056b4127001b626a4fcc631efb30cd79f6b4c0984c5c6ae4031ef9f243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e1b72ba4c1374ee7def94c45e1f16cacc330b2d3e90ca790d283de5db18cb8`  
		Last Modified: Tue, 23 Jul 2024 04:14:18 GMT  
		Size: 46.7 MB (46746369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e9b14b806a8f1a54d78e10962c1460615fa346fbea1aeb53c168a9807e5a7e`  
		Last Modified: Tue, 23 Jul 2024 04:14:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85331be2ec25884f920b5a4938bc420e89eddfe3915d32e7aab3ec5460a9adb`  
		Last Modified: Thu, 25 Jul 2024 17:46:26 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844575c678f805cf81d9c360ab485b3b29dd869b70f2280a46179ce6683a1ac`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ea9fe94d6c9f3dd496975a7990f3962db1c73da5a5cb3c2ef84246907f8689`  
		Last Modified: Thu, 25 Jul 2024 23:11:49 GMT  
		Size: 15.3 MB (15342477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fea1225e74c81c57ebf9c46b7678aeab7fff4c9bf4f00463cc337d997ece84`  
		Last Modified: Thu, 25 Jul 2024 23:11:57 GMT  
		Size: 455.5 MB (455457470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5410ba6eb2b76558ec703a9071b1c9396cdc6caa315adddedb92d19823ae6c88`  
		Last Modified: Thu, 25 Jul 2024 23:11:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:e4343f877ef88eaa3bfe32d4dc033c91eabf8887e1b12d1239b40c4b87138742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb7f94fdd80aab1c3d6bb5359f5c2e3ae733f6068aef3bfdb26a55c869a24c`

```dockerfile
```

-	Layers:
	-	`sha256:df8be2ff779a5c54f561699edac772d7c02c4d8630cf604014020f0976728b3d`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 4.4 MB (4387197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593269837b26412e267518fa115c491ad8a64e67e78c56723cfcdc7950c0684d`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.3`

```console
$ docker pull storm@sha256:49b5609cb361380e8894cf1bb2104eb6b734624df49a2cb2557e3e29f8071b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.3` - linux; amd64

```console
$ docker pull storm@sha256:fb4efccb11ccfee3c6d6290ee8d9e106583ca92bd701b5c63ad11aa48ed4c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562556600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b5b4b81b2292268e2c29c24724c8712091d4f961c2f6e68339964d055342a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e099afec730878428840c0d2f264142aa67639bafa6800aef3c8e64142fa7`  
		Last Modified: Wed, 24 Jul 2024 01:28:45 GMT  
		Size: 47.2 MB (47199067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044a01badf8dcf28102bb2f45b15a1c5365bd268eeca75ab1806bb2d9eac7ca6`  
		Last Modified: Wed, 24 Jul 2024 01:28:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8566ef7b73d970e8d4d569565e9b14cee8d66b8fdb354365b224446f0a3a2c84`  
		Last Modified: Thu, 25 Jul 2024 17:29:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6b5d5dece52081692e222c0695307fad1a3e20784e5e0b300875e60f28e11`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d2ed12cd9fe9e667e432e7199cec4713891af4a5c7ebc5670b8d4ef76ad76`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 15.6 MB (15564070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27ed3c089288e04766256c43e7501bf908364bee503e0e4525c52d25131112`  
		Last Modified: Fri, 26 Jul 2024 17:57:04 GMT  
		Size: 455.5 MB (455457504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224d19760e215b1a83d9330f9762f5630cd599c486da7d6243043aa2848e4209`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3` - unknown; unknown

```console
$ docker pull storm@sha256:b6a95c517a049e6fc2f963bcd2529bf207009228ea01db0954cec00639748e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fcb334b0bfb0176b3570164a75b0ed8c92f7fec1fe6d068196c1add7478eec`

```dockerfile
```

-	Layers:
	-	`sha256:14ca67eda10922bbea3710b31908ece34c2341b744f1d03bae90f4353a65982b`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 4.4 MB (4386342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06e9bb282c289e2a9c3cc3fd40c776d578b49b012732542f6c166e196c83b7`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.3` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:1258e068dc89774a073b22587b72dbd7a51aa59eaff194893e9c1b84e7346c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560064617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151bee215870a3ae94646b7b6be9b2ea559e00c5f49bb3b789715f83e862704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fa0f182b10a5408a16f357489563b2063f57d1a29e3a980f22b7c7a3b504ba`  
		Last Modified: Wed, 24 Jul 2024 00:52:04 GMT  
		Size: 45.6 MB (45557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e01fb2c2ac99676381b49f4880b2b6bc2ea1137cea03d7d4c2115b157a7aec3`  
		Last Modified: Wed, 24 Jul 2024 00:51:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdedded73abbf17c0e92c96408b63ccd7eb1089cd27f30d140e78496f3263e`  
		Last Modified: Thu, 25 Jul 2024 17:45:28 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3bd03e48f6e67d07d054a5adf8f989e69867be4283be43f4942165b00e52c1`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3c6269498ae71518f668cd38f8cca271671258a8ab1f1e967d1af1ecf4114`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 15.3 MB (15342630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17fb833970e5a40d19fb3647d28b122c9c4f9cad448a8751363d6f1ff72db7`  
		Last Modified: Fri, 26 Jul 2024 17:58:15 GMT  
		Size: 455.5 MB (455457529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355bd289a2d5c760610504aaad64b184d18d3e36a946a5ae101a199862ddb108`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3` - unknown; unknown

```console
$ docker pull storm@sha256:03f1779b71be0f0a83ad23f99ae997c0261e119314abb4e3a20f024ed63be81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba675c5c6631fa67d0ebdda6a29f2e2fa9a6222b78fadf6033657ade20f0fd8`

```dockerfile
```

-	Layers:
	-	`sha256:748d4f65c583f258ec1d309356e6ee9ddd1eac8d7f0ae41f12408da8e5e934a3`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 4.4 MB (4387476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e9d3cab8a185fba8bc7ed649709e37a54e132793ece22f0b84dbfe307defb5`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.6.3-jre17`

```console
$ docker pull storm@sha256:3e71b0325e84841d1a2f41bcb5b58a3e3b6b504a20dfc8cbe03abb6861b670a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.6.3-jre17` - linux; amd64

```console
$ docker pull storm@sha256:1d6534e265922315e6482258e9e48e02e69eb8fa9d59321cff3010bf688ae0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562637634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801b122ea3c8ae1db33e2ec213292605f85aab8b9c2a4192af2d30604b2bcc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced013eec6cb5fa5c1146b85b09e19552a5b54474297bbaeba8a333739bbbbef`  
		Last Modified: Tue, 23 Jul 2024 01:09:03 GMT  
		Size: 47.3 MB (47280194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73663ebb99d0b0749c0e265014cd2e9a976615d5b102f5d5d69b141899661e7f`  
		Last Modified: Tue, 23 Jul 2024 01:08:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083ab7049b9d911a90609cf0790cf4715c8edc0c0ec4a7447210b0f302e562`  
		Last Modified: Thu, 25 Jul 2024 17:30:44 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d640dc901f690deb28b1a07a9215793e6fd229bc91a8b18f9d8d47621ee759cd`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e876ee7a7111d3d4bdf09b835d86250fa3c648cde2fe8a01e92c0140c0ab8d`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 15.6 MB (15564003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678710695fe1958923ff134cb78b65f88832ca249db525ee308ed3a113d26c04`  
		Last Modified: Thu, 25 Jul 2024 19:14:37 GMT  
		Size: 455.5 MB (455457474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe81fda2dee6b5e11a677169730e66ca8b0f8656e09e77bda06c473aadd225b`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:5164d1ef35958811938516764205999e0b6f907687211c0ff5cf78d5086f1073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4411884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0cecf1aba5fb1a20826fa157430afc1fb45e92a8d0437ea3ce7df7d70be373`

```dockerfile
```

-	Layers:
	-	`sha256:0d394de04df6bb29ce15b2533cb3ebe53f3cfb8030a0ad297d5b9dbb71ea2778`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 4.4 MB (4386075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc877238b91f4131594e4401d5a2d85e3b8f7f5d3e782792b760878eb1969e48`  
		Last Modified: Thu, 25 Jul 2024 19:14:31 GMT  
		Size: 25.8 KB (25809 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.6.3-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:d0aca9c8b3bd7a5d9041ed099d7e39fe535b083b162a647fd6b1bafa6ce4cf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561253476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33657f056b4127001b626a4fcc631efb30cd79f6b4c0984c5c6ae4031ef9f243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e1b72ba4c1374ee7def94c45e1f16cacc330b2d3e90ca790d283de5db18cb8`  
		Last Modified: Tue, 23 Jul 2024 04:14:18 GMT  
		Size: 46.7 MB (46746369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e9b14b806a8f1a54d78e10962c1460615fa346fbea1aeb53c168a9807e5a7e`  
		Last Modified: Tue, 23 Jul 2024 04:14:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85331be2ec25884f920b5a4938bc420e89eddfe3915d32e7aab3ec5460a9adb`  
		Last Modified: Thu, 25 Jul 2024 17:46:26 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844575c678f805cf81d9c360ab485b3b29dd869b70f2280a46179ce6683a1ac`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ea9fe94d6c9f3dd496975a7990f3962db1c73da5a5cb3c2ef84246907f8689`  
		Last Modified: Thu, 25 Jul 2024 23:11:49 GMT  
		Size: 15.3 MB (15342477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fea1225e74c81c57ebf9c46b7678aeab7fff4c9bf4f00463cc337d997ece84`  
		Last Modified: Thu, 25 Jul 2024 23:11:57 GMT  
		Size: 455.5 MB (455457470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5410ba6eb2b76558ec703a9071b1c9396cdc6caa315adddedb92d19823ae6c88`  
		Last Modified: Thu, 25 Jul 2024 23:11:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.6.3-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:e4343f877ef88eaa3bfe32d4dc033c91eabf8887e1b12d1239b40c4b87138742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb7f94fdd80aab1c3d6bb5359f5c2e3ae733f6068aef3bfdb26a55c869a24c`

```dockerfile
```

-	Layers:
	-	`sha256:df8be2ff779a5c54f561699edac772d7c02c4d8630cf604014020f0976728b3d`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 4.4 MB (4387197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593269837b26412e267518fa115c491ad8a64e67e78c56723cfcdc7950c0684d`  
		Last Modified: Thu, 25 Jul 2024 23:11:48 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:latest`

```console
$ docker pull storm@sha256:49b5609cb361380e8894cf1bb2104eb6b734624df49a2cb2557e3e29f8071b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:fb4efccb11ccfee3c6d6290ee8d9e106583ca92bd701b5c63ad11aa48ed4c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.6 MB (562556600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b5b4b81b2292268e2c29c24724c8712091d4f961c2f6e68339964d055342a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e099afec730878428840c0d2f264142aa67639bafa6800aef3c8e64142fa7`  
		Last Modified: Wed, 24 Jul 2024 01:28:45 GMT  
		Size: 47.2 MB (47199067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044a01badf8dcf28102bb2f45b15a1c5365bd268eeca75ab1806bb2d9eac7ca6`  
		Last Modified: Wed, 24 Jul 2024 01:28:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8566ef7b73d970e8d4d569565e9b14cee8d66b8fdb354365b224446f0a3a2c84`  
		Last Modified: Thu, 25 Jul 2024 17:29:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6b5d5dece52081692e222c0695307fad1a3e20784e5e0b300875e60f28e11`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d2ed12cd9fe9e667e432e7199cec4713891af4a5c7ebc5670b8d4ef76ad76`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 15.6 MB (15564070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27ed3c089288e04766256c43e7501bf908364bee503e0e4525c52d25131112`  
		Last Modified: Fri, 26 Jul 2024 17:57:04 GMT  
		Size: 455.5 MB (455457504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224d19760e215b1a83d9330f9762f5630cd599c486da7d6243043aa2848e4209`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:b6a95c517a049e6fc2f963bcd2529bf207009228ea01db0954cec00639748e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4412294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fcb334b0bfb0176b3570164a75b0ed8c92f7fec1fe6d068196c1add7478eec`

```dockerfile
```

-	Layers:
	-	`sha256:14ca67eda10922bbea3710b31908ece34c2341b744f1d03bae90f4353a65982b`  
		Last Modified: Fri, 26 Jul 2024 17:56:50 GMT  
		Size: 4.4 MB (4386342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06e9bb282c289e2a9c3cc3fd40c776d578b49b012732542f6c166e196c83b7`  
		Last Modified: Fri, 26 Jul 2024 17:56:49 GMT  
		Size: 26.0 KB (25952 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:1258e068dc89774a073b22587b72dbd7a51aa59eaff194893e9c1b84e7346c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.1 MB (560064617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151bee215870a3ae94646b7b6be9b2ea559e00c5f49bb3b789715f83e862704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fa0f182b10a5408a16f357489563b2063f57d1a29e3a980f22b7c7a3b504ba`  
		Last Modified: Wed, 24 Jul 2024 00:52:04 GMT  
		Size: 45.6 MB (45557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e01fb2c2ac99676381b49f4880b2b6bc2ea1137cea03d7d4c2115b157a7aec3`  
		Last Modified: Wed, 24 Jul 2024 00:51:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdedded73abbf17c0e92c96408b63ccd7eb1089cd27f30d140e78496f3263e`  
		Last Modified: Thu, 25 Jul 2024 17:45:28 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3bd03e48f6e67d07d054a5adf8f989e69867be4283be43f4942165b00e52c1`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3c6269498ae71518f668cd38f8cca271671258a8ab1f1e967d1af1ecf4114`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 15.3 MB (15342630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17fb833970e5a40d19fb3647d28b122c9c4f9cad448a8751363d6f1ff72db7`  
		Last Modified: Fri, 26 Jul 2024 17:58:15 GMT  
		Size: 455.5 MB (455457529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355bd289a2d5c760610504aaad64b184d18d3e36a946a5ae101a199862ddb108`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:03f1779b71be0f0a83ad23f99ae997c0261e119314abb4e3a20f024ed63be81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4413728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba675c5c6631fa67d0ebdda6a29f2e2fa9a6222b78fadf6033657ade20f0fd8`

```dockerfile
```

-	Layers:
	-	`sha256:748d4f65c583f258ec1d309356e6ee9ddd1eac8d7f0ae41f12408da8e5e934a3`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 4.4 MB (4387476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e9d3cab8a185fba8bc7ed649709e37a54e132793ece22f0b84dbfe307defb5`  
		Last Modified: Fri, 26 Jul 2024 17:58:06 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json
