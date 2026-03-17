## `liquibase:latest`

```console
$ docker pull liquibase@sha256:2f8e167e72e31e1340e09d834cfa9b309c269c67d4948cb1e8dbf624fc40e7a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:a24235e261619f7d233da62fb565ffc47f17b157bef7dca1d14c98d2b655d0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111111839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2aa006ac0ddae3f3b1760187d525f9452a743a73bae1340959b64e04d732541`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:17 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:22:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:22:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:22:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:22:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:40:51 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Mar 2026 02:40:51 GMT
WORKDIR /liquibase
# Tue, 17 Mar 2026 02:40:52 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Mar 2026 02:40:52 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Mar 2026 02:40:52 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Mar 2026 02:40:52 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Mar 2026 02:40:52 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Mar 2026 02:40:52 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Mar 2026 02:40:52 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Mar 2026 02:40:52 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Mar 2026 02:40:52 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Mar 2026 02:40:52 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Mar 2026 02:40:52 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Mar 2026 02:41:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Mar 2026 02:41:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Mar 2026 02:41:00 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Mar 2026 02:41:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Mar 2026 02:41:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Mar 2026 02:41:00 GMT
USER liquibase:liquibase
# Tue, 17 Mar 2026 02:41:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:41:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0ce981274bc790f263f31fa8a63cc62b619cf97c4342da3a62903aaecd69b`  
		Last Modified: Tue, 17 Mar 2026 01:22:42 GMT  
		Size: 16.1 MB (16149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b445b8fa955eb4bdcf4505698bb88d51550a8e823b9a5b2a5fe8ec4fd5b94e`  
		Last Modified: Tue, 17 Mar 2026 01:23:08 GMT  
		Size: 53.0 MB (52985523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd00f9a8c41980de68ff0ce870388eb0f3c76cc144ddc1150250766d01a7400`  
		Last Modified: Tue, 17 Mar 2026 01:23:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d049ee86af27ea59a1cfb64ca1fcd92dde4e8eb578863fa94ccbe6d9691db0b`  
		Last Modified: Tue, 17 Mar 2026 01:23:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b73ea915827b05b9dddf50e5110667452142331172267c96d327db0c2c33b8b`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f934280894ed20401099811872a1430fa5c7aff6fe254d12cc57ad60d286015`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 8.7 MB (8665796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9091e7e2c1cf83902668292cb6417c787281433a9ad9f76be26eb9ba411d49a7`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 3.8 MB (3764444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d044e4a373526032ad48ec6c525b6482f40b88e3d543972a227554c51e778f3`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035f225bdc0226950799207d889a35c2636df3e102380144ad4e05b7698396a`  
		Last Modified: Tue, 17 Mar 2026 02:41:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:cd4a332d1a5f6b400515f07cade32129c6684ab5ba2387cd6879ffaf457d9d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8025038432b5fb3cd706a50c527eb4a017bfcff29a9beff02833113957265f`

```dockerfile
```

-	Layers:
	-	`sha256:c9d8501be17b2ac178f698d18273b84507b8c6d0d6e1562f46925b536e16b1d5`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf6e531a65b67aaf0bf0f61e00c7bdc09339bb5322a9918aa44f9b003246777`  
		Last Modified: Tue, 17 Mar 2026 02:41:08 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:a25201a7896a1328fd85bd5aeaf6e5b165a72fb30f1fd073d124e048e7455e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107733541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662e0d541138e939923862644211e6e68fe2b7d9acc28ebd3be01df935e5c0be`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:55 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:24:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:45:06 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Mar 2026 02:45:06 GMT
WORKDIR /liquibase
# Tue, 17 Mar 2026 02:45:07 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Mar 2026 02:45:07 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Mar 2026 02:45:07 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Mar 2026 02:45:07 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Mar 2026 02:45:07 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Mar 2026 02:45:07 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Mar 2026 02:45:07 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Mar 2026 02:45:07 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Mar 2026 02:45:07 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Mar 2026 02:45:07 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Mar 2026 02:45:07 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Mar 2026 02:45:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Mar 2026 02:45:19 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Mar 2026 02:45:19 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Mar 2026 02:45:19 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Mar 2026 02:45:19 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Mar 2026 02:45:19 GMT
USER liquibase:liquibase
# Tue, 17 Mar 2026 02:45:19 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:45:19 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd066b1ebbd8fb552f9c7bc038227296b6be90ab9b47f1a2b1e8c0e40b450309`  
		Last Modified: Tue, 17 Mar 2026 01:24:20 GMT  
		Size: 16.1 MB (16073499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7f4e7ff04dca56f293805123d3c21407bcbc425037f08ae8a2848b1213de0`  
		Last Modified: Tue, 17 Mar 2026 01:24:48 GMT  
		Size: 52.2 MB (52155642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba23e36651f44df306db43d2f72d8c76baea036ae97c024d0195abdcb492b5e`  
		Last Modified: Tue, 17 Mar 2026 01:24:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f42adf5c10b40811d2213dd9231d004c92cab7d8049b84a72af374cc967163`  
		Last Modified: Tue, 17 Mar 2026 01:24:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3429c3f8c1da44e0392ac7c8d597191e2263f984249a510ce936dbed9cd68e`  
		Last Modified: Tue, 17 Mar 2026 02:45:28 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8eecafcf3b9849f04de04bfc741d1d27ca92eeb93fabf35340fe9a6225659a`  
		Last Modified: Tue, 17 Mar 2026 02:45:29 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a444fbc83099ebb4be6fe46ad37c0fc35d1341c2c374bdc7d3e0a28fd9044873`  
		Last Modified: Tue, 17 Mar 2026 02:45:28 GMT  
		Size: 3.4 MB (3441190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a64bf569fbe3a10a3c96203357cc836ff3e2ac0efa530ef64314ed87b643c3b`  
		Last Modified: Tue, 17 Mar 2026 02:45:28 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b05b147793911f6ea50ef40b1639a9afd09d3e257698513bcf4686344a5ee7`  
		Last Modified: Tue, 17 Mar 2026 02:45:29 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:71db4041dcdb43b6d4e8e8fa02cc24729895b96d6f8ffe212510ca51d6bcb803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f4a0b6a425d358545c3190ad9bde9a8d7a4b92b57174d4e55c721eb976a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:9b362601268fd4f535ff4d812c8296dceeeb8f15e2fb5a3264691f5150636fde`  
		Last Modified: Tue, 17 Mar 2026 02:45:28 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a80e167193db23c03180c576056f2da513103847532ead1ae859494a77010f`  
		Last Modified: Tue, 17 Mar 2026 02:45:28 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
