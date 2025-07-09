<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.33`](#liquibase433)
-	[`liquibase:4.33-alpine`](#liquibase433-alpine)
-	[`liquibase:4.33.0`](#liquibase4330)
-	[`liquibase:4.33.0-alpine`](#liquibase4330-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.33`

```console
$ docker pull liquibase@sha256:544ac2748d04174603f1b0495570a18023172cdb1f7643ed32072760705e180a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33` - linux; amd64

```console
$ docker pull liquibase@sha256:9df5e219b3d4c4a0ac1f78f1b3bf766c1e08079693f7a9c2f5bb28b323ab6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456685577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9e92189627f0afeb548a52c1af904bfaeb1cc1e338a2cd1d59527c48b1b0ff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43186e9339c95b15376ec7176560dc5f984c271d45fc58aa5e17cdbd7e356f3`  
		Last Modified: Wed, 09 Jul 2025 20:12:38 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ed63f42d7e4bfdb6c8de27647b88bef5a8204f83784d6f65ff2ac6d553203`  
		Last Modified: Wed, 09 Jul 2025 21:43:11 GMT  
		Size: 354.4 MB (354408299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9df7a05a912a709130646595d24b2b41b4d28ed7ce86f507dabe06ec9b6f4`  
		Last Modified: Wed, 09 Jul 2025 20:12:46 GMT  
		Size: 3.7 MB (3696548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aa3a1a07e7feccfde731e9a348ebf3316245e2c6ba232f7e884f6e3bdf3e60`  
		Last Modified: Wed, 09 Jul 2025 20:12:51 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0e248b6a6dab64e44af43a4ec6a3ebf5ee9bf46d8479dda4b6024ddaca99d`  
		Last Modified: Wed, 09 Jul 2025 20:12:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:ed61a9553c5252daea65b3c8b873a9bd35ce3436e0f9852c80f8e2f0d6cc5112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b9028fb88803fad5ebe58d92bf07402e26ed02fb21cfd1f545718ce77878dc`

```dockerfile
```

-	Layers:
	-	`sha256:59e4ce0186c67de921000a596f4481ebd72d5bbd449779a8efd511fc2f3b8f3d`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e72bd00bf85887bd191302144d7bbc2271affdf088d0c6fff221116a2c185a4`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f9630b80da904131922b859aab548b6fcf0995ccf3b70059d7410e9c3f90c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.3 MB (453311125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbff287b779e8c854a2b6a5a7b7448eccff97521e3c38705cd07ef764baf2818`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b118eb757ac7763a739a3d3815afaec9105a13de997d34ceb84cfceeb9e5f`  
		Last Modified: Wed, 09 Jul 2025 22:34:28 GMT  
		Size: 354.4 MB (354408294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98e22c567a78264a81e4b97e0bafb823e0a61209b0be26ac466dec693deee72`  
		Last Modified: Wed, 09 Jul 2025 20:23:25 GMT  
		Size: 3.4 MB (3405518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a67f69f01f0a54c3d90c560a6c89f398bab30a34271991a37f201ec00809d`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1cfcd0d2fc07d2831775770d6f477edf9b68ca2262af4fe115eeae47b7dfd`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33` - unknown; unknown

```console
$ docker pull liquibase@sha256:5f864465ca1aa18ce4599bc9c56bebf1d91c5dec43f09a60894733cb6c76ac5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130725a841759197bb89c19ee47a49ddd0a3f444953348d490560dd8fb789734`

```dockerfile
```

-	Layers:
	-	`sha256:bfe50c8247ec8851b09bbeea8f936fc215b9127967d729ffb28b9a3e264b853c`  
		Last Modified: Wed, 09 Jul 2025 21:39:27 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c1b89efaf7239bb3502ef47e1ea37ae66dc313b9c1eaa5a0396ddcb5db9880`  
		Last Modified: Wed, 09 Jul 2025 21:39:28 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33-alpine`

```console
$ docker pull liquibase@sha256:5e620416683a8b76e72a90b84df0cae37fae6427c3f7ec64069791f96f403b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c309975b746aca9d9b7a31f884e65cbcba3137d33a8750e6c7e36068084cafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429646046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b083f5cf0f76274ff676fedc33da3e85853306c0e7362f1335f89aba04a99886`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04661512e3672b349f8824a94a0ce214c0d1c1c46b92d0fd533b40d2c5e548f1`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad37e982a9379fa4ba7ff3490fefcd8af915b5ef6ecf49475bdf02f840d122`  
		Last Modified: Wed, 09 Jul 2025 19:59:30 GMT  
		Size: 67.8 MB (67800393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b3981deba2179f4e269f0778dc7c3a3dc0eb19744003f1518a68b5341f891`  
		Last Modified: Wed, 09 Jul 2025 19:59:01 GMT  
		Size: 354.4 MB (354431085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3812ce921fee006c438096d29b14ba966adceec2ecbe3069dd05712845c653`  
		Last Modified: Wed, 09 Jul 2025 19:59:26 GMT  
		Size: 3.6 MB (3616110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca701866794160219494e7e4d53c3a12c7f8d8246d4980d21a5da4d0a45d216`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc826f5b9276b3c910bb80a031ff133c34dfe728ac69041d94adb6552bcf93e`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a6e862a8953db9f0fc185b176094e671ea46cbc181c05730a1d556c64f871ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.7 KB (425744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e8156e74b3ca294bca526023e642e3bb2347f1cc8a359adb7d841589b9ab03`

```dockerfile
```

-	Layers:
	-	`sha256:a8ef69a77f438781832ce47616b7148da57d14f091c1fec9feb463751c093ea5`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 404.0 KB (404031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2fba02a46b3246b86d84283002e93b1db9781ed73f6e4fd1a39872ab3ec045`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c0de4d9b7cb3cc102a1898b776ed13da48d2d2430fd36d3d31fa85d2b8063168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428696150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32567c70bcc575cb5a9becb968c3827c7105f70216a25437791c655b388c6421`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d889d0ac9e8307b4c08661c76a81b965d2fae37e45747b72e6db533b5839fae`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31c9e5502ce5d0c33f17beda02f924fb28b35cc10f9a654d68b926a7cd2ec1`  
		Last Modified: Wed, 09 Jul 2025 20:24:18 GMT  
		Size: 66.8 MB (66803159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1b42d769c4e371237b0e136c02ee1dadc6f4be783d8f155e0bbf3539834120`  
		Last Modified: Wed, 09 Jul 2025 20:23:59 GMT  
		Size: 354.4 MB (354430919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3442c9110a33c517d4e0101ea5109215ac2c2c71bc5cd9f78356bcdfb22b1abd`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 3.3 MB (3324515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a71c0204b0d1bf13b05909c050347f3efe0411d2e0bef3b368a0a3862ec599`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea2af4763b4915197f23de8faefc0746a03faf8c0739c92f6629b265023c541`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:eace7156570ae94ddd2f731e651839fb2d13cf28d6d420a9cc581d0904339f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 KB (425128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b7a0054b786050dfec1c9121cd257a643d78b2b9d26f6dc9fb0628b6d082d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e2d7496f123b444f0592c3e9bb0464d51fc94578f1b45758734efb89abdcc`  
		Last Modified: Wed, 09 Jul 2025 21:39:33 GMT  
		Size: 403.3 KB (403278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d218135e2f832988120e3f396bbe2430c938d3ad018c30412106a7731962912`  
		Last Modified: Wed, 09 Jul 2025 21:39:34 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33.0`

```console
$ docker pull liquibase@sha256:544ac2748d04174603f1b0495570a18023172cdb1f7643ed32072760705e180a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33.0` - linux; amd64

```console
$ docker pull liquibase@sha256:9df5e219b3d4c4a0ac1f78f1b3bf766c1e08079693f7a9c2f5bb28b323ab6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456685577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9e92189627f0afeb548a52c1af904bfaeb1cc1e338a2cd1d59527c48b1b0ff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43186e9339c95b15376ec7176560dc5f984c271d45fc58aa5e17cdbd7e356f3`  
		Last Modified: Wed, 09 Jul 2025 20:12:38 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ed63f42d7e4bfdb6c8de27647b88bef5a8204f83784d6f65ff2ac6d553203`  
		Last Modified: Wed, 09 Jul 2025 21:43:11 GMT  
		Size: 354.4 MB (354408299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9df7a05a912a709130646595d24b2b41b4d28ed7ce86f507dabe06ec9b6f4`  
		Last Modified: Wed, 09 Jul 2025 20:12:46 GMT  
		Size: 3.7 MB (3696548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aa3a1a07e7feccfde731e9a348ebf3316245e2c6ba232f7e884f6e3bdf3e60`  
		Last Modified: Wed, 09 Jul 2025 20:12:51 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0e248b6a6dab64e44af43a4ec6a3ebf5ee9bf46d8479dda4b6024ddaca99d`  
		Last Modified: Wed, 09 Jul 2025 20:12:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:ed61a9553c5252daea65b3c8b873a9bd35ce3436e0f9852c80f8e2f0d6cc5112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b9028fb88803fad5ebe58d92bf07402e26ed02fb21cfd1f545718ce77878dc`

```dockerfile
```

-	Layers:
	-	`sha256:59e4ce0186c67de921000a596f4481ebd72d5bbd449779a8efd511fc2f3b8f3d`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e72bd00bf85887bd191302144d7bbc2271affdf088d0c6fff221116a2c185a4`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f9630b80da904131922b859aab548b6fcf0995ccf3b70059d7410e9c3f90c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.3 MB (453311125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbff287b779e8c854a2b6a5a7b7448eccff97521e3c38705cd07ef764baf2818`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b118eb757ac7763a739a3d3815afaec9105a13de997d34ceb84cfceeb9e5f`  
		Last Modified: Wed, 09 Jul 2025 22:34:28 GMT  
		Size: 354.4 MB (354408294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98e22c567a78264a81e4b97e0bafb823e0a61209b0be26ac466dec693deee72`  
		Last Modified: Wed, 09 Jul 2025 20:23:25 GMT  
		Size: 3.4 MB (3405518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a67f69f01f0a54c3d90c560a6c89f398bab30a34271991a37f201ec00809d`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1cfcd0d2fc07d2831775770d6f477edf9b68ca2262af4fe115eeae47b7dfd`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:5f864465ca1aa18ce4599bc9c56bebf1d91c5dec43f09a60894733cb6c76ac5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130725a841759197bb89c19ee47a49ddd0a3f444953348d490560dd8fb789734`

```dockerfile
```

-	Layers:
	-	`sha256:bfe50c8247ec8851b09bbeea8f936fc215b9127967d729ffb28b9a3e264b853c`  
		Last Modified: Wed, 09 Jul 2025 21:39:27 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c1b89efaf7239bb3502ef47e1ea37ae66dc313b9c1eaa5a0396ddcb5db9880`  
		Last Modified: Wed, 09 Jul 2025 21:39:28 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.33.0-alpine`

```console
$ docker pull liquibase@sha256:5e620416683a8b76e72a90b84df0cae37fae6427c3f7ec64069791f96f403b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.33.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c309975b746aca9d9b7a31f884e65cbcba3137d33a8750e6c7e36068084cafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429646046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b083f5cf0f76274ff676fedc33da3e85853306c0e7362f1335f89aba04a99886`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04661512e3672b349f8824a94a0ce214c0d1c1c46b92d0fd533b40d2c5e548f1`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad37e982a9379fa4ba7ff3490fefcd8af915b5ef6ecf49475bdf02f840d122`  
		Last Modified: Wed, 09 Jul 2025 19:59:30 GMT  
		Size: 67.8 MB (67800393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b3981deba2179f4e269f0778dc7c3a3dc0eb19744003f1518a68b5341f891`  
		Last Modified: Wed, 09 Jul 2025 19:59:01 GMT  
		Size: 354.4 MB (354431085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3812ce921fee006c438096d29b14ba966adceec2ecbe3069dd05712845c653`  
		Last Modified: Wed, 09 Jul 2025 19:59:26 GMT  
		Size: 3.6 MB (3616110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca701866794160219494e7e4d53c3a12c7f8d8246d4980d21a5da4d0a45d216`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc826f5b9276b3c910bb80a031ff133c34dfe728ac69041d94adb6552bcf93e`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a6e862a8953db9f0fc185b176094e671ea46cbc181c05730a1d556c64f871ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.7 KB (425744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e8156e74b3ca294bca526023e642e3bb2347f1cc8a359adb7d841589b9ab03`

```dockerfile
```

-	Layers:
	-	`sha256:a8ef69a77f438781832ce47616b7148da57d14f091c1fec9feb463751c093ea5`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 404.0 KB (404031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2fba02a46b3246b86d84283002e93b1db9781ed73f6e4fd1a39872ab3ec045`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.33.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c0de4d9b7cb3cc102a1898b776ed13da48d2d2430fd36d3d31fa85d2b8063168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428696150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32567c70bcc575cb5a9becb968c3827c7105f70216a25437791c655b388c6421`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d889d0ac9e8307b4c08661c76a81b965d2fae37e45747b72e6db533b5839fae`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31c9e5502ce5d0c33f17beda02f924fb28b35cc10f9a654d68b926a7cd2ec1`  
		Last Modified: Wed, 09 Jul 2025 20:24:18 GMT  
		Size: 66.8 MB (66803159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1b42d769c4e371237b0e136c02ee1dadc6f4be783d8f155e0bbf3539834120`  
		Last Modified: Wed, 09 Jul 2025 20:23:59 GMT  
		Size: 354.4 MB (354430919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3442c9110a33c517d4e0101ea5109215ac2c2c71bc5cd9f78356bcdfb22b1abd`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 3.3 MB (3324515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a71c0204b0d1bf13b05909c050347f3efe0411d2e0bef3b368a0a3862ec599`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea2af4763b4915197f23de8faefc0746a03faf8c0739c92f6629b265023c541`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.33.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:eace7156570ae94ddd2f731e651839fb2d13cf28d6d420a9cc581d0904339f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 KB (425128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b7a0054b786050dfec1c9121cd257a643d78b2b9d26f6dc9fb0628b6d082d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e2d7496f123b444f0592c3e9bb0464d51fc94578f1b45758734efb89abdcc`  
		Last Modified: Wed, 09 Jul 2025 21:39:33 GMT  
		Size: 403.3 KB (403278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d218135e2f832988120e3f396bbe2430c938d3ad018c30412106a7731962912`  
		Last Modified: Wed, 09 Jul 2025 21:39:34 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:5e620416683a8b76e72a90b84df0cae37fae6427c3f7ec64069791f96f403b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c309975b746aca9d9b7a31f884e65cbcba3137d33a8750e6c7e36068084cafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429646046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b083f5cf0f76274ff676fedc33da3e85853306c0e7362f1335f89aba04a99886`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04661512e3672b349f8824a94a0ce214c0d1c1c46b92d0fd533b40d2c5e548f1`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ad37e982a9379fa4ba7ff3490fefcd8af915b5ef6ecf49475bdf02f840d122`  
		Last Modified: Wed, 09 Jul 2025 19:59:30 GMT  
		Size: 67.8 MB (67800393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b3981deba2179f4e269f0778dc7c3a3dc0eb19744003f1518a68b5341f891`  
		Last Modified: Wed, 09 Jul 2025 19:59:01 GMT  
		Size: 354.4 MB (354431085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3812ce921fee006c438096d29b14ba966adceec2ecbe3069dd05712845c653`  
		Last Modified: Wed, 09 Jul 2025 19:59:26 GMT  
		Size: 3.6 MB (3616110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca701866794160219494e7e4d53c3a12c7f8d8246d4980d21a5da4d0a45d216`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc826f5b9276b3c910bb80a031ff133c34dfe728ac69041d94adb6552bcf93e`  
		Last Modified: Wed, 09 Jul 2025 19:59:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a6e862a8953db9f0fc185b176094e671ea46cbc181c05730a1d556c64f871ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.7 KB (425744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e8156e74b3ca294bca526023e642e3bb2347f1cc8a359adb7d841589b9ab03`

```dockerfile
```

-	Layers:
	-	`sha256:a8ef69a77f438781832ce47616b7148da57d14f091c1fec9feb463751c093ea5`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 404.0 KB (404031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2fba02a46b3246b86d84283002e93b1db9781ed73f6e4fd1a39872ab3ec045`  
		Last Modified: Wed, 09 Jul 2025 21:39:29 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:c0de4d9b7cb3cc102a1898b776ed13da48d2d2430fd36d3d31fa85d2b8063168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428696150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32567c70bcc575cb5a9becb968c3827c7105f70216a25437791c655b388c6421`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d889d0ac9e8307b4c08661c76a81b965d2fae37e45747b72e6db533b5839fae`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31c9e5502ce5d0c33f17beda02f924fb28b35cc10f9a654d68b926a7cd2ec1`  
		Last Modified: Wed, 09 Jul 2025 20:24:18 GMT  
		Size: 66.8 MB (66803159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1b42d769c4e371237b0e136c02ee1dadc6f4be783d8f155e0bbf3539834120`  
		Last Modified: Wed, 09 Jul 2025 20:23:59 GMT  
		Size: 354.4 MB (354430919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3442c9110a33c517d4e0101ea5109215ac2c2c71bc5cd9f78356bcdfb22b1abd`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 3.3 MB (3324515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a71c0204b0d1bf13b05909c050347f3efe0411d2e0bef3b368a0a3862ec599`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea2af4763b4915197f23de8faefc0746a03faf8c0739c92f6629b265023c541`  
		Last Modified: Wed, 09 Jul 2025 20:24:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:eace7156570ae94ddd2f731e651839fb2d13cf28d6d420a9cc581d0904339f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 KB (425128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b7a0054b786050dfec1c9121cd257a643d78b2b9d26f6dc9fb0628b6d082d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e2d7496f123b444f0592c3e9bb0464d51fc94578f1b45758734efb89abdcc`  
		Last Modified: Wed, 09 Jul 2025 21:39:33 GMT  
		Size: 403.3 KB (403278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d218135e2f832988120e3f396bbe2430c938d3ad018c30412106a7731962912`  
		Last Modified: Wed, 09 Jul 2025 21:39:34 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:544ac2748d04174603f1b0495570a18023172cdb1f7643ed32072760705e180a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:9df5e219b3d4c4a0ac1f78f1b3bf766c1e08079693f7a9c2f5bb28b323ab6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.7 MB (456685577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9e92189627f0afeb548a52c1af904bfaeb1cc1e338a2cd1d59527c48b1b0ff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43186e9339c95b15376ec7176560dc5f984c271d45fc58aa5e17cdbd7e356f3`  
		Last Modified: Wed, 09 Jul 2025 20:12:38 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ed63f42d7e4bfdb6c8de27647b88bef5a8204f83784d6f65ff2ac6d553203`  
		Last Modified: Wed, 09 Jul 2025 21:43:11 GMT  
		Size: 354.4 MB (354408299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9df7a05a912a709130646595d24b2b41b4d28ed7ce86f507dabe06ec9b6f4`  
		Last Modified: Wed, 09 Jul 2025 20:12:46 GMT  
		Size: 3.7 MB (3696548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aa3a1a07e7feccfde731e9a348ebf3316245e2c6ba232f7e884f6e3bdf3e60`  
		Last Modified: Wed, 09 Jul 2025 20:12:51 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0e248b6a6dab64e44af43a4ec6a3ebf5ee9bf46d8479dda4b6024ddaca99d`  
		Last Modified: Wed, 09 Jul 2025 20:12:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:ed61a9553c5252daea65b3c8b873a9bd35ce3436e0f9852c80f8e2f0d6cc5112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b9028fb88803fad5ebe58d92bf07402e26ed02fb21cfd1f545718ce77878dc`

```dockerfile
```

-	Layers:
	-	`sha256:59e4ce0186c67de921000a596f4481ebd72d5bbd449779a8efd511fc2f3b8f3d`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 3.9 MB (3940477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e72bd00bf85887bd191302144d7bbc2271affdf088d0c6fff221116a2c185a4`  
		Last Modified: Wed, 09 Jul 2025 21:39:22 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:f9630b80da904131922b859aab548b6fcf0995ccf3b70059d7410e9c3f90c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.3 MB (453311125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbff287b779e8c854a2b6a5a7b7448eccff97521e3c38705cd07ef764baf2818`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
WORKDIR /liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LIQUIBASE_VERSION=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_VERSION=0.2.10
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3
# Wed, 09 Jul 2025 14:57:56 GMT
ARG LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.version=4.33.0
# Wed, 09 Jul 2025 14:57:56 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 09 Jul 2025 14:57:56 GMT
# ARGS: LIQUIBASE_VERSION=4.33.0 LB_SHA256=689acfcdc97bad0d4c150d1efab9c851e251b398cb3d6326f75e8aafe40ed578 LPM_VERSION=0.2.10 LPM_SHA256=3a47a733e4bf203f9d09ff400ff34146aacac79bd2d192fa0cd2ba3e6312f8d3 LPM_SHA256_ARM=5f63a39b0774b372f64189f1e332c70098a51e55bc0f4c442a86753e8e8a0978
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 09 Jul 2025 14:57:56 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 09 Jul 2025 14:57:56 GMT
USER liquibase:liquibase
# Wed, 09 Jul 2025 14:57:56 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 09 Jul 2025 14:57:56 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b118eb757ac7763a739a3d3815afaec9105a13de997d34ceb84cfceeb9e5f`  
		Last Modified: Wed, 09 Jul 2025 22:34:28 GMT  
		Size: 354.4 MB (354408294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98e22c567a78264a81e4b97e0bafb823e0a61209b0be26ac466dec693deee72`  
		Last Modified: Wed, 09 Jul 2025 20:23:25 GMT  
		Size: 3.4 MB (3405518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a67f69f01f0a54c3d90c560a6c89f398bab30a34271991a37f201ec00809d`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e1cfcd0d2fc07d2831775770d6f477edf9b68ca2262af4fe115eeae47b7dfd`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:5f864465ca1aa18ce4599bc9c56bebf1d91c5dec43f09a60894733cb6c76ac5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130725a841759197bb89c19ee47a49ddd0a3f444953348d490560dd8fb789734`

```dockerfile
```

-	Layers:
	-	`sha256:bfe50c8247ec8851b09bbeea8f936fc215b9127967d729ffb28b9a3e264b853c`  
		Last Modified: Wed, 09 Jul 2025 21:39:27 GMT  
		Size: 3.9 MB (3940145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c1b89efaf7239bb3502ef47e1ea37ae66dc313b9c1eaa5a0396ddcb5db9880`  
		Last Modified: Wed, 09 Jul 2025 21:39:28 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json
