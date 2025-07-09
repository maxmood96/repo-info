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
