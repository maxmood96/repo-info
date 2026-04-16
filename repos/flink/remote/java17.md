## `flink:java17`

```console
$ docker pull flink@sha256:4d69877f2cf068c77551194559a15149980bc5c1c7d76662e1df2ea72eace2ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java17` - linux; amd64

```console
$ docker pull flink@sha256:d1083d107cb6c34e22515d4a431b4f73849f9f2632ef154316ad5029c1b61561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.6 MB (665608690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b36d70c88cf1d46cf35efa01681fabebb8c9c77651ac31fde10f70575ebd1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:56 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:25 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Wed, 15 Apr 2026 21:27:25 GMT
ENV FLINK_HOME=/opt/flink
# Wed, 15 Apr 2026 21:27:25 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:27:25 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
WORKDIR /opt/flink
# Wed, 15 Apr 2026 21:28:03 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Wed, 15 Apr 2026 21:28:03 GMT
USER flink
# Wed, 15 Apr 2026 21:28:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:28:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:28:03 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Wed, 15 Apr 2026 21:28:03 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f2a026f4e857e6710d7371079214474f83b2a72af7243a5be77a97b2f7f5ec`  
		Last Modified: Wed, 15 Apr 2026 20:34:12 GMT  
		Size: 17.0 MB (16983429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220fbdf6ba711172c65f46573fb8ae25fa235a06039daf1c9e8ac635285fb9cb`  
		Last Modified: Wed, 15 Apr 2026 20:34:13 GMT  
		Size: 47.4 MB (47434831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8c1cd79a1e9cbb0d2f65b7542a9e9817b0659fd9c6e6ca5376208775e31416`  
		Last Modified: Wed, 15 Apr 2026 20:34:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094e86219be8ad2c0ff540151faa5cf78418e7062517cb774dfc01885b395a0`  
		Last Modified: Wed, 15 Apr 2026 20:34:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af64fa260a0e2617ce0bd037da0e8916c63785018e65c262330d0eb476680509`  
		Last Modified: Wed, 15 Apr 2026 21:28:31 GMT  
		Size: 1.3 MB (1323146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8300d6b3fd7f428859f1a0dbfea0a6d9cec1a6ade8351ddf0c56a0724ac77633`  
		Last Modified: Wed, 15 Apr 2026 21:28:31 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24dc82d9836db1850a7c564a80dc398c03f98094ad33437a01f6e8fcb523704`  
		Last Modified: Wed, 15 Apr 2026 21:28:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a1f2cef44ad822f4f6fcf912923c06e6c2b333f17912f95f1ffe67f0c783bc`  
		Last Modified: Wed, 15 Apr 2026 21:28:47 GMT  
		Size: 570.1 MB (570128357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0269dce164304a5dee77c4635a5881d8382d42b6b1b5a4131c704485180ed12f`  
		Last Modified: Wed, 15 Apr 2026 21:28:32 GMT  
		Size: 2.2 KB (2235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:efd8ce8a51c845281629f6cab3eb69ce754e86d734b75938636ef6d1cc0faf21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3420806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82b7be94079de049adec6ad0b32b2eb6c985b5c9455e463900251798d12451`

```dockerfile
```

-	Layers:
	-	`sha256:2b6b45b8bc7ca3d0ade915d9e90d5718b7c94ce0a29c250f32c6d2e2b3efbdd7`  
		Last Modified: Wed, 15 Apr 2026 21:28:31 GMT  
		Size: 3.4 MB (3395226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29de4bb627ade48d91d8eb3b8d97c94af05b2763c17553a8aa13dfc72b06685d`  
		Last Modified: Wed, 15 Apr 2026 21:28:31 GMT  
		Size: 25.6 KB (25580 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java17` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:afb4fc885c3b6803ae53fac6956a7d4faa8f46f8b8026d23535420aaf3b84316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.1 MB (664116314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a262a082139113597251d9dabf468056db1bb5fe8674e96e49e405c30bef900f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:39 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:40:39 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Wed, 15 Apr 2026 21:40:39 GMT
ENV FLINK_HOME=/opt/flink
# Wed, 15 Apr 2026 21:40:39 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:40:39 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Wed, 15 Apr 2026 21:40:39 GMT
WORKDIR /opt/flink
# Wed, 15 Apr 2026 21:41:16 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Wed, 15 Apr 2026 21:41:16 GMT
USER flink
# Wed, 15 Apr 2026 21:41:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:41:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:41:16 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Wed, 15 Apr 2026 21:41:16 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05498ca84c34f7a91e3e695646db9b00c8acd41836f3ed4561193dbf7daca54`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 17.0 MB (16996261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf808475c74724ef30e1327e0aee1183fe00af6431bbfe3a03dc45bef6a982f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 46.9 MB (46922138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7290fbca45383216175d6032c9b32fc43206a736f84c41398fc9b0f259f0994`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df16b5408bf4e5f6f55b19c476ee82b617ab0251da0c9b96fc03b3bd29f60420`  
		Last Modified: Wed, 15 Apr 2026 21:41:48 GMT  
		Size: 1.2 MB (1187843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8f14fa09a116a628a5df4134c166a355d6f7e6a6286f6decea9d3ccc429745`  
		Last Modified: Wed, 15 Apr 2026 21:41:48 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1dd4b14d7765a25b2a0833bdaa9ea6b8325bc8db732d928a57e76b07bc8a1c`  
		Last Modified: Wed, 15 Apr 2026 21:41:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db087aa0217bf5e597226c1238fdd53de1ca8b9e765c9c75814ed9848a69a136`  
		Last Modified: Wed, 15 Apr 2026 21:42:01 GMT  
		Size: 570.1 MB (570128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d5a7fbafce11d340697af726379486764a1f62dce7693f4010d70db0cebe17`  
		Last Modified: Wed, 15 Apr 2026 21:41:50 GMT  
		Size: 2.2 KB (2238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java17` - unknown; unknown

```console
$ docker pull flink@sha256:ff96d4fc4b41426a9a287baacab6080411290b61ba415251d3f822c0e21ddbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3421609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50da8edeb67bf200ddba57c2dab1ae907b9fe6977b9eca29d0ee1fc6594c8ab`

```dockerfile
```

-	Layers:
	-	`sha256:d2a2be26fb4d7dd2c754238ce0c150e5ac3bed94c7152eb38cfbee9def610c54`  
		Last Modified: Wed, 15 Apr 2026 21:41:48 GMT  
		Size: 3.4 MB (3395798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25832cebe9adf795ba20269028f045ca8fc64f8821dfce22e74d8c25aa7bc528`  
		Last Modified: Wed, 15 Apr 2026 21:41:48 GMT  
		Size: 25.8 KB (25811 bytes)  
		MIME: application/vnd.in-toto+json
