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
$ docker pull liquibase@sha256:d32791cda3c21341a32de3b4ee2b9dd6011ceb9504b58f72d0bb16f907c630cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:7aca0b6cee3df49a1cbd523d474780d0d3093093ba1ba9497fc6ecc00bc6cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111311694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8576262e7f46721727455323be0fa770d45adc8227e2040603b98768fce4bdd`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:20 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:39:20 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:39:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:39:27 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:39:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434fc527435d14ec923b0acc9953dacb6ec1bd892d7d48eb54eb7a312aa0f5b`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 53.0 MB (52985647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf851d0cdffee253ce46e5cdf9a5c19c21be33fa5231efb26464aa3846ec0f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed9e099432789068ce1d3578eeff3f3c7b7db69e22b254afc8941073a1cfd`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c79ac736d59e190eb4085e35989155e87a681372ee3c543c4c05e02b7ddde7`  
		Last Modified: Wed, 15 Apr 2026 21:39:35 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470d81a2b49e664d09fa00475b00b7b370dcbed8ca4a6002b7df660f4a44c040`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c4c3558213483d21933b731fd97c5a78328cc059b1c0a487e423d2133bf8c`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.8 MB (3764521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4def313b4ef3f3b133a908ab22b843ca624211d93346c45d7b8214f7db7b26`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b934ad6d2ce59ac312ae8597506c3c3d477e315197a219d424a061386eb53ee`  
		Last Modified: Wed, 15 Apr 2026 21:39:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:471d2b3cd45d17f254108f95b68c15a073f57f1826cca61ba044c534d2313c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f1e80f11fa6f6fa4990ca9e560591241d17538649362126667966581d3adcb`

```dockerfile
```

-	Layers:
	-	`sha256:aec908c17f4f601b622ea75c41baf401e3cb020dc55fb2929f7aeb9aa2993db0`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49cb2bec83d881716101da9c7fe584be9de31bfc11c7d27f5d63883e39351c5`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:94a33c58f906f8cc3ac660e4609d6b3b6f4d37a62e9a6dafa9afb7af52586c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5750ed561ea4efc3964f1384fc29b5f58690fbbd90d10e139e2618c01aee5df`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:50:59 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:51:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:51:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:51:10 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:51:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976ad46810a0a1b423803f447753b429b04144c676b1d429a09e94303e03d1b`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 16.1 MB (16075150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471cc4701b229f4446be5d8c981bd3d0eeb429de8c98c2bd5869d49f549d8e4d`  
		Last Modified: Wed, 15 Apr 2026 20:34:48 GMT  
		Size: 52.2 MB (52155611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df963689a6ce26de9c84e4dc05e2f0a2086bdc9709bd12098f0a1f50ddd4485`  
		Last Modified: Wed, 15 Apr 2026 20:34:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e1d661ef05644b20d264beb4376aab10dc6ab7dfd0fa292caf433a1b564d6`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a44d0fb4e7c478abcd296fbc074b0b71f08fc3556aa9f5de84ddafc894a74e8`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19560702612f561994a92c9d741f2ba45dd3f32fd478ac65290f84a5a27239ab`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab9d8528f372163742339f7b13ecd6e72ac3eb71db2bac0ab4d51678ecf1e4e`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.4 MB (3441239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d29a1bc0bafdee80c3e72648638d213746526cdeeaca136b7ac1a3b01a9237d`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42d22a0d6c70018e131e080c034c21225b812d9fd5b3830a1b8800c7673ad1`  
		Last Modified: Wed, 15 Apr 2026 21:51:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:15688f8690904dcf0a3e10ad45f894f4e2e9f9e91b83549d00e7c5254987d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e92b07474edf43932cdfb839f4253b6fd47bb8f419fe9e7ae96a295741344b3`

```dockerfile
```

-	Layers:
	-	`sha256:ca36c57f14580a6fc4db9d58313a55f24532653538605fb82402277f014b4dbd`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870ccacd94f882cd79dd6491fd4ac4c9ddf5c65e442f9b17a6ab24d37c1dee53`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
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
$ docker pull liquibase@sha256:d32791cda3c21341a32de3b4ee2b9dd6011ceb9504b58f72d0bb16f907c630cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:7aca0b6cee3df49a1cbd523d474780d0d3093093ba1ba9497fc6ecc00bc6cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111311694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8576262e7f46721727455323be0fa770d45adc8227e2040603b98768fce4bdd`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:20 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:39:20 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:39:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:39:27 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:39:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434fc527435d14ec923b0acc9953dacb6ec1bd892d7d48eb54eb7a312aa0f5b`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 53.0 MB (52985647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf851d0cdffee253ce46e5cdf9a5c19c21be33fa5231efb26464aa3846ec0f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed9e099432789068ce1d3578eeff3f3c7b7db69e22b254afc8941073a1cfd`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c79ac736d59e190eb4085e35989155e87a681372ee3c543c4c05e02b7ddde7`  
		Last Modified: Wed, 15 Apr 2026 21:39:35 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470d81a2b49e664d09fa00475b00b7b370dcbed8ca4a6002b7df660f4a44c040`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c4c3558213483d21933b731fd97c5a78328cc059b1c0a487e423d2133bf8c`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.8 MB (3764521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4def313b4ef3f3b133a908ab22b843ca624211d93346c45d7b8214f7db7b26`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b934ad6d2ce59ac312ae8597506c3c3d477e315197a219d424a061386eb53ee`  
		Last Modified: Wed, 15 Apr 2026 21:39:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:471d2b3cd45d17f254108f95b68c15a073f57f1826cca61ba044c534d2313c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f1e80f11fa6f6fa4990ca9e560591241d17538649362126667966581d3adcb`

```dockerfile
```

-	Layers:
	-	`sha256:aec908c17f4f601b622ea75c41baf401e3cb020dc55fb2929f7aeb9aa2993db0`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49cb2bec83d881716101da9c7fe584be9de31bfc11c7d27f5d63883e39351c5`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:94a33c58f906f8cc3ac660e4609d6b3b6f4d37a62e9a6dafa9afb7af52586c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5750ed561ea4efc3964f1384fc29b5f58690fbbd90d10e139e2618c01aee5df`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:50:59 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:51:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:51:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:51:10 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:51:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976ad46810a0a1b423803f447753b429b04144c676b1d429a09e94303e03d1b`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 16.1 MB (16075150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471cc4701b229f4446be5d8c981bd3d0eeb429de8c98c2bd5869d49f549d8e4d`  
		Last Modified: Wed, 15 Apr 2026 20:34:48 GMT  
		Size: 52.2 MB (52155611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df963689a6ce26de9c84e4dc05e2f0a2086bdc9709bd12098f0a1f50ddd4485`  
		Last Modified: Wed, 15 Apr 2026 20:34:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e1d661ef05644b20d264beb4376aab10dc6ab7dfd0fa292caf433a1b564d6`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a44d0fb4e7c478abcd296fbc074b0b71f08fc3556aa9f5de84ddafc894a74e8`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19560702612f561994a92c9d741f2ba45dd3f32fd478ac65290f84a5a27239ab`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab9d8528f372163742339f7b13ecd6e72ac3eb71db2bac0ab4d51678ecf1e4e`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.4 MB (3441239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d29a1bc0bafdee80c3e72648638d213746526cdeeaca136b7ac1a3b01a9237d`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42d22a0d6c70018e131e080c034c21225b812d9fd5b3830a1b8800c7673ad1`  
		Last Modified: Wed, 15 Apr 2026 21:51:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:15688f8690904dcf0a3e10ad45f894f4e2e9f9e91b83549d00e7c5254987d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e92b07474edf43932cdfb839f4253b6fd47bb8f419fe9e7ae96a295741344b3`

```dockerfile
```

-	Layers:
	-	`sha256:ca36c57f14580a6fc4db9d58313a55f24532653538605fb82402277f014b4dbd`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870ccacd94f882cd79dd6491fd4ac4c9ddf5c65e442f9b17a6ab24d37c1dee53`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
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
$ docker pull liquibase@sha256:d32791cda3c21341a32de3b4ee2b9dd6011ceb9504b58f72d0bb16f907c630cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:7aca0b6cee3df49a1cbd523d474780d0d3093093ba1ba9497fc6ecc00bc6cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111311694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8576262e7f46721727455323be0fa770d45adc8227e2040603b98768fce4bdd`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:20 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:39:20 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:39:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:39:21 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:39:21 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:39:27 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:39:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:39:27 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:39:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:39:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434fc527435d14ec923b0acc9953dacb6ec1bd892d7d48eb54eb7a312aa0f5b`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 53.0 MB (52985647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf851d0cdffee253ce46e5cdf9a5c19c21be33fa5231efb26464aa3846ec0f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed9e099432789068ce1d3578eeff3f3c7b7db69e22b254afc8941073a1cfd`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c79ac736d59e190eb4085e35989155e87a681372ee3c543c4c05e02b7ddde7`  
		Last Modified: Wed, 15 Apr 2026 21:39:35 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470d81a2b49e664d09fa00475b00b7b370dcbed8ca4a6002b7df660f4a44c040`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 8.7 MB (8665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c4c3558213483d21933b731fd97c5a78328cc059b1c0a487e423d2133bf8c`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.8 MB (3764521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4def313b4ef3f3b133a908ab22b843ca624211d93346c45d7b8214f7db7b26`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b934ad6d2ce59ac312ae8597506c3c3d477e315197a219d424a061386eb53ee`  
		Last Modified: Wed, 15 Apr 2026 21:39:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:471d2b3cd45d17f254108f95b68c15a073f57f1826cca61ba044c534d2313c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f1e80f11fa6f6fa4990ca9e560591241d17538649362126667966581d3adcb`

```dockerfile
```

-	Layers:
	-	`sha256:aec908c17f4f601b622ea75c41baf401e3cb020dc55fb2929f7aeb9aa2993db0`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49cb2bec83d881716101da9c7fe584be9de31bfc11c7d27f5d63883e39351c5`  
		Last Modified: Wed, 15 Apr 2026 21:39:36 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:94a33c58f906f8cc3ac660e4609d6b3b6f4d37a62e9a6dafa9afb7af52586c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5750ed561ea4efc3964f1384fc29b5f58690fbbd90d10e139e2618c01aee5df`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:50:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 15 Apr 2026 21:50:59 GMT
WORKDIR /liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 15 Apr 2026 21:51:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_VERSION=0.2.14
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 15 Apr 2026 21:51:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 15 Apr 2026 21:51:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 15 Apr 2026 21:51:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 15 Apr 2026 21:51:10 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 15 Apr 2026 21:51:10 GMT
USER liquibase:liquibase
# Wed, 15 Apr 2026 21:51:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:51:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976ad46810a0a1b423803f447753b429b04144c676b1d429a09e94303e03d1b`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 16.1 MB (16075150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471cc4701b229f4446be5d8c981bd3d0eeb429de8c98c2bd5869d49f549d8e4d`  
		Last Modified: Wed, 15 Apr 2026 20:34:48 GMT  
		Size: 52.2 MB (52155611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df963689a6ce26de9c84e4dc05e2f0a2086bdc9709bd12098f0a1f50ddd4485`  
		Last Modified: Wed, 15 Apr 2026 20:34:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e1d661ef05644b20d264beb4376aab10dc6ab7dfd0fa292caf433a1b564d6`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a44d0fb4e7c478abcd296fbc074b0b71f08fc3556aa9f5de84ddafc894a74e8`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19560702612f561994a92c9d741f2ba45dd3f32fd478ac65290f84a5a27239ab`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab9d8528f372163742339f7b13ecd6e72ac3eb71db2bac0ab4d51678ecf1e4e`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.4 MB (3441239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d29a1bc0bafdee80c3e72648638d213746526cdeeaca136b7ac1a3b01a9237d`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42d22a0d6c70018e131e080c034c21225b812d9fd5b3830a1b8800c7673ad1`  
		Last Modified: Wed, 15 Apr 2026 21:51:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:15688f8690904dcf0a3e10ad45f894f4e2e9f9e91b83549d00e7c5254987d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e92b07474edf43932cdfb839f4253b6fd47bb8f419fe9e7ae96a295741344b3`

```dockerfile
```

-	Layers:
	-	`sha256:ca36c57f14580a6fc4db9d58313a55f24532653538605fb82402277f014b4dbd`  
		Last Modified: Wed, 15 Apr 2026 21:51:18 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870ccacd94f882cd79dd6491fd4ac4c9ddf5c65e442f9b17a6ab24d37c1dee53`  
		Last Modified: Wed, 15 Apr 2026 21:51:17 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
