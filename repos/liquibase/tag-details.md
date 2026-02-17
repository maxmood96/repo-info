<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:5.0`](#liquibase50)
-	[`liquibase:5.0-alpine`](#liquibase50-alpine)
-	[`liquibase:5.0.1`](#liquibase501)
-	[`liquibase:5.0.1-alpine`](#liquibase501-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:5.0`

```console
$ docker pull liquibase@sha256:30a08754815f214a095da5749a65f163ea0d8d96f1176f5aec5d3434b073fc53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:cbe0274d5e14a1eb94fd7660bc52be22836ed7f910fda44e8d3ef5df34529f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111109544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d863007b16ca53f7a4e26c53215f895b5e86647b0aa5796c63e3855f6cc11`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:25 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:25 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:26 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:35 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:35 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:35 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d575991a97516fe461d4e4036a37490052a3d42ec380135d014249e16b1d678`  
		Last Modified: Tue, 17 Feb 2026 20:19:05 GMT  
		Size: 16.1 MB (16147788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f70e2ff0d31ec24265820e65fb54d456b519fdb231448a0215d65703962a577`  
		Last Modified: Tue, 17 Feb 2026 20:20:15 GMT  
		Size: 53.0 MB (52985649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ba00cee2ad0168cf5988afb99d1aebb4e9016bee9e9391836ea3460fbd969`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f3670b78ac53ea39b08a6d287c35de5e8b733eb3f29916247010553254e8d`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218d52aea3b1d5147762843a6f2d8bdd41619b747cd1b50285fa742a754c5cb8`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821fe225c8232aa3924c3e22e91b30789b9731a48497262f8afd0fe04fabe14b`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15a8aa57efd3268b02d02285e4589e19bea0517d7d8bee6ba54d37269888d51`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49ae8fc1d5311adff89e57a5a43c22efaf17a28260c0453c194080de3829b77`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb90d82e3b2e3e6edbec1939a5e443b23398135256508a851c64ffbfb2785b6`  
		Last Modified: Tue, 17 Feb 2026 21:24:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:8caeef10dc8172d7f92fb18cf344a138f7c342d30cec0691b3528c807ee2191d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c93adbe2897c872eb91e7697bbcb946f9b74849a2701dd813bf59729d0f4f69`

```dockerfile
```

-	Layers:
	-	`sha256:398dee132eb9bd91b6798844faeee3adec45b1e3bc20054ed556aec9a28598cb`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c9f5cdbb5d9f9b9ed1c2bc4d01442aeb46ac6970bfd6b5c7619ccebf2a6d8d`  
		Last Modified: Tue, 17 Feb 2026 21:24:42 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:b8863cd1352a9baaadc6108c36fc67b7d125a152138241a37f237db70b32e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107728862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab877e154471a2899c3269679a4b14a586bd5bd1283570fa4ffb9ebe01ed72f3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:38 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:38 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:40 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2e1ffbed2e086872db296d7127853f11bef6e4799f7cb2b4e156095c1e23b`  
		Last Modified: Tue, 17 Feb 2026 20:19:12 GMT  
		Size: 16.1 MB (16072781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe4e0b231918fe2ead0afa921cbeff424dd42baa4d098009cc336e8441dc5e`  
		Last Modified: Tue, 17 Feb 2026 20:19:40 GMT  
		Size: 52.2 MB (52155631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abcf86440735c564d25176f95b4c79e326dbe28b63b3010e2a001ef88ee4e6a`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4eb0849933a83cc6f6987607d815fae05c7034219ce685e6c36b1e732367c8`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b21e05a99c7d57fe8f747e682f910c8d2927319907cb0588370e923efad2b`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055b6ef92e76375fb137aa7b087a69b5dcdae095060fd53d309aa4a5b3889733`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 8.7 MB (8665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac06bd993cf9e2355a7d44f86dbc4a20e0d129ea9581f7a5748ebee6a8ec6f4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.4 MB (3441317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbde0472c9860b7c2a9dbe01f6847bd802a1be89e51ab0860955bdc20ec9e21`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b37963e4f06320a583ae14bbc0b6bc1d5771ae5c0cffc74c5e9efbd11607b7`  
		Last Modified: Tue, 17 Feb 2026 21:25:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:99f79d4038f7b077ae294cecc1f7e91088ac1a481ee6b9c530c78e71ef8e855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40a6606d24abb82e7f025b6a0d2aba81e598933fbdf93c5796fdec535229631`

```dockerfile
```

-	Layers:
	-	`sha256:7a95cbb2ec3dfd2ab4f4e2ce087e6c14e7325ab13a655132eec6991d714fc4b4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f162b16313339322fe19692c99d992d15a10ae3539c04a2a95769b29496c8138`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1`

```console
$ docker pull liquibase@sha256:30a08754815f214a095da5749a65f163ea0d8d96f1176f5aec5d3434b073fc53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:cbe0274d5e14a1eb94fd7660bc52be22836ed7f910fda44e8d3ef5df34529f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111109544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d863007b16ca53f7a4e26c53215f895b5e86647b0aa5796c63e3855f6cc11`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:25 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:25 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:26 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:35 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:35 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:35 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d575991a97516fe461d4e4036a37490052a3d42ec380135d014249e16b1d678`  
		Last Modified: Tue, 17 Feb 2026 20:19:05 GMT  
		Size: 16.1 MB (16147788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f70e2ff0d31ec24265820e65fb54d456b519fdb231448a0215d65703962a577`  
		Last Modified: Tue, 17 Feb 2026 20:20:15 GMT  
		Size: 53.0 MB (52985649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ba00cee2ad0168cf5988afb99d1aebb4e9016bee9e9391836ea3460fbd969`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f3670b78ac53ea39b08a6d287c35de5e8b733eb3f29916247010553254e8d`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218d52aea3b1d5147762843a6f2d8bdd41619b747cd1b50285fa742a754c5cb8`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821fe225c8232aa3924c3e22e91b30789b9731a48497262f8afd0fe04fabe14b`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15a8aa57efd3268b02d02285e4589e19bea0517d7d8bee6ba54d37269888d51`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49ae8fc1d5311adff89e57a5a43c22efaf17a28260c0453c194080de3829b77`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb90d82e3b2e3e6edbec1939a5e443b23398135256508a851c64ffbfb2785b6`  
		Last Modified: Tue, 17 Feb 2026 21:24:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:8caeef10dc8172d7f92fb18cf344a138f7c342d30cec0691b3528c807ee2191d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c93adbe2897c872eb91e7697bbcb946f9b74849a2701dd813bf59729d0f4f69`

```dockerfile
```

-	Layers:
	-	`sha256:398dee132eb9bd91b6798844faeee3adec45b1e3bc20054ed556aec9a28598cb`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c9f5cdbb5d9f9b9ed1c2bc4d01442aeb46ac6970bfd6b5c7619ccebf2a6d8d`  
		Last Modified: Tue, 17 Feb 2026 21:24:42 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:b8863cd1352a9baaadc6108c36fc67b7d125a152138241a37f237db70b32e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107728862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab877e154471a2899c3269679a4b14a586bd5bd1283570fa4ffb9ebe01ed72f3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:38 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:38 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:40 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2e1ffbed2e086872db296d7127853f11bef6e4799f7cb2b4e156095c1e23b`  
		Last Modified: Tue, 17 Feb 2026 20:19:12 GMT  
		Size: 16.1 MB (16072781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe4e0b231918fe2ead0afa921cbeff424dd42baa4d098009cc336e8441dc5e`  
		Last Modified: Tue, 17 Feb 2026 20:19:40 GMT  
		Size: 52.2 MB (52155631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abcf86440735c564d25176f95b4c79e326dbe28b63b3010e2a001ef88ee4e6a`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4eb0849933a83cc6f6987607d815fae05c7034219ce685e6c36b1e732367c8`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b21e05a99c7d57fe8f747e682f910c8d2927319907cb0588370e923efad2b`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055b6ef92e76375fb137aa7b087a69b5dcdae095060fd53d309aa4a5b3889733`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 8.7 MB (8665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac06bd993cf9e2355a7d44f86dbc4a20e0d129ea9581f7a5748ebee6a8ec6f4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.4 MB (3441317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbde0472c9860b7c2a9dbe01f6847bd802a1be89e51ab0860955bdc20ec9e21`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b37963e4f06320a583ae14bbc0b6bc1d5771ae5c0cffc74c5e9efbd11607b7`  
		Last Modified: Tue, 17 Feb 2026 21:25:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:99f79d4038f7b077ae294cecc1f7e91088ac1a481ee6b9c530c78e71ef8e855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40a6606d24abb82e7f025b6a0d2aba81e598933fbdf93c5796fdec535229631`

```dockerfile
```

-	Layers:
	-	`sha256:7a95cbb2ec3dfd2ab4f4e2ce087e6c14e7325ab13a655132eec6991d714fc4b4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f162b16313339322fe19692c99d992d15a10ae3539c04a2a95769b29496c8138`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1-alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:30a08754815f214a095da5749a65f163ea0d8d96f1176f5aec5d3434b073fc53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:cbe0274d5e14a1eb94fd7660bc52be22836ed7f910fda44e8d3ef5df34529f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111109544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d863007b16ca53f7a4e26c53215f895b5e86647b0aa5796c63e3855f6cc11`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:25 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:25 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:26 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:26 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:26 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:35 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:35 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:35 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:35 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:35 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d575991a97516fe461d4e4036a37490052a3d42ec380135d014249e16b1d678`  
		Last Modified: Tue, 17 Feb 2026 20:19:05 GMT  
		Size: 16.1 MB (16147788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f70e2ff0d31ec24265820e65fb54d456b519fdb231448a0215d65703962a577`  
		Last Modified: Tue, 17 Feb 2026 20:20:15 GMT  
		Size: 53.0 MB (52985649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ba00cee2ad0168cf5988afb99d1aebb4e9016bee9e9391836ea3460fbd969`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f3670b78ac53ea39b08a6d287c35de5e8b733eb3f29916247010553254e8d`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218d52aea3b1d5147762843a6f2d8bdd41619b747cd1b50285fa742a754c5cb8`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821fe225c8232aa3924c3e22e91b30789b9731a48497262f8afd0fe04fabe14b`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15a8aa57efd3268b02d02285e4589e19bea0517d7d8bee6ba54d37269888d51`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49ae8fc1d5311adff89e57a5a43c22efaf17a28260c0453c194080de3829b77`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb90d82e3b2e3e6edbec1939a5e443b23398135256508a851c64ffbfb2785b6`  
		Last Modified: Tue, 17 Feb 2026 21:24:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:8caeef10dc8172d7f92fb18cf344a138f7c342d30cec0691b3528c807ee2191d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c93adbe2897c872eb91e7697bbcb946f9b74849a2701dd813bf59729d0f4f69`

```dockerfile
```

-	Layers:
	-	`sha256:398dee132eb9bd91b6798844faeee3adec45b1e3bc20054ed556aec9a28598cb`  
		Last Modified: Tue, 17 Feb 2026 21:24:43 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c9f5cdbb5d9f9b9ed1c2bc4d01442aeb46ac6970bfd6b5c7619ccebf2a6d8d`  
		Last Modified: Tue, 17 Feb 2026 21:24:42 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:b8863cd1352a9baaadc6108c36fc67b7d125a152138241a37f237db70b32e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107728862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab877e154471a2899c3269679a4b14a586bd5bd1283570fa4ffb9ebe01ed72f3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:38 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Tue, 17 Feb 2026 21:24:38 GMT
WORKDIR /liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Tue, 17 Feb 2026 21:24:40 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_VERSION=0.2.14
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Tue, 17 Feb 2026 21:24:40 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.version=5.0.1
# Tue, 17 Feb 2026 21:24:40 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Tue, 17 Feb 2026 21:24:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENV DOCKER_LIQUIBASE=true
# Tue, 17 Feb 2026 21:24:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Tue, 17 Feb 2026 21:24:51 GMT
USER liquibase:liquibase
# Tue, 17 Feb 2026 21:24:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2e1ffbed2e086872db296d7127853f11bef6e4799f7cb2b4e156095c1e23b`  
		Last Modified: Tue, 17 Feb 2026 20:19:12 GMT  
		Size: 16.1 MB (16072781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe4e0b231918fe2ead0afa921cbeff424dd42baa4d098009cc336e8441dc5e`  
		Last Modified: Tue, 17 Feb 2026 20:19:40 GMT  
		Size: 52.2 MB (52155631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abcf86440735c564d25176f95b4c79e326dbe28b63b3010e2a001ef88ee4e6a`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4eb0849933a83cc6f6987607d815fae05c7034219ce685e6c36b1e732367c8`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b21e05a99c7d57fe8f747e682f910c8d2927319907cb0588370e923efad2b`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055b6ef92e76375fb137aa7b087a69b5dcdae095060fd53d309aa4a5b3889733`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 8.7 MB (8665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac06bd993cf9e2355a7d44f86dbc4a20e0d129ea9581f7a5748ebee6a8ec6f4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.4 MB (3441317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbde0472c9860b7c2a9dbe01f6847bd802a1be89e51ab0860955bdc20ec9e21`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b37963e4f06320a583ae14bbc0b6bc1d5771ae5c0cffc74c5e9efbd11607b7`  
		Last Modified: Tue, 17 Feb 2026 21:25:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:99f79d4038f7b077ae294cecc1f7e91088ac1a481ee6b9c530c78e71ef8e855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40a6606d24abb82e7f025b6a0d2aba81e598933fbdf93c5796fdec535229631`

```dockerfile
```

-	Layers:
	-	`sha256:7a95cbb2ec3dfd2ab4f4e2ce087e6c14e7325ab13a655132eec6991d714fc4b4`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f162b16313339322fe19692c99d992d15a10ae3539c04a2a95769b29496c8138`  
		Last Modified: Tue, 17 Feb 2026 21:24:59 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
