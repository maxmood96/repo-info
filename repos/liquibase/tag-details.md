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
$ docker pull liquibase@sha256:f37d1c72e9fde25e89b4a472cda73674ce98bde2d80e3755d544a222d4ac86f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:f4dc0b852d8f5a47b526f70bbe3caf969d0391e223ffd332023e6b17e9550772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111108844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7b83e859920427bf69d10591b767cb4cfe95522eccdb29f92a916ed8f503c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:11 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:11 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:13 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:18 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:18 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:18 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f300e476a4af62d3eb8108d4414f528a092430562a81753005205bcd852d5`  
		Last Modified: Thu, 05 Feb 2026 22:21:09 GMT  
		Size: 16.1 MB (16147805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a332353d462dfe66edcfe8b1844d862a3845095c181d98f91b2dcbdfc75aee`  
		Last Modified: Thu, 05 Feb 2026 22:21:10 GMT  
		Size: 53.0 MB (52985637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9aef824f98f969525143a997286ac4aac37599778499b84734a6d04af5b62e`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a0e575c8a1cb7a4895e5ec1779c6054d9d9733556ce673d407cda3d3a3d0d`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20962ca6035a260202c37f7a6878989dd5abfc06f4c24165a962878a1652049d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93704037916a2073ac3b11be735de72a0b6f6ac4386fd13c2253f0f8ac50c5`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 8.7 MB (8665794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a4f0cbf2da46812667b39f204938ccfeb3089852273444dc1b68b460080e0`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8ceb04de66f09285e694a48cb3bf4d2ddca726573fa6ba3a2ea6f100ab7e9`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938fa6d99268e8d8a61f66f5599e10cefbcf21febe29e93115ede9de470848e`  
		Last Modified: Thu, 05 Feb 2026 22:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:9180ae790b228d3eba04ab12bbca38f070f6d872e075da3cddca744f8556aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bd0e0a29b032b08c6e2dc67cf2c08e9cde77b3b64cdd1847affa33d2218567`

```dockerfile
```

-	Layers:
	-	`sha256:f51e456eb50cf3d8ed0b13c216b56730cb59d11ac6793290d309690b48725e5d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.9 MB (3901256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f650ae90d40ba9b8359abb388200ce3598f15c5ac0b6bb13c21fb10bb8532e`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:71712d682449119d870a3d6d437806c1433e8adbab0de81d61f15dc7a02597d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107726025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b8e22721a687f73748ccf9d04fabd0f43bd358d08b6f2e837ba1caccd0c061`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:08 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:08 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b74e59f4a2977bd147493969b81a71d324adcad8507f34dde0ce1dd8fb1d0f5`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 16.1 MB (16071549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4019ee84927424dda11a3fe488d18dadfeb23ebc7519c133a5b805a59fd5080`  
		Last Modified: Thu, 05 Feb 2026 22:20:11 GMT  
		Size: 52.2 MB (52155593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a84a7cc0285e1dca907592ad680cc05983d6ff179bbaf8fde1b1f80173a77ee`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fa20b50908f47baf72d0006de80ad9488b904484955d5df94a41a5ae7032d`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad643b78a4a829362d794caca7094f739ff6cbec3bc4696da6b5fd4d2728ec1`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d397dfccacd86bfe40faab651e6b286f8df966678811965d89b67018db0162c`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 8.7 MB (8665796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87840a19bbae44c5633bbb0207fb868a53fc9f8d1a7b99b2e2a7be33dbaa9bf2`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 3.4 MB (3441210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00710174575d8f3ec1256c5c7d2daff2ed429d8a109848af1e122f02827a8091`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c2fef01113a48e663cddeb0e38a10094655ce8f2666fb65ccd50a47e2cc276`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:79d31f528197d5ae04ea7072432131f27a4d62f0e4ddefa6407389d0dd85e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cbded76d99c940b42d54fb09cd786c2894b47c529bd28f77d8d5ba7a75530b`

```dockerfile
```

-	Layers:
	-	`sha256:61f3bfabbec752dcf5e0c9d305aa9a5dc691c051628a52da2e60bce48475f4eb`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 3.9 MB (3900924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139039470b53564f36b4b948d57af184a5538cd59dcb0dd4a2d8655823b046e6`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
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
$ docker pull liquibase@sha256:f37d1c72e9fde25e89b4a472cda73674ce98bde2d80e3755d544a222d4ac86f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:f4dc0b852d8f5a47b526f70bbe3caf969d0391e223ffd332023e6b17e9550772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111108844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7b83e859920427bf69d10591b767cb4cfe95522eccdb29f92a916ed8f503c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:11 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:11 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:13 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:18 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:18 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:18 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f300e476a4af62d3eb8108d4414f528a092430562a81753005205bcd852d5`  
		Last Modified: Thu, 05 Feb 2026 22:21:09 GMT  
		Size: 16.1 MB (16147805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a332353d462dfe66edcfe8b1844d862a3845095c181d98f91b2dcbdfc75aee`  
		Last Modified: Thu, 05 Feb 2026 22:21:10 GMT  
		Size: 53.0 MB (52985637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9aef824f98f969525143a997286ac4aac37599778499b84734a6d04af5b62e`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a0e575c8a1cb7a4895e5ec1779c6054d9d9733556ce673d407cda3d3a3d0d`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20962ca6035a260202c37f7a6878989dd5abfc06f4c24165a962878a1652049d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93704037916a2073ac3b11be735de72a0b6f6ac4386fd13c2253f0f8ac50c5`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 8.7 MB (8665794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a4f0cbf2da46812667b39f204938ccfeb3089852273444dc1b68b460080e0`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8ceb04de66f09285e694a48cb3bf4d2ddca726573fa6ba3a2ea6f100ab7e9`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938fa6d99268e8d8a61f66f5599e10cefbcf21febe29e93115ede9de470848e`  
		Last Modified: Thu, 05 Feb 2026 22:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:9180ae790b228d3eba04ab12bbca38f070f6d872e075da3cddca744f8556aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bd0e0a29b032b08c6e2dc67cf2c08e9cde77b3b64cdd1847affa33d2218567`

```dockerfile
```

-	Layers:
	-	`sha256:f51e456eb50cf3d8ed0b13c216b56730cb59d11ac6793290d309690b48725e5d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.9 MB (3901256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f650ae90d40ba9b8359abb388200ce3598f15c5ac0b6bb13c21fb10bb8532e`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:71712d682449119d870a3d6d437806c1433e8adbab0de81d61f15dc7a02597d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107726025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b8e22721a687f73748ccf9d04fabd0f43bd358d08b6f2e837ba1caccd0c061`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:08 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:08 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b74e59f4a2977bd147493969b81a71d324adcad8507f34dde0ce1dd8fb1d0f5`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 16.1 MB (16071549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4019ee84927424dda11a3fe488d18dadfeb23ebc7519c133a5b805a59fd5080`  
		Last Modified: Thu, 05 Feb 2026 22:20:11 GMT  
		Size: 52.2 MB (52155593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a84a7cc0285e1dca907592ad680cc05983d6ff179bbaf8fde1b1f80173a77ee`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fa20b50908f47baf72d0006de80ad9488b904484955d5df94a41a5ae7032d`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad643b78a4a829362d794caca7094f739ff6cbec3bc4696da6b5fd4d2728ec1`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d397dfccacd86bfe40faab651e6b286f8df966678811965d89b67018db0162c`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 8.7 MB (8665796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87840a19bbae44c5633bbb0207fb868a53fc9f8d1a7b99b2e2a7be33dbaa9bf2`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 3.4 MB (3441210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00710174575d8f3ec1256c5c7d2daff2ed429d8a109848af1e122f02827a8091`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c2fef01113a48e663cddeb0e38a10094655ce8f2666fb65ccd50a47e2cc276`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:79d31f528197d5ae04ea7072432131f27a4d62f0e4ddefa6407389d0dd85e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cbded76d99c940b42d54fb09cd786c2894b47c529bd28f77d8d5ba7a75530b`

```dockerfile
```

-	Layers:
	-	`sha256:61f3bfabbec752dcf5e0c9d305aa9a5dc691c051628a52da2e60bce48475f4eb`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 3.9 MB (3900924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139039470b53564f36b4b948d57af184a5538cd59dcb0dd4a2d8655823b046e6`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
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
$ docker pull liquibase@sha256:f37d1c72e9fde25e89b4a472cda73674ce98bde2d80e3755d544a222d4ac86f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:f4dc0b852d8f5a47b526f70bbe3caf969d0391e223ffd332023e6b17e9550772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111108844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7b83e859920427bf69d10591b767cb4cfe95522eccdb29f92a916ed8f503c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:11 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:11 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:13 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:13 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:13 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:18 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:18 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:18 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:18 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f300e476a4af62d3eb8108d4414f528a092430562a81753005205bcd852d5`  
		Last Modified: Thu, 05 Feb 2026 22:21:09 GMT  
		Size: 16.1 MB (16147805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a332353d462dfe66edcfe8b1844d862a3845095c181d98f91b2dcbdfc75aee`  
		Last Modified: Thu, 05 Feb 2026 22:21:10 GMT  
		Size: 53.0 MB (52985637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9aef824f98f969525143a997286ac4aac37599778499b84734a6d04af5b62e`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a0e575c8a1cb7a4895e5ec1779c6054d9d9733556ce673d407cda3d3a3d0d`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20962ca6035a260202c37f7a6878989dd5abfc06f4c24165a962878a1652049d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93704037916a2073ac3b11be735de72a0b6f6ac4386fd13c2253f0f8ac50c5`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 8.7 MB (8665794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a4f0cbf2da46812667b39f204938ccfeb3089852273444dc1b68b460080e0`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8ceb04de66f09285e694a48cb3bf4d2ddca726573fa6ba3a2ea6f100ab7e9`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938fa6d99268e8d8a61f66f5599e10cefbcf21febe29e93115ede9de470848e`  
		Last Modified: Thu, 05 Feb 2026 22:50:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:9180ae790b228d3eba04ab12bbca38f070f6d872e075da3cddca744f8556aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bd0e0a29b032b08c6e2dc67cf2c08e9cde77b3b64cdd1847affa33d2218567`

```dockerfile
```

-	Layers:
	-	`sha256:f51e456eb50cf3d8ed0b13c216b56730cb59d11ac6793290d309690b48725e5d`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 3.9 MB (3901256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f650ae90d40ba9b8359abb388200ce3598f15c5ac0b6bb13c21fb10bb8532e`  
		Last Modified: Thu, 05 Feb 2026 22:50:27 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:71712d682449119d870a3d6d437806c1433e8adbab0de81d61f15dc7a02597d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107726025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b8e22721a687f73748ccf9d04fabd0f43bd358d08b6f2e837ba1caccd0c061`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:19:53 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:08 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Thu, 05 Feb 2026 22:50:08 GMT
WORKDIR /liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Thu, 05 Feb 2026 22:50:10 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_VERSION=0.2.14
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Thu, 05 Feb 2026 22:50:10 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.version=5.0.1
# Thu, 05 Feb 2026 22:50:10 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Thu, 05 Feb 2026 22:50:17 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 05 Feb 2026 22:50:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
USER liquibase:liquibase
# Thu, 05 Feb 2026 22:50:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b74e59f4a2977bd147493969b81a71d324adcad8507f34dde0ce1dd8fb1d0f5`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 16.1 MB (16071549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4019ee84927424dda11a3fe488d18dadfeb23ebc7519c133a5b805a59fd5080`  
		Last Modified: Thu, 05 Feb 2026 22:20:11 GMT  
		Size: 52.2 MB (52155593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a84a7cc0285e1dca907592ad680cc05983d6ff179bbaf8fde1b1f80173a77ee`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fa20b50908f47baf72d0006de80ad9488b904484955d5df94a41a5ae7032d`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad643b78a4a829362d794caca7094f739ff6cbec3bc4696da6b5fd4d2728ec1`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d397dfccacd86bfe40faab651e6b286f8df966678811965d89b67018db0162c`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 8.7 MB (8665796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87840a19bbae44c5633bbb0207fb868a53fc9f8d1a7b99b2e2a7be33dbaa9bf2`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 3.4 MB (3441210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00710174575d8f3ec1256c5c7d2daff2ed429d8a109848af1e122f02827a8091`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c2fef01113a48e663cddeb0e38a10094655ce8f2666fb65ccd50a47e2cc276`  
		Last Modified: Thu, 05 Feb 2026 22:50:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:79d31f528197d5ae04ea7072432131f27a4d62f0e4ddefa6407389d0dd85e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cbded76d99c940b42d54fb09cd786c2894b47c529bd28f77d8d5ba7a75530b`

```dockerfile
```

-	Layers:
	-	`sha256:61f3bfabbec752dcf5e0c9d305aa9a5dc691c051628a52da2e60bce48475f4eb`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 3.9 MB (3900924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139039470b53564f36b4b948d57af184a5538cd59dcb0dd4a2d8655823b046e6`  
		Last Modified: Thu, 05 Feb 2026 22:50:25 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
