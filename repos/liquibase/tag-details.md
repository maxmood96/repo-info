<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.31`](#liquibase431)
-	[`liquibase:4.31-alpine`](#liquibase431-alpine)
-	[`liquibase:4.31.0`](#liquibase4310)
-	[`liquibase:4.31.0-alpine`](#liquibase4310-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.31`

```console
$ docker pull liquibase@sha256:b101950c0b3977b53cbb97e636f5d1169f75d4f1045476d4ec4d3547c1a5ee7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31` - linux; amd64

```console
$ docker pull liquibase@sha256:8ee6063a01e96e822ec6ebc435fe056cd91e8f5324f6b42277eae289fb69bfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6993fb466cf46d2df5b9f7e9b3d3992f06ccdcdd52406ae0a2281459167091d3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19444cade5a1e0e6a400abf320ea486f245a7dff698e81c60d801455dd152bf`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd80e0f85681d8c69c6e6ee118f82d5b6963d9c49393b9e584316f35caddf4`  
		Last Modified: Fri, 17 Jan 2025 00:28:38 GMT  
		Size: 349.9 MB (349941633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde9a337ed925d167f2a472db0013c8738a22c563519238f8fa3cd43806debc6`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 3.3 MB (3318522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba730807991f505e04468f1140789d6eb69a843e41b6d4f400509d74a50a6d0`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa18434745d589672c31dbe5b7aa240e25be57b38345f78baaa1fedafaacbf8`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:e40b58871740231e7cf24dfee8dccc71074d132aa124234f0cc1b8e3e9a808ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41351914e1aaa793b4ae5a279597191844a4957ec00d76f1c59c8b977cc4e802`

```dockerfile
```

-	Layers:
	-	`sha256:86a65558f69beff8c859d9ae56b2c037391612d03f997591d7dbed5759934e0d`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2aa312456a1b1421a1757cb2b1252fe8fd12b0d2fa9379ee06942a6d4bd8645`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 24.2 KB (24184 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:a9aaff5e30c6927e5955a9d0697c46aba89afbed644fbf8b73300a958e9ac816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442871042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0c278594d41ef0091109b5d52fa42ed17fa50f89d084a8e6b40d15a94b4592`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f330b4eaadf8f00b278574f44f4b243e87769f52d22401d047baf641f16aa02`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e692d7ed124b9f99b4d5ba5fe6931baaddc1ea53b251a55f68b26dd3b7049d`  
		Last Modified: Fri, 17 Jan 2025 00:28:50 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89fe11f64e2c6b74f5ee6bd4a3c62e39c86fcc47746390e08f361d4743ee5b`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.1 MB (3073128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca446ad7476ed3b071b2aa73bb438fffededd5cefb6f9c7f9e07ec8f390d5d4e`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a8f9d62966dc47150bb4949011736e4c265f6cb9ee4d953a11a6da8814d9b2`  
		Last Modified: Fri, 17 Jan 2025 00:28:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:196e1d3e004e27f902b0bd074626f8d28d0b857be906b6079aa15a807a97ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6534ea806c67bdbc799e0616242dc66ea9c01a60a213fcdded40805e70ef953a`

```dockerfile
```

-	Layers:
	-	`sha256:bf9a4b2ae73a96174b12a844c31fa07d10044f97aa7f45c949b9c75b2e689516`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46e9c95a8cf3d929231f07234926d019d26ae22e8cfe0895e0fde4aeef36b6a`  
		Last Modified: Fri, 17 Jan 2025 00:28:42 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31-alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0`

```console
$ docker pull liquibase@sha256:b101950c0b3977b53cbb97e636f5d1169f75d4f1045476d4ec4d3547c1a5ee7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0` - linux; amd64

```console
$ docker pull liquibase@sha256:8ee6063a01e96e822ec6ebc435fe056cd91e8f5324f6b42277eae289fb69bfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6993fb466cf46d2df5b9f7e9b3d3992f06ccdcdd52406ae0a2281459167091d3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19444cade5a1e0e6a400abf320ea486f245a7dff698e81c60d801455dd152bf`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd80e0f85681d8c69c6e6ee118f82d5b6963d9c49393b9e584316f35caddf4`  
		Last Modified: Fri, 17 Jan 2025 00:28:38 GMT  
		Size: 349.9 MB (349941633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde9a337ed925d167f2a472db0013c8738a22c563519238f8fa3cd43806debc6`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 3.3 MB (3318522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba730807991f505e04468f1140789d6eb69a843e41b6d4f400509d74a50a6d0`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa18434745d589672c31dbe5b7aa240e25be57b38345f78baaa1fedafaacbf8`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:e40b58871740231e7cf24dfee8dccc71074d132aa124234f0cc1b8e3e9a808ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41351914e1aaa793b4ae5a279597191844a4957ec00d76f1c59c8b977cc4e802`

```dockerfile
```

-	Layers:
	-	`sha256:86a65558f69beff8c859d9ae56b2c037391612d03f997591d7dbed5759934e0d`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2aa312456a1b1421a1757cb2b1252fe8fd12b0d2fa9379ee06942a6d4bd8645`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 24.2 KB (24184 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:a9aaff5e30c6927e5955a9d0697c46aba89afbed644fbf8b73300a958e9ac816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442871042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0c278594d41ef0091109b5d52fa42ed17fa50f89d084a8e6b40d15a94b4592`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f330b4eaadf8f00b278574f44f4b243e87769f52d22401d047baf641f16aa02`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e692d7ed124b9f99b4d5ba5fe6931baaddc1ea53b251a55f68b26dd3b7049d`  
		Last Modified: Fri, 17 Jan 2025 00:28:50 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89fe11f64e2c6b74f5ee6bd4a3c62e39c86fcc47746390e08f361d4743ee5b`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.1 MB (3073128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca446ad7476ed3b071b2aa73bb438fffededd5cefb6f9c7f9e07ec8f390d5d4e`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a8f9d62966dc47150bb4949011736e4c265f6cb9ee4d953a11a6da8814d9b2`  
		Last Modified: Fri, 17 Jan 2025 00:28:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:196e1d3e004e27f902b0bd074626f8d28d0b857be906b6079aa15a807a97ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6534ea806c67bdbc799e0616242dc66ea9c01a60a213fcdded40805e70ef953a`

```dockerfile
```

-	Layers:
	-	`sha256:bf9a4b2ae73a96174b12a844c31fa07d10044f97aa7f45c949b9c75b2e689516`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46e9c95a8cf3d929231f07234926d019d26ae22e8cfe0895e0fde4aeef36b6a`  
		Last Modified: Fri, 17 Jan 2025 00:28:42 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0-alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:b101950c0b3977b53cbb97e636f5d1169f75d4f1045476d4ec4d3547c1a5ee7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:8ee6063a01e96e822ec6ebc435fe056cd91e8f5324f6b42277eae289fb69bfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445885495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6993fb466cf46d2df5b9f7e9b3d3992f06ccdcdd52406ae0a2281459167091d3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19444cade5a1e0e6a400abf320ea486f245a7dff698e81c60d801455dd152bf`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd80e0f85681d8c69c6e6ee118f82d5b6963d9c49393b9e584316f35caddf4`  
		Last Modified: Fri, 17 Jan 2025 00:28:38 GMT  
		Size: 349.9 MB (349941633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde9a337ed925d167f2a472db0013c8738a22c563519238f8fa3cd43806debc6`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 3.3 MB (3318522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba730807991f505e04468f1140789d6eb69a843e41b6d4f400509d74a50a6d0`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa18434745d589672c31dbe5b7aa240e25be57b38345f78baaa1fedafaacbf8`  
		Last Modified: Fri, 17 Jan 2025 00:28:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:e40b58871740231e7cf24dfee8dccc71074d132aa124234f0cc1b8e3e9a808ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41351914e1aaa793b4ae5a279597191844a4957ec00d76f1c59c8b977cc4e802`

```dockerfile
```

-	Layers:
	-	`sha256:86a65558f69beff8c859d9ae56b2c037391612d03f997591d7dbed5759934e0d`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2aa312456a1b1421a1757cb2b1252fe8fd12b0d2fa9379ee06942a6d4bd8645`  
		Last Modified: Fri, 17 Jan 2025 00:28:32 GMT  
		Size: 24.2 KB (24184 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:a9aaff5e30c6927e5955a9d0697c46aba89afbed644fbf8b73300a958e9ac816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442871042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0c278594d41ef0091109b5d52fa42ed17fa50f89d084a8e6b40d15a94b4592`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f330b4eaadf8f00b278574f44f4b243e87769f52d22401d047baf641f16aa02`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e692d7ed124b9f99b4d5ba5fe6931baaddc1ea53b251a55f68b26dd3b7049d`  
		Last Modified: Fri, 17 Jan 2025 00:28:50 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89fe11f64e2c6b74f5ee6bd4a3c62e39c86fcc47746390e08f361d4743ee5b`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.1 MB (3073128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca446ad7476ed3b071b2aa73bb438fffededd5cefb6f9c7f9e07ec8f390d5d4e`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a8f9d62966dc47150bb4949011736e4c265f6cb9ee4d953a11a6da8814d9b2`  
		Last Modified: Fri, 17 Jan 2025 00:28:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:196e1d3e004e27f902b0bd074626f8d28d0b857be906b6079aa15a807a97ef40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6534ea806c67bdbc799e0616242dc66ea9c01a60a213fcdded40805e70ef953a`

```dockerfile
```

-	Layers:
	-	`sha256:bf9a4b2ae73a96174b12a844c31fa07d10044f97aa7f45c949b9c75b2e689516`  
		Last Modified: Fri, 17 Jan 2025 00:28:43 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46e9c95a8cf3d929231f07234926d019d26ae22e8cfe0895e0fde4aeef36b6a`  
		Last Modified: Fri, 17 Jan 2025 00:28:42 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json
