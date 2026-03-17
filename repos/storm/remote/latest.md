## `storm:latest`

```console
$ docker pull storm@sha256:98e5f3590ad490e150c8f7ede867fa386f17ca5d5f429f840b360ac72c48199d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:a38954d704ed81c13576608d6f6ac1f89b98a8628a6d12aee6578d4f6d97d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.8 MB (458785062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc217d056a7e15d9816b4d14c4d31f1a5bfd85f1dafc81e55a68e716420b7a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:58 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:23:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:49:22 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 17 Mar 2026 02:49:22 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 17 Mar 2026 02:49:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:49:31 GMT
ARG DISTRO_NAME=apache-storm-2.8.4
# Tue, 17 Mar 2026 02:50:02 GMT
# ARGS: DISTRO_NAME=apache-storm-2.8.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     mv "$DISTRO_NAME" apache-storm;     chown -R storm:storm apache-storm # buildkit
# Tue, 17 Mar 2026 02:50:02 GMT
WORKDIR /apache-storm
# Tue, 17 Mar 2026 02:50:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm/bin
# Tue, 17 Mar 2026 02:50:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:50:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63239663e8a87d05403e1af415931bdfdf82d1d2d24da508b4978810eceeab0`  
		Last Modified: Tue, 17 Mar 2026 01:23:13 GMT  
		Size: 17.0 MB (16983363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ae756ce2bc866173a999ba2b5bbc5da6d52dcdb544c0f5dfa7a16502ceb5a`  
		Last Modified: Tue, 17 Mar 2026 01:23:14 GMT  
		Size: 47.4 MB (47434771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58843afac925a3c42eff31a3a65862901decf85c79e1569412537836b4d6b033`  
		Last Modified: Tue, 17 Mar 2026 01:23:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d515e2ee9d6c9606efeb5f3dfc93b0db3d642deebde4d4da49b62406b989e4c`  
		Last Modified: Tue, 17 Mar 2026 01:23:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c0c8016eccf6c37cd5583452d878d6a85509e13895d349304124b9110e1cce`  
		Last Modified: Tue, 17 Mar 2026 02:50:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97158f1ea18ca7e75b9a4cd79c95fa662d1170c4636c253c2e143c1feb87a4e8`  
		Last Modified: Tue, 17 Mar 2026 02:50:25 GMT  
		Size: 12.4 MB (12391427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8363204ef14840fd05557f08e1c4d393c146305ddc1cb08d9ff6b898facd33a3`  
		Last Modified: Tue, 17 Mar 2026 02:50:32 GMT  
		Size: 352.2 MB (352239358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5fe729cece67ee7769177133a34cf065fd309c4b7216c20082722870c9fbc2`  
		Last Modified: Tue, 17 Mar 2026 02:50:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:fc7de925e20c9d71639ab05785c721bea69d590413807ac76ae3696c2bc7d68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4546832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd654ed5a91ce56a84a890b5f7fcdfb5750658cc83b7e8167e0b12a01cd9a2d3`

```dockerfile
```

-	Layers:
	-	`sha256:9a1e92ae9c63ba64b97508585ba36057cb3e4d0408fc2c3d7fa8a9fb929d07ea`  
		Last Modified: Tue, 17 Mar 2026 02:50:25 GMT  
		Size: 4.5 MB (4520044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96b8af64cecb3bbd3b486f4a5012205815a8a1596d41bb52e7c99ec67b93e56`  
		Last Modified: Tue, 17 Mar 2026 02:50:25 GMT  
		Size: 26.8 KB (26788 bytes)  
		MIME: application/vnd.in-toto+json

### `storm:latest` - linux; arm64 variant v8

```console
$ docker pull storm@sha256:7ebd2afc194444651e3e27e57bcfa381355a932d61cda2587f6659f11c09984c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.2 MB (457207127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c14fa94d82121f1355369062c4e9272acd2f6292aa4fbd3d70c0bd3d5e55417`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:24:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:53:16 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Tue, 17 Mar 2026 02:53:16 GMT
RUN userdel -r ubuntu &&     groupdel ubuntu || true RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"`` # buildkit
# Tue, 17 Mar 2026 02:53:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python3         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:53:29 GMT
ARG DISTRO_NAME=apache-storm-2.8.4
# Tue, 17 Mar 2026 02:53:42 GMT
# ARGS: DISTRO_NAME=apache-storm-2.8.4
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     importKeys() {       for key in       5167DE337E7370373499FC1DA4A672F11B5050C8       32C8C0BEE3D01AF46B6E24B0AC30BFA8FEF0711F       79B03D059E628478FC9F1D8B152CAD0C46E87B61       51379DA8A7AE5B02674EF15C134716AF768D9B6E       DA903F2CF9BBD42EAECFA9E45EA6FAEF09A4474D       6156BAC0C21A1991CF1B690AB2973D6F4A67943A       B83D15E72253ED1104EB4FBBDAB472F0E5B8A431       339F3B2F72129ABCA81D96DA91EA7956A2DAD9CE       72B436558AA9CDCA2C4CBAC340D4B35E2C1452E5       ; do         gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$key" ||         gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||         gpg --batch --keyserver hkps://pgp.mit.edu --recv-keys "$key" ||         gpg --batch --keyserver hkps://keyserver.pgp.com --recv-keys "$key" ;       done;     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     importKeys;     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     mv "$DISTRO_NAME" apache-storm;     chown -R storm:storm apache-storm # buildkit
# Tue, 17 Mar 2026 02:53:42 GMT
WORKDIR /apache-storm
# Tue, 17 Mar 2026 02:53:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm/bin
# Tue, 17 Mar 2026 02:53:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:53:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135b685185570494910edd394b8134172c97bab64cfef4134685bc7a7adf965`  
		Last Modified: Tue, 17 Mar 2026 01:24:08 GMT  
		Size: 17.0 MB (16996055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2cd9590e5d48e6a3302ddc079709cd642f78e0609ee70084045d54b69f1cd8`  
		Last Modified: Tue, 17 Mar 2026 01:24:31 GMT  
		Size: 46.9 MB (46922135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7c1c52c3ce02cf734adb29eb7a2c7d950c8a89652378cf9ec8eac5a321fa90`  
		Last Modified: Tue, 17 Mar 2026 01:24:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7483a7f867de37bbf4a1c948255b63498ac2c0520ec35a0d753e382658eb1b`  
		Last Modified: Tue, 17 Mar 2026 01:24:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f04d041ca7ed40eb00e6e1960da4f497c4c6fd7432b506fc734d3fc4d8e99`  
		Last Modified: Tue, 17 Mar 2026 02:54:06 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954c41525212534b5a4fbd5299d2f41c5740468fc4a8084a6470301c61458ec`  
		Last Modified: Tue, 17 Mar 2026 02:54:07 GMT  
		Size: 12.2 MB (12175662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9069a086a174a8b552ab50e60d99574df9afcc3d9db9c19f86303cf07c5e929d`  
		Last Modified: Tue, 17 Mar 2026 02:54:16 GMT  
		Size: 352.2 MB (352239407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90945ba0e99d080882966ff0158840e61eb7b4bfd156a46ed00ff7ac0d0934`  
		Last Modified: Tue, 17 Mar 2026 02:54:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `storm:latest` - unknown; unknown

```console
$ docker pull storm@sha256:ebcd0f2677c6558db082ffc9c2363a1d352597d348b0d9c83cbf2d29fff5e39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4547507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eb7b652646ca8f9a06bae3bf2a0a8e3e357c4c8e49cf531408af48b4635607`

```dockerfile
```

-	Layers:
	-	`sha256:34d4adbffa9c6c87fad2cc895e8b150641edde3e8eec02eb891b41716f66c269`  
		Last Modified: Tue, 17 Mar 2026 02:54:07 GMT  
		Size: 4.5 MB (4520574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3bdbe0619c678748c8d753547eb789e85e96d7731d71b171e2d31d47eadcd5`  
		Last Modified: Tue, 17 Mar 2026 02:54:06 GMT  
		Size: 26.9 KB (26933 bytes)  
		MIME: application/vnd.in-toto+json
