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
$ docker pull liquibase@sha256:63f66b3498638b43ffd2f7eab276997481b43c68b60a43a3de5a8c6c4a9eb8bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31` - linux; amd64

```console
$ docker pull liquibase@sha256:4b7f30314c9fb454a8741cfeedacb1c3025bf3edbd13b4822dc3e413ab022d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445891655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e6fedf8cef7c3ddc5fea15ad7444b72655fcb8804735deb2cc586cff00e90`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 08:00:24 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 07:44:36 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 07:29:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 07:22:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0b427604b344a4326dd3e56901dc73df14bff8ff4118574ab7cc86bff0c498`  
		Last Modified: Tue, 04 Feb 2025 10:09:59 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85097ffcef9c840716c6e07f52b663b9e5f5c1bd369700f7f26f4030871258fb`  
		Last Modified: Tue, 04 Feb 2025 08:11:58 GMT  
		Size: 349.9 MB (349941634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e6f7a81fc4bf71c4893877257e34125521098687b6fded55b69a0192641fd`  
		Last Modified: Tue, 04 Feb 2025 12:03:26 GMT  
		Size: 3.3 MB (3318841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae49f7e1a21c0655bc42e85da402aa6aad2f282e08e972355a8cee56062632`  
		Last Modified: Tue, 04 Feb 2025 07:40:35 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78005c7d5bb63ede2a8179d0e63d8b4fd4c8d41bfbe3fd83854e9a48e06940f`  
		Last Modified: Tue, 04 Feb 2025 15:40:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:f6f6ff72ffbfe813c030489fa1958c8d0d9338103ec35b7002e07d46c0d8b8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e95b0127da62e0947ab21845259ec225ccee1161f5c29ef78ac2d835c5c3393`

```dockerfile
```

-	Layers:
	-	`sha256:d604468d32972dd5a27ac6fa50d63391ebbc6f350434cf8090e1b5c1e6632e1e`  
		Last Modified: Fri, 07 Feb 2025 19:11:15 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bc10c9eef8e444be0b79a07db2c54287551e3bd230dd8b57801464956f74a`  
		Last Modified: Sat, 15 Feb 2025 07:24:54 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:81dc21bd1d0fdf07c4f93aeaa7d63726ca9f7685c2cdc56ea9249925b4ccf007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442896804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366e6979e78a33ca8736190d020f70f40fbd8ec01934f1045eef3ae76f570f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 11:06:23 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 13:23:17 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 13:40:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 13:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d030d8c5c3fea15a4d55ee39e670bb061a369847ba083aa52e87794eb17fd7d`  
		Last Modified: Wed, 05 Feb 2025 03:50:48 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dea1487fe6cb995ebbc2405946f0fbab81df0a75848ab2be443eb8ff7ac9d0`  
		Last Modified: Wed, 05 Feb 2025 03:51:01 GMT  
		Size: 349.9 MB (349941635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f0c67a6bedc8ff79234ecb3b66edb44ec66e0ad12db80fcd4b26929096bc4`  
		Last Modified: Wed, 05 Feb 2025 07:54:21 GMT  
		Size: 3.1 MB (3073342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55feb9bd2a239ad4b38befee57993da25dfd2c22651e8948169210e3dd4444b3`  
		Last Modified: Wed, 05 Feb 2025 11:18:11 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd50796692a868f9466b0be91f08d76f71961bde8f52c03807eda2c90f4160b1`  
		Last Modified: Wed, 05 Feb 2025 07:54:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:4efa71aa82bcaceabf5a93d414f0fe29ea56f2e29bfcc1edde5f78ac264132bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3598d9d70f2cffc1f3175784f1c49a59b06fdabf83dbc24cb33be7f08a7c10`

```dockerfile
```

-	Layers:
	-	`sha256:7ad72d80b62324ddd60bb0d510e1b325518460b1589e1e2bd7824624ee72db7e`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 3.8 MB (3751003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1943e37df7a8ac5db4527d0c66588bea44d4a06359f745f9740e09f8000f3b2`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 24.3 KB (24329 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31-alpine`

```console
$ docker pull liquibase@sha256:b80db5940f1ecc9cb3a95117de32be3127adb378f344d57661f186f40a6d5745
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:6cf0664468d650726efe6b98323537e418891a577d9a6f953505c911549d7fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419623328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca22b5b5239bf48111838ad4215dcaad5d1e99bad31ebbfcd1f04096cb2eb62`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8559cb8dbe523927995a9e51c525ad9efec9808a6d7f71fd57d2f87c17fb987`  
		Last Modified: Sat, 15 Feb 2025 03:05:53 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e103e3a24bd99280cb261a8ed343c5470e704f6bf6e6adf4c00658b5c7be85`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 62.8 MB (62774578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f152bf46cd2b13ea0fdae5671c8467692d20111b1e2c6b245a9fa72793b538`  
		Last Modified: Sat, 15 Feb 2025 03:06:06 GMT  
		Size: 350.0 MB (349963620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbabe51a2d3c2bd2266914dcf852d468e8f69b7d097cca729f5e903c6bec60`  
		Last Modified: Sat, 15 Feb 2025 03:05:54 GMT  
		Size: 3.2 MB (3241273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751d88c7cb7a193f1f7134ee7345fa8e1f07ac49b28d5064870b37587fabc46`  
		Last Modified: Sat, 15 Feb 2025 03:05:55 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c5a8278b7b36763a72df3e8aad861d909f7d703c7a8d4de9211e65a7211a64`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:1181f24b7d3fd1ef5f9d93a7120951e974d4be8662b52661bb915996800b39d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3338d8455e983ed6bb8e86ca633fb3581868c22dee1926cdb54373264aa655b`

```dockerfile
```

-	Layers:
	-	`sha256:b6d55809ebfcdc0d6d5a4f6b1d5b6efa170a5c6e68d536285a4951d779095c72`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 385.1 KB (385084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56359eb57b436c912d967fb591f3baaa3c625fa4c6fbfb67ce9e7e7f182c015d`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 21.2 KB (21248 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:3a11726a97db2e8cee9f0a5b33471c7fb4dbbefcb7239b8259a4a574126ceb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418922540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5e90e120487d2375cc76e6d9fe3bb7c0309006ab336d40c26be8e57355fc9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d80fac97bd8e989f5679486996280eb8838fe67583da9b3c5f8bbad00ca0b3`  
		Last Modified: Sat, 15 Feb 2025 05:03:27 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f90999cbb6c5d850cf2b2349bfc316f2389ec487c7f90e511751acc8822080`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 62.0 MB (61972256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64ec182147456b4f252cfbe511f0982d0e57d451a3a8be347f7e6b0312f787c`  
		Last Modified: Sat, 15 Feb 2025 05:03:42 GMT  
		Size: 350.0 MB (349963688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cead277b8aae8282fe3808d812ef56576ee5a06bbe4407ff7763c96ab0ff7410`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 3.0 MB (2991957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b9d36e2dd90cfc120347a98d2e989345481ffdba94c16362913cc697924762`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819c2e09f0e19b0333f9228074c7fd4f295d19cbb2b6162b8cd51980de9d4729`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bacb1f617573aa82726b9c055c850932929b64e05b73c617966e76d942efb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbb8f225f77abb0b11ecc7fb76cfa8d1af4d72ff07866557125a8d8a1b61544`

```dockerfile
```

-	Layers:
	-	`sha256:698a1c9baa429105dfafea5b0b7ef95167a1f9bd0b4fc088c31ab17d34e3447f`  
		Last Modified: Sat, 15 Feb 2025 01:39:19 GMT  
		Size: 384.3 KB (384331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51539ea61c548f18c49e093cbe5300c9a8df41e3b1c527cf2c6c7e4c9dfda341`  
		Last Modified: Sat, 15 Feb 2025 01:39:20 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0`

```console
$ docker pull liquibase@sha256:63f66b3498638b43ffd2f7eab276997481b43c68b60a43a3de5a8c6c4a9eb8bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0` - linux; amd64

```console
$ docker pull liquibase@sha256:4b7f30314c9fb454a8741cfeedacb1c3025bf3edbd13b4822dc3e413ab022d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445891655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e6fedf8cef7c3ddc5fea15ad7444b72655fcb8804735deb2cc586cff00e90`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 08:00:24 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 07:44:36 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 07:29:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 07:22:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0b427604b344a4326dd3e56901dc73df14bff8ff4118574ab7cc86bff0c498`  
		Last Modified: Tue, 04 Feb 2025 10:09:59 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85097ffcef9c840716c6e07f52b663b9e5f5c1bd369700f7f26f4030871258fb`  
		Last Modified: Tue, 04 Feb 2025 08:11:58 GMT  
		Size: 349.9 MB (349941634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e6f7a81fc4bf71c4893877257e34125521098687b6fded55b69a0192641fd`  
		Last Modified: Tue, 04 Feb 2025 12:03:26 GMT  
		Size: 3.3 MB (3318841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae49f7e1a21c0655bc42e85da402aa6aad2f282e08e972355a8cee56062632`  
		Last Modified: Tue, 04 Feb 2025 07:40:35 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78005c7d5bb63ede2a8179d0e63d8b4fd4c8d41bfbe3fd83854e9a48e06940f`  
		Last Modified: Tue, 04 Feb 2025 15:40:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:f6f6ff72ffbfe813c030489fa1958c8d0d9338103ec35b7002e07d46c0d8b8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e95b0127da62e0947ab21845259ec225ccee1161f5c29ef78ac2d835c5c3393`

```dockerfile
```

-	Layers:
	-	`sha256:d604468d32972dd5a27ac6fa50d63391ebbc6f350434cf8090e1b5c1e6632e1e`  
		Last Modified: Fri, 07 Feb 2025 19:11:15 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bc10c9eef8e444be0b79a07db2c54287551e3bd230dd8b57801464956f74a`  
		Last Modified: Sat, 15 Feb 2025 07:24:54 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:81dc21bd1d0fdf07c4f93aeaa7d63726ca9f7685c2cdc56ea9249925b4ccf007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442896804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366e6979e78a33ca8736190d020f70f40fbd8ec01934f1045eef3ae76f570f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 11:06:23 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 13:23:17 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 13:40:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 13:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d030d8c5c3fea15a4d55ee39e670bb061a369847ba083aa52e87794eb17fd7d`  
		Last Modified: Wed, 05 Feb 2025 03:50:48 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dea1487fe6cb995ebbc2405946f0fbab81df0a75848ab2be443eb8ff7ac9d0`  
		Last Modified: Wed, 05 Feb 2025 03:51:01 GMT  
		Size: 349.9 MB (349941635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f0c67a6bedc8ff79234ecb3b66edb44ec66e0ad12db80fcd4b26929096bc4`  
		Last Modified: Wed, 05 Feb 2025 07:54:21 GMT  
		Size: 3.1 MB (3073342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55feb9bd2a239ad4b38befee57993da25dfd2c22651e8948169210e3dd4444b3`  
		Last Modified: Wed, 05 Feb 2025 11:18:11 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd50796692a868f9466b0be91f08d76f71961bde8f52c03807eda2c90f4160b1`  
		Last Modified: Wed, 05 Feb 2025 07:54:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:4efa71aa82bcaceabf5a93d414f0fe29ea56f2e29bfcc1edde5f78ac264132bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3598d9d70f2cffc1f3175784f1c49a59b06fdabf83dbc24cb33be7f08a7c10`

```dockerfile
```

-	Layers:
	-	`sha256:7ad72d80b62324ddd60bb0d510e1b325518460b1589e1e2bd7824624ee72db7e`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 3.8 MB (3751003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1943e37df7a8ac5db4527d0c66588bea44d4a06359f745f9740e09f8000f3b2`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 24.3 KB (24329 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0-alpine`

```console
$ docker pull liquibase@sha256:b80db5940f1ecc9cb3a95117de32be3127adb378f344d57661f186f40a6d5745
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:6cf0664468d650726efe6b98323537e418891a577d9a6f953505c911549d7fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419623328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca22b5b5239bf48111838ad4215dcaad5d1e99bad31ebbfcd1f04096cb2eb62`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8559cb8dbe523927995a9e51c525ad9efec9808a6d7f71fd57d2f87c17fb987`  
		Last Modified: Sat, 15 Feb 2025 03:05:53 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e103e3a24bd99280cb261a8ed343c5470e704f6bf6e6adf4c00658b5c7be85`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 62.8 MB (62774578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f152bf46cd2b13ea0fdae5671c8467692d20111b1e2c6b245a9fa72793b538`  
		Last Modified: Sat, 15 Feb 2025 03:06:06 GMT  
		Size: 350.0 MB (349963620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbabe51a2d3c2bd2266914dcf852d468e8f69b7d097cca729f5e903c6bec60`  
		Last Modified: Sat, 15 Feb 2025 03:05:54 GMT  
		Size: 3.2 MB (3241273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751d88c7cb7a193f1f7134ee7345fa8e1f07ac49b28d5064870b37587fabc46`  
		Last Modified: Sat, 15 Feb 2025 03:05:55 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c5a8278b7b36763a72df3e8aad861d909f7d703c7a8d4de9211e65a7211a64`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:1181f24b7d3fd1ef5f9d93a7120951e974d4be8662b52661bb915996800b39d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3338d8455e983ed6bb8e86ca633fb3581868c22dee1926cdb54373264aa655b`

```dockerfile
```

-	Layers:
	-	`sha256:b6d55809ebfcdc0d6d5a4f6b1d5b6efa170a5c6e68d536285a4951d779095c72`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 385.1 KB (385084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56359eb57b436c912d967fb591f3baaa3c625fa4c6fbfb67ce9e7e7f182c015d`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 21.2 KB (21248 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:3a11726a97db2e8cee9f0a5b33471c7fb4dbbefcb7239b8259a4a574126ceb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418922540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5e90e120487d2375cc76e6d9fe3bb7c0309006ab336d40c26be8e57355fc9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d80fac97bd8e989f5679486996280eb8838fe67583da9b3c5f8bbad00ca0b3`  
		Last Modified: Sat, 15 Feb 2025 05:03:27 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f90999cbb6c5d850cf2b2349bfc316f2389ec487c7f90e511751acc8822080`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 62.0 MB (61972256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64ec182147456b4f252cfbe511f0982d0e57d451a3a8be347f7e6b0312f787c`  
		Last Modified: Sat, 15 Feb 2025 05:03:42 GMT  
		Size: 350.0 MB (349963688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cead277b8aae8282fe3808d812ef56576ee5a06bbe4407ff7763c96ab0ff7410`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 3.0 MB (2991957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b9d36e2dd90cfc120347a98d2e989345481ffdba94c16362913cc697924762`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819c2e09f0e19b0333f9228074c7fd4f295d19cbb2b6162b8cd51980de9d4729`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bacb1f617573aa82726b9c055c850932929b64e05b73c617966e76d942efb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbb8f225f77abb0b11ecc7fb76cfa8d1af4d72ff07866557125a8d8a1b61544`

```dockerfile
```

-	Layers:
	-	`sha256:698a1c9baa429105dfafea5b0b7ef95167a1f9bd0b4fc088c31ab17d34e3447f`  
		Last Modified: Sat, 15 Feb 2025 01:39:19 GMT  
		Size: 384.3 KB (384331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51539ea61c548f18c49e093cbe5300c9a8df41e3b1c527cf2c6c7e4c9dfda341`  
		Last Modified: Sat, 15 Feb 2025 01:39:20 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:b80db5940f1ecc9cb3a95117de32be3127adb378f344d57661f186f40a6d5745
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:6cf0664468d650726efe6b98323537e418891a577d9a6f953505c911549d7fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419623328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca22b5b5239bf48111838ad4215dcaad5d1e99bad31ebbfcd1f04096cb2eb62`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8559cb8dbe523927995a9e51c525ad9efec9808a6d7f71fd57d2f87c17fb987`  
		Last Modified: Sat, 15 Feb 2025 03:05:53 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e103e3a24bd99280cb261a8ed343c5470e704f6bf6e6adf4c00658b5c7be85`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 62.8 MB (62774578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f152bf46cd2b13ea0fdae5671c8467692d20111b1e2c6b245a9fa72793b538`  
		Last Modified: Sat, 15 Feb 2025 03:06:06 GMT  
		Size: 350.0 MB (349963620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbabe51a2d3c2bd2266914dcf852d468e8f69b7d097cca729f5e903c6bec60`  
		Last Modified: Sat, 15 Feb 2025 03:05:54 GMT  
		Size: 3.2 MB (3241273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751d88c7cb7a193f1f7134ee7345fa8e1f07ac49b28d5064870b37587fabc46`  
		Last Modified: Sat, 15 Feb 2025 03:05:55 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c5a8278b7b36763a72df3e8aad861d909f7d703c7a8d4de9211e65a7211a64`  
		Last Modified: Sat, 15 Feb 2025 03:05:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:1181f24b7d3fd1ef5f9d93a7120951e974d4be8662b52661bb915996800b39d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3338d8455e983ed6bb8e86ca633fb3581868c22dee1926cdb54373264aa655b`

```dockerfile
```

-	Layers:
	-	`sha256:b6d55809ebfcdc0d6d5a4f6b1d5b6efa170a5c6e68d536285a4951d779095c72`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 385.1 KB (385084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56359eb57b436c912d967fb591f3baaa3c625fa4c6fbfb67ce9e7e7f182c015d`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 21.2 KB (21248 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:3a11726a97db2e8cee9f0a5b33471c7fb4dbbefcb7239b8259a4a574126ceb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418922540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5e90e120487d2375cc76e6d9fe3bb7c0309006ab336d40c26be8e57355fc9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d80fac97bd8e989f5679486996280eb8838fe67583da9b3c5f8bbad00ca0b3`  
		Last Modified: Sat, 15 Feb 2025 05:03:27 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f90999cbb6c5d850cf2b2349bfc316f2389ec487c7f90e511751acc8822080`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 62.0 MB (61972256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64ec182147456b4f252cfbe511f0982d0e57d451a3a8be347f7e6b0312f787c`  
		Last Modified: Sat, 15 Feb 2025 05:03:42 GMT  
		Size: 350.0 MB (349963688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cead277b8aae8282fe3808d812ef56576ee5a06bbe4407ff7763c96ab0ff7410`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 3.0 MB (2991957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b9d36e2dd90cfc120347a98d2e989345481ffdba94c16362913cc697924762`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819c2e09f0e19b0333f9228074c7fd4f295d19cbb2b6162b8cd51980de9d4729`  
		Last Modified: Sat, 15 Feb 2025 05:03:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bacb1f617573aa82726b9c055c850932929b64e05b73c617966e76d942efb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbb8f225f77abb0b11ecc7fb76cfa8d1af4d72ff07866557125a8d8a1b61544`

```dockerfile
```

-	Layers:
	-	`sha256:698a1c9baa429105dfafea5b0b7ef95167a1f9bd0b4fc088c31ab17d34e3447f`  
		Last Modified: Sat, 15 Feb 2025 01:39:19 GMT  
		Size: 384.3 KB (384331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51539ea61c548f18c49e093cbe5300c9a8df41e3b1c527cf2c6c7e4c9dfda341`  
		Last Modified: Sat, 15 Feb 2025 01:39:20 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:63f66b3498638b43ffd2f7eab276997481b43c68b60a43a3de5a8c6c4a9eb8bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:4b7f30314c9fb454a8741cfeedacb1c3025bf3edbd13b4822dc3e413ab022d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445891655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e6fedf8cef7c3ddc5fea15ad7444b72655fcb8804735deb2cc586cff00e90`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 08:00:24 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 07:44:36 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 07:29:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 07:22:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0b427604b344a4326dd3e56901dc73df14bff8ff4118574ab7cc86bff0c498`  
		Last Modified: Tue, 04 Feb 2025 10:09:59 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85097ffcef9c840716c6e07f52b663b9e5f5c1bd369700f7f26f4030871258fb`  
		Last Modified: Tue, 04 Feb 2025 08:11:58 GMT  
		Size: 349.9 MB (349941634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e6f7a81fc4bf71c4893877257e34125521098687b6fded55b69a0192641fd`  
		Last Modified: Tue, 04 Feb 2025 12:03:26 GMT  
		Size: 3.3 MB (3318841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae49f7e1a21c0655bc42e85da402aa6aad2f282e08e972355a8cee56062632`  
		Last Modified: Tue, 04 Feb 2025 07:40:35 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78005c7d5bb63ede2a8179d0e63d8b4fd4c8d41bfbe3fd83854e9a48e06940f`  
		Last Modified: Tue, 04 Feb 2025 15:40:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:f6f6ff72ffbfe813c030489fa1958c8d0d9338103ec35b7002e07d46c0d8b8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e95b0127da62e0947ab21845259ec225ccee1161f5c29ef78ac2d835c5c3393`

```dockerfile
```

-	Layers:
	-	`sha256:d604468d32972dd5a27ac6fa50d63391ebbc6f350434cf8090e1b5c1e6632e1e`  
		Last Modified: Fri, 07 Feb 2025 19:11:15 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bc10c9eef8e444be0b79a07db2c54287551e3bd230dd8b57801464956f74a`  
		Last Modified: Sat, 15 Feb 2025 07:24:54 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:81dc21bd1d0fdf07c4f93aeaa7d63726ca9f7685c2cdc56ea9249925b4ccf007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442896804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366e6979e78a33ca8736190d020f70f40fbd8ec01934f1045eef3ae76f570f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 24 Jan 2025 17:25:12 GMT
ARG RELEASE
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 17:25:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 17:25:12 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 11:06:23 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 13:23:17 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 13:40:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 13:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d030d8c5c3fea15a4d55ee39e670bb061a369847ba083aa52e87794eb17fd7d`  
		Last Modified: Wed, 05 Feb 2025 03:50:48 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dea1487fe6cb995ebbc2405946f0fbab81df0a75848ab2be443eb8ff7ac9d0`  
		Last Modified: Wed, 05 Feb 2025 03:51:01 GMT  
		Size: 349.9 MB (349941635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f0c67a6bedc8ff79234ecb3b66edb44ec66e0ad12db80fcd4b26929096bc4`  
		Last Modified: Wed, 05 Feb 2025 07:54:21 GMT  
		Size: 3.1 MB (3073342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55feb9bd2a239ad4b38befee57993da25dfd2c22651e8948169210e3dd4444b3`  
		Last Modified: Wed, 05 Feb 2025 11:18:11 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd50796692a868f9466b0be91f08d76f71961bde8f52c03807eda2c90f4160b1`  
		Last Modified: Wed, 05 Feb 2025 07:54:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:4efa71aa82bcaceabf5a93d414f0fe29ea56f2e29bfcc1edde5f78ac264132bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3598d9d70f2cffc1f3175784f1c49a59b06fdabf83dbc24cb33be7f08a7c10`

```dockerfile
```

-	Layers:
	-	`sha256:7ad72d80b62324ddd60bb0d510e1b325518460b1589e1e2bd7824624ee72db7e`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 3.8 MB (3751003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1943e37df7a8ac5db4527d0c66588bea44d4a06359f745f9740e09f8000f3b2`  
		Last Modified: Fri, 07 Feb 2025 19:12:02 GMT  
		Size: 24.3 KB (24329 bytes)  
		MIME: application/vnd.in-toto+json
