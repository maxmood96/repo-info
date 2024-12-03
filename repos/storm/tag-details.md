<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:2.7`](#storm27)
-	[`storm:2.7-jre17`](#storm27-jre17)
-	[`storm:2.7.1`](#storm271)
-	[`storm:2.7.1-jre17`](#storm271-jre17)
-	[`storm:latest`](#stormlatest)

## `storm:2.7`

```console
$ docker pull storm@sha256:23dd892ec188a6d44bbeda3f9cb62926252ad3b3dd363181da645140cdd77a54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.7` - linux; amd64

```console
$ docker pull storm@sha256:1d1573425ab184016622eb813da7abf6412acc092438b54f1865dad52d8faa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.4 MB (598403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947e54979dce5877c3e1f96bcddd161798db96cbca578e7dd6df0a532c5265c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee5e42e638331b77b0e5463a888e36cf34c74dc011204a42fbaa32fb4740587`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 17.0 MB (16966070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d16bbe0304af54c175c37b3beef61124e72b9de2eac39c8e87d0541bf3c00`  
		Last Modified: Sat, 16 Nov 2024 02:56:38 GMT  
		Size: 47.2 MB (47216996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20384b31c64ae4521aac223fdb3442e202c0ce5e242cc958328dc2b822226a17`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2324da7add4d487c09e7a24c7c4f94b5606843ec735ae27bfe5151ad68b9d1a3`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe3db8fae36279f122564ce6be3467c0496eb9c1f8a46b5d4edbb1f5aa53377`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9268f9c3bc750dfe0e8e9e8fd0d3f0c621f923ac0ecabbafac1845cbc0dbc7`  
		Last Modified: Mon, 02 Dec 2024 20:26:49 GMT  
		Size: 12.4 MB (12383868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe8430a328e3db65ba55b498b5a2ec14e70aca1a2580a06b75b4c7e52dea0ed`  
		Last Modified: Mon, 02 Dec 2024 20:27:03 GMT  
		Size: 492.1 MB (492081091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa79a664629b4fcbf91ec85105fbc8d08d0b1b08014bc5eef7c12b75c5c0d840`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7` - unknown; unknown

```console
$ docker pull storm@sha256:79b3f4af71c2aed8b09fb91e67d4436c488de02bd12155a8963e720d79bf438a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627cdc9c6d38bf3a87647845686b16b2c3dbf023c79d7a0cccc957bb2f029dc1`

```dockerfile
```

-	Layers:
	-	`sha256:74ad047a4c4d88df3274e34a47b20db524cdc291cde66da4834881efd86d294d`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 4.6 MB (4580316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267b2a73ca26c6abee4544af95dc63713030bfc1617bc1f3d51378bfe8c58a4`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.7` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:459c352225a3a8c8055e637861973f8407f827c811a4696b7a3c8c4c2e24423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 MB (595706915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1da9a89a77607c56f849ed30bdd41341c74ac1ca21a18f923bfc34cbf44f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46d31ccd7c839aa8a7d1943c68ca0318d885238023919e2bc3ee7d64fb022f`  
		Last Modified: Sat, 16 Nov 2024 03:09:27 GMT  
		Size: 45.6 MB (45577581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf902ff6a58eb102f981ab4d96df2ed8e9668b2672aea0160a69365aff064d`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c7c3c201dfabf7f53721eda596b927f1c39cad09692695e97f5cdd11601a8`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf47c08a1013c8c592c74645a0ac0df336a72eb5a68d5a188a1fbad1bf34bb`  
		Last Modified: Sat, 16 Nov 2024 04:56:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b09b6685e69a1c2b1b8de1e04ae7827e60d765fe6f97089364c6b1c33549c`  
		Last Modified: Sat, 16 Nov 2024 04:56:01 GMT  
		Size: 12.2 MB (12170731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479737179610c3b2f727da3239a6aa01e32fbbfebcd6a84dcc920edd90cf10bb`  
		Last Modified: Mon, 02 Dec 2024 20:43:02 GMT  
		Size: 492.1 MB (492081048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97c4f16f0b73677cce5a481ed413a58bb41e0e961e264796164d3bbc2ec5b7d`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7` - unknown; unknown

```console
$ docker pull storm@sha256:e51964c52794ad2598cc2a4cb196d1294cee84915e1b0acea474c60b6186bb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5ac40ba2c9e642e36c508b82ec4623521570295f92dc05db92633b0eee526`

```dockerfile
```

-	Layers:
	-	`sha256:6ab7c97aaecb28ba9fc8bea276082b4ff5e94eafe5b3a368ea98543b1bc50dfe`  
		Last Modified: Mon, 02 Dec 2024 20:42:53 GMT  
		Size: 4.6 MB (4581440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ac4dcc7d8deccf16c8ff850e62f367dbc60a1cf0ae6ffa96c15b565785c230`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 26.1 KB (26119 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.7-jre17`

```console
$ docker pull storm@sha256:570a3d95e00717915869b7a54f844c6eb785cb58c3cb9cc4e8330e97feca7454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.7-jre17` - linux; amd64

```console
$ docker pull storm@sha256:37c965615abb48ba975a57c1353fc0597a4a45c789cfe259ac94e01d62b80d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598128773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7d277b20148f8fe208bd02106a9ba3e4ec4e7a38eda259878a60bacdd7d19b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cdce4894a71f973fa9abc3e2c1d469dfd4621fe70e355f32d79ca115dfee4a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 17.0 MB (16966061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ac7aa71697a2320c1fe4ead00f2444c7300ce5bea68a3d2c7ce45bd1ddd7a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 46.9 MB (46941772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e405f17e3562bd1874c952ff62356307897e8b88dc986da2e761728ee91631`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1cc78034c3680aaf89f46cf86bf07a1afacebe58652cf7cd204a1c5a8e2bc`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a61295d35e57457b89e6a3efaeb903ee9ad4d3b836fe01c16d858438693cd12`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748bc0a20d75e5aeadf451483335ab63597bfaa2dfc8c38acaa98d68ae56ce9a`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 12.4 MB (12383799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb699ab0966b46c8ffb25e62aa0bce7aa0d0343e2e9c67f8bb6c6b3450c12e8`  
		Last Modified: Mon, 02 Dec 2024 20:27:00 GMT  
		Size: 492.1 MB (492081205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4e5ae3731daa0e316adcddaf3282a45bae620a8601e180ac47a35cb3e04c81`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:b8184133d31b53a06c2ea441f63ab4485068539f8fb75cb4b7c01b6cb150dc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4592767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40632f58cc31787e76f14bc364d0b51eaff62dab43e53fbae4a79c495bdc09bb`

```dockerfile
```

-	Layers:
	-	`sha256:f1852ac7ba9d66dae0e7090e21406a8a7f7a3ba4cf1e9b35ea6cc74b084ba727`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 4.6 MB (4566911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6febaac51e0cbb043def80eefe8632dc988a0a390c39a21caffd82aa81ff99de`  
		Last Modified: Mon, 02 Dec 2024 20:26:49 GMT  
		Size: 25.9 KB (25856 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.7-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:727d7540d5807fa1e921a6ec289eeda6a8751f42dcaae125b045e4811466c90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596560198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a558e5e6fe747269139ec2a880425aeeab0620ee11408fa9ca738475f93ff3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9645c74eb59d3dc798c961d1d23973795136cdd64d274b2eba5d7b6070728`  
		Last Modified: Sat, 16 Nov 2024 03:10:59 GMT  
		Size: 46.4 MB (46430937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e42cee9f192b8f6883387f85980e69d95d0c9d1c397285374ae3738062a650b`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09343514b98c9ec6bd4ef0d351d9d5375c6f53ec935eee85e8a6bf4dca1282d`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae23b9d6247c1d68a83f2f7dd7b80566cf820b08e1cdf708b02c9d62d60a7ce`  
		Last Modified: Sat, 16 Nov 2024 04:59:31 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4466bd776cf069db4e97f7809ed130b5a5cb039d532c2051560e6f24a66cc`  
		Last Modified: Sat, 16 Nov 2024 04:59:32 GMT  
		Size: 12.2 MB (12170693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e6e03fbfb758cc406e6ad65670a4271ec5ed27a2b2c10ce26ea377bd3bab2e`  
		Last Modified: Mon, 02 Dec 2024 20:46:17 GMT  
		Size: 492.1 MB (492081014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f7fda9a6781d00b089d575445ffc8961458eab208ea5e9b7d01be12891c9d`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:7aa04bf56d6c7a4c77ddfef7a3d3e7f3c28fcb5da89ccb7c88c00ced499466cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6567598c4805d8c46bda457b53d31067d739359e56e1531a6f6542a7c4dc2eb`

```dockerfile
```

-	Layers:
	-	`sha256:838ef9a8481457c6e27ba66a7bc299c1cd462035805ad1b9185cb427545aa288`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 4.6 MB (4567404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc1502dd6866e8d4663f9a964e324f3e660ddd2ec488ee6111c5ea7662baa9`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.7.1`

```console
$ docker pull storm@sha256:23dd892ec188a6d44bbeda3f9cb62926252ad3b3dd363181da645140cdd77a54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.7.1` - linux; amd64

```console
$ docker pull storm@sha256:1d1573425ab184016622eb813da7abf6412acc092438b54f1865dad52d8faa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.4 MB (598403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947e54979dce5877c3e1f96bcddd161798db96cbca578e7dd6df0a532c5265c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee5e42e638331b77b0e5463a888e36cf34c74dc011204a42fbaa32fb4740587`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 17.0 MB (16966070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d16bbe0304af54c175c37b3beef61124e72b9de2eac39c8e87d0541bf3c00`  
		Last Modified: Sat, 16 Nov 2024 02:56:38 GMT  
		Size: 47.2 MB (47216996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20384b31c64ae4521aac223fdb3442e202c0ce5e242cc958328dc2b822226a17`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2324da7add4d487c09e7a24c7c4f94b5606843ec735ae27bfe5151ad68b9d1a3`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe3db8fae36279f122564ce6be3467c0496eb9c1f8a46b5d4edbb1f5aa53377`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9268f9c3bc750dfe0e8e9e8fd0d3f0c621f923ac0ecabbafac1845cbc0dbc7`  
		Last Modified: Mon, 02 Dec 2024 20:26:49 GMT  
		Size: 12.4 MB (12383868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe8430a328e3db65ba55b498b5a2ec14e70aca1a2580a06b75b4c7e52dea0ed`  
		Last Modified: Mon, 02 Dec 2024 20:27:03 GMT  
		Size: 492.1 MB (492081091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa79a664629b4fcbf91ec85105fbc8d08d0b1b08014bc5eef7c12b75c5c0d840`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7.1` - unknown; unknown

```console
$ docker pull storm@sha256:79b3f4af71c2aed8b09fb91e67d4436c488de02bd12155a8963e720d79bf438a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627cdc9c6d38bf3a87647845686b16b2c3dbf023c79d7a0cccc957bb2f029dc1`

```dockerfile
```

-	Layers:
	-	`sha256:74ad047a4c4d88df3274e34a47b20db524cdc291cde66da4834881efd86d294d`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 4.6 MB (4580316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267b2a73ca26c6abee4544af95dc63713030bfc1617bc1f3d51378bfe8c58a4`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.7.1` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:459c352225a3a8c8055e637861973f8407f827c811a4696b7a3c8c4c2e24423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 MB (595706915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1da9a89a77607c56f849ed30bdd41341c74ac1ca21a18f923bfc34cbf44f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46d31ccd7c839aa8a7d1943c68ca0318d885238023919e2bc3ee7d64fb022f`  
		Last Modified: Sat, 16 Nov 2024 03:09:27 GMT  
		Size: 45.6 MB (45577581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf902ff6a58eb102f981ab4d96df2ed8e9668b2672aea0160a69365aff064d`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c7c3c201dfabf7f53721eda596b927f1c39cad09692695e97f5cdd11601a8`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf47c08a1013c8c592c74645a0ac0df336a72eb5a68d5a188a1fbad1bf34bb`  
		Last Modified: Sat, 16 Nov 2024 04:56:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b09b6685e69a1c2b1b8de1e04ae7827e60d765fe6f97089364c6b1c33549c`  
		Last Modified: Sat, 16 Nov 2024 04:56:01 GMT  
		Size: 12.2 MB (12170731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479737179610c3b2f727da3239a6aa01e32fbbfebcd6a84dcc920edd90cf10bb`  
		Last Modified: Mon, 02 Dec 2024 20:43:02 GMT  
		Size: 492.1 MB (492081048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97c4f16f0b73677cce5a481ed413a58bb41e0e961e264796164d3bbc2ec5b7d`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7.1` - unknown; unknown

```console
$ docker pull storm@sha256:e51964c52794ad2598cc2a4cb196d1294cee84915e1b0acea474c60b6186bb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5ac40ba2c9e642e36c508b82ec4623521570295f92dc05db92633b0eee526`

```dockerfile
```

-	Layers:
	-	`sha256:6ab7c97aaecb28ba9fc8bea276082b4ff5e94eafe5b3a368ea98543b1bc50dfe`  
		Last Modified: Mon, 02 Dec 2024 20:42:53 GMT  
		Size: 4.6 MB (4581440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ac4dcc7d8deccf16c8ff850e62f367dbc60a1cf0ae6ffa96c15b565785c230`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 26.1 KB (26119 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:2.7.1-jre17`

```console
$ docker pull storm@sha256:570a3d95e00717915869b7a54f844c6eb785cb58c3cb9cc4e8330e97feca7454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:2.7.1-jre17` - linux; amd64

```console
$ docker pull storm@sha256:37c965615abb48ba975a57c1353fc0597a4a45c789cfe259ac94e01d62b80d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598128773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7d277b20148f8fe208bd02106a9ba3e4ec4e7a38eda259878a60bacdd7d19b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cdce4894a71f973fa9abc3e2c1d469dfd4621fe70e355f32d79ca115dfee4a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 17.0 MB (16966061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ac7aa71697a2320c1fe4ead00f2444c7300ce5bea68a3d2c7ce45bd1ddd7a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 46.9 MB (46941772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e405f17e3562bd1874c952ff62356307897e8b88dc986da2e761728ee91631`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1cc78034c3680aaf89f46cf86bf07a1afacebe58652cf7cd204a1c5a8e2bc`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a61295d35e57457b89e6a3efaeb903ee9ad4d3b836fe01c16d858438693cd12`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748bc0a20d75e5aeadf451483335ab63597bfaa2dfc8c38acaa98d68ae56ce9a`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 12.4 MB (12383799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb699ab0966b46c8ffb25e62aa0bce7aa0d0343e2e9c67f8bb6c6b3450c12e8`  
		Last Modified: Mon, 02 Dec 2024 20:27:00 GMT  
		Size: 492.1 MB (492081205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4e5ae3731daa0e316adcddaf3282a45bae620a8601e180ac47a35cb3e04c81`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7.1-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:b8184133d31b53a06c2ea441f63ab4485068539f8fb75cb4b7c01b6cb150dc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4592767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40632f58cc31787e76f14bc364d0b51eaff62dab43e53fbae4a79c495bdc09bb`

```dockerfile
```

-	Layers:
	-	`sha256:f1852ac7ba9d66dae0e7090e21406a8a7f7a3ba4cf1e9b35ea6cc74b084ba727`  
		Last Modified: Mon, 02 Dec 2024 20:26:50 GMT  
		Size: 4.6 MB (4566911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6febaac51e0cbb043def80eefe8632dc988a0a390c39a21caffd82aa81ff99de`  
		Last Modified: Mon, 02 Dec 2024 20:26:49 GMT  
		Size: 25.9 KB (25856 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:2.7.1-jre17` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:727d7540d5807fa1e921a6ec289eeda6a8751f42dcaae125b045e4811466c90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596560198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a558e5e6fe747269139ec2a880425aeeab0620ee11408fa9ca738475f93ff3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9645c74eb59d3dc798c961d1d23973795136cdd64d274b2eba5d7b6070728`  
		Last Modified: Sat, 16 Nov 2024 03:10:59 GMT  
		Size: 46.4 MB (46430937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e42cee9f192b8f6883387f85980e69d95d0c9d1c397285374ae3738062a650b`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09343514b98c9ec6bd4ef0d351d9d5375c6f53ec935eee85e8a6bf4dca1282d`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae23b9d6247c1d68a83f2f7dd7b80566cf820b08e1cdf708b02c9d62d60a7ce`  
		Last Modified: Sat, 16 Nov 2024 04:59:31 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4466bd776cf069db4e97f7809ed130b5a5cb039d532c2051560e6f24a66cc`  
		Last Modified: Sat, 16 Nov 2024 04:59:32 GMT  
		Size: 12.2 MB (12170693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e6e03fbfb758cc406e6ad65670a4271ec5ed27a2b2c10ce26ea377bd3bab2e`  
		Last Modified: Mon, 02 Dec 2024 20:46:17 GMT  
		Size: 492.1 MB (492081014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f7fda9a6781d00b089d575445ffc8961458eab208ea5e9b7d01be12891c9d`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:2.7.1-jre17` - unknown; unknown

```console
$ docker pull storm@sha256:7aa04bf56d6c7a4c77ddfef7a3d3e7f3c28fcb5da89ccb7c88c00ced499466cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6567598c4805d8c46bda457b53d31067d739359e56e1531a6f6542a7c4dc2eb`

```dockerfile
```

-	Layers:
	-	`sha256:838ef9a8481457c6e27ba66a7bc299c1cd462035805ad1b9185cb427545aa288`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 4.6 MB (4567404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc1502dd6866e8d4663f9a964e324f3e660ddd2ec488ee6111c5ea7662baa9`  
		Last Modified: Mon, 02 Dec 2024 20:46:06 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `storm:latest`

```console
$ docker pull storm@sha256:23dd892ec188a6d44bbeda3f9cb62926252ad3b3dd363181da645140cdd77a54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:1d1573425ab184016622eb813da7abf6412acc092438b54f1865dad52d8faa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.4 MB (598403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947e54979dce5877c3e1f96bcddd161798db96cbca578e7dd6df0a532c5265c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee5e42e638331b77b0e5463a888e36cf34c74dc011204a42fbaa32fb4740587`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 17.0 MB (16966070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d16bbe0304af54c175c37b3beef61124e72b9de2eac39c8e87d0541bf3c00`  
		Last Modified: Sat, 16 Nov 2024 02:56:38 GMT  
		Size: 47.2 MB (47216996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20384b31c64ae4521aac223fdb3442e202c0ce5e242cc958328dc2b822226a17`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2324da7add4d487c09e7a24c7c4f94b5606843ec735ae27bfe5151ad68b9d1a3`  
		Last Modified: Sat, 16 Nov 2024 02:56:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe3db8fae36279f122564ce6be3467c0496eb9c1f8a46b5d4edbb1f5aa53377`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9268f9c3bc750dfe0e8e9e8fd0d3f0c621f923ac0ecabbafac1845cbc0dbc7`  
		Last Modified: Mon, 02 Dec 2024 20:26:49 GMT  
		Size: 12.4 MB (12383868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe8430a328e3db65ba55b498b5a2ec14e70aca1a2580a06b75b4c7e52dea0ed`  
		Last Modified: Mon, 02 Dec 2024 20:27:03 GMT  
		Size: 492.1 MB (492081091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa79a664629b4fcbf91ec85105fbc8d08d0b1b08014bc5eef7c12b75c5c0d840`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:79b3f4af71c2aed8b09fb91e67d4436c488de02bd12155a8963e720d79bf438a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627cdc9c6d38bf3a87647845686b16b2c3dbf023c79d7a0cccc957bb2f029dc1`

```dockerfile
```

-	Layers:
	-	`sha256:74ad047a4c4d88df3274e34a47b20db524cdc291cde66da4834881efd86d294d`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 4.6 MB (4580316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267b2a73ca26c6abee4544af95dc63713030bfc1617bc1f3d51378bfe8c58a4`  
		Last Modified: Mon, 02 Dec 2024 20:26:48 GMT  
		Size: 26.0 KB (25997 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:459c352225a3a8c8055e637861973f8407f827c811a4696b7a3c8c4c2e24423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 MB (595706915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1da9a89a77607c56f849ed30bdd41341c74ac1ca21a18f923bfc34cbf44f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Dec 2024 07:06:13 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Mon, 02 Dec 2024 07:06:13 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ARG DISTRO_NAME=apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
# ARGS: DISTRO_NAME=apache-storm-2.7.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME" # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
WORKDIR /apache-storm-2.7.1
# Mon, 02 Dec 2024 07:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.7.1/bin
# Mon, 02 Dec 2024 07:06:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 02 Dec 2024 07:06:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46d31ccd7c839aa8a7d1943c68ca0318d885238023919e2bc3ee7d64fb022f`  
		Last Modified: Sat, 16 Nov 2024 03:09:27 GMT  
		Size: 45.6 MB (45577581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf902ff6a58eb102f981ab4d96df2ed8e9668b2672aea0160a69365aff064d`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c7c3c201dfabf7f53721eda596b927f1c39cad09692695e97f5cdd11601a8`  
		Last Modified: Sat, 16 Nov 2024 03:09:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf47c08a1013c8c592c74645a0ac0df336a72eb5a68d5a188a1fbad1bf34bb`  
		Last Modified: Sat, 16 Nov 2024 04:56:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b09b6685e69a1c2b1b8de1e04ae7827e60d765fe6f97089364c6b1c33549c`  
		Last Modified: Sat, 16 Nov 2024 04:56:01 GMT  
		Size: 12.2 MB (12170731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479737179610c3b2f727da3239a6aa01e32fbbfebcd6a84dcc920edd90cf10bb`  
		Last Modified: Mon, 02 Dec 2024 20:43:02 GMT  
		Size: 492.1 MB (492081048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97c4f16f0b73677cce5a481ed413a58bb41e0e961e264796164d3bbc2ec5b7d`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:e51964c52794ad2598cc2a4cb196d1294cee84915e1b0acea474c60b6186bb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb5ac40ba2c9e642e36c508b82ec4623521570295f92dc05db92633b0eee526`

```dockerfile
```

-	Layers:
	-	`sha256:6ab7c97aaecb28ba9fc8bea276082b4ff5e94eafe5b3a368ea98543b1bc50dfe`  
		Last Modified: Mon, 02 Dec 2024 20:42:53 GMT  
		Size: 4.6 MB (4581440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ac4dcc7d8deccf16c8ff850e62f367dbc60a1cf0ae6ffa96c15b565785c230`  
		Last Modified: Mon, 02 Dec 2024 20:42:52 GMT  
		Size: 26.1 KB (26119 bytes)  
		MIME: application/vnd.in-toto+json
