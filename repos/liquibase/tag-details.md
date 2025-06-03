<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.32`](#liquibase432)
-	[`liquibase:4.32-alpine`](#liquibase432-alpine)
-	[`liquibase:4.32.0`](#liquibase4320)
-	[`liquibase:4.32.0-alpine`](#liquibase4320-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.32`

```console
$ docker pull liquibase@sha256:b1c9e4082ab9039aaf181425d1399551b74ce4078c5e2b22397407485908d3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32` - linux; amd64

```console
$ docker pull liquibase@sha256:4902301eaa3b8e674065ee545f7d20b8052bce6419b0d561fbc5d77710d2d50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c309eb793b0627c106c8c47de95b23351a40cc97cd34046f5f5f5bc2500ffc5`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec65b0a960d876d89c4e336597de256371b2c39f8a70053a74a88f6432aa78d`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 16.1 MB (16146403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6ebde483e5e55714fbed9a5d73ee34bcf3bd2098862ddbe020fc48fb9bd34`  
		Last Modified: Tue, 03 Jun 2025 04:16:10 GMT  
		Size: 52.9 MB (52891235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d914152eed4806d3ec7eb97d67feea997fc20d7ba8956d38359c128ef1f265`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b977c46889de2487c980399cba0fa6c04d3bd8fde596eb59cccf75b06684ea8`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534e2236d6ca10f8ab1fe5e66351b1c4fd4d229b732cd27bc6ae05207a402a0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63e4b5b057d247baaeb40e2710c7b3b743f633b365a30f0d26c53775f25b85`  
		Last Modified: Tue, 03 Jun 2025 05:13:38 GMT  
		Size: 353.6 MB (353635002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c858b74cb07bc3d83a5cc3275ff29c6701a18c7e7ecf8e05db65fc4d8aee5`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.5 MB (3514817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22df6c14824078b1524f367c45b7aa3a03e3cd21d08baf49e9582959e8c44f0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595edb5fd896452773189f92924ee8e6d4b1f7f6fa27b321145eff165e5c292`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:a9c63ebd13f89a339b8585a605e145b799afdae1ad93cbb411c3d6be0c9af2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359bd50351b5d0b79a26efa3a7dee2f2d6abc6a43eacfd3169dc3602a97fd0b0`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a9680c7f2368fdf5d65a77c22f2e6d2e8c42b9fad6bb42de45a90d79393ee`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.8 MB (3797989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c8e5075a6d85f3eebfb96cc35eb9f5092e5e4e0ac4b05c89b06e6dd92d15ef`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:91995ece7abb19a84d48cfb9ec494dcf10e8721495e8824fdfd82f721c6a4bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452384855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f9b42aa254582181786ea3a1dc78dd813564878dde7736dd65dd07a196296`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 04:36:48 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7fe9a9405de0a49e978e4e5c9f2e884543fdcf565c75e81408bba0e7f2148`  
		Last Modified: Tue, 03 Jun 2025 04:44:18 GMT  
		Size: 52.1 MB (52070735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edbdd8db42ec6c19f89c8dec4f8cb06ed32fa7627bf526b1b1ad0b37e2c8574`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68aeaebbf0603c0f28825078e2e4b8447ed3428a86335fa8606fcc0526ed9c5`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f56713fb3b0e3391646969776f24d722e09f71248381fac93342d065f53e7b`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fafbc7aee75d684bf66dee390a1550906b0b03d02fc52aea8bc1c1c09899ea`  
		Last Modified: Tue, 03 Jun 2025 07:46:23 GMT  
		Size: 353.6 MB (353635048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf75d686d811dc75815ad81e0ce70af8253eb7d1841fe14510f836633713a5c`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.3 MB (3256232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c922eb8a70edea13fb36e6dee6556a291eea92646c86729a7060f7ba3ef7e`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 467.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3260b5d7de87a2b28d0f825de1e5cd6f509bf9a3edbb9891ff5f5f3dd54f7`  
		Last Modified: Tue, 03 Jun 2025 07:46:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:9193f446c498fc928523191e3a14140f9f948d34baeda22b04694e24769f8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f683e3a26764e8c7d0cb8c697543f3e1a5308fda83eb96700d678c87bff15`

```dockerfile
```

-	Layers:
	-	`sha256:37497612c17d717e24b9829385961ad356b7c9bdfd1fb218068302135b470544`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.8 MB (3797657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109126a455a73b649e16502d1d3e465bbbb437f87d3a8c7bfd01faa8f6c3b462`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32-alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Fri, 23 May 2025 17:08:03 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Fri, 23 May 2025 17:09:28 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32.0`

```console
$ docker pull liquibase@sha256:b1c9e4082ab9039aaf181425d1399551b74ce4078c5e2b22397407485908d3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32.0` - linux; amd64

```console
$ docker pull liquibase@sha256:4902301eaa3b8e674065ee545f7d20b8052bce6419b0d561fbc5d77710d2d50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c309eb793b0627c106c8c47de95b23351a40cc97cd34046f5f5f5bc2500ffc5`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec65b0a960d876d89c4e336597de256371b2c39f8a70053a74a88f6432aa78d`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 16.1 MB (16146403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6ebde483e5e55714fbed9a5d73ee34bcf3bd2098862ddbe020fc48fb9bd34`  
		Last Modified: Tue, 03 Jun 2025 04:16:10 GMT  
		Size: 52.9 MB (52891235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d914152eed4806d3ec7eb97d67feea997fc20d7ba8956d38359c128ef1f265`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b977c46889de2487c980399cba0fa6c04d3bd8fde596eb59cccf75b06684ea8`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534e2236d6ca10f8ab1fe5e66351b1c4fd4d229b732cd27bc6ae05207a402a0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63e4b5b057d247baaeb40e2710c7b3b743f633b365a30f0d26c53775f25b85`  
		Last Modified: Tue, 03 Jun 2025 05:13:38 GMT  
		Size: 353.6 MB (353635002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c858b74cb07bc3d83a5cc3275ff29c6701a18c7e7ecf8e05db65fc4d8aee5`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.5 MB (3514817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22df6c14824078b1524f367c45b7aa3a03e3cd21d08baf49e9582959e8c44f0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595edb5fd896452773189f92924ee8e6d4b1f7f6fa27b321145eff165e5c292`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:a9c63ebd13f89a339b8585a605e145b799afdae1ad93cbb411c3d6be0c9af2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359bd50351b5d0b79a26efa3a7dee2f2d6abc6a43eacfd3169dc3602a97fd0b0`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a9680c7f2368fdf5d65a77c22f2e6d2e8c42b9fad6bb42de45a90d79393ee`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.8 MB (3797989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c8e5075a6d85f3eebfb96cc35eb9f5092e5e4e0ac4b05c89b06e6dd92d15ef`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:91995ece7abb19a84d48cfb9ec494dcf10e8721495e8824fdfd82f721c6a4bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452384855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f9b42aa254582181786ea3a1dc78dd813564878dde7736dd65dd07a196296`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 04:36:48 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7fe9a9405de0a49e978e4e5c9f2e884543fdcf565c75e81408bba0e7f2148`  
		Last Modified: Tue, 03 Jun 2025 04:44:18 GMT  
		Size: 52.1 MB (52070735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edbdd8db42ec6c19f89c8dec4f8cb06ed32fa7627bf526b1b1ad0b37e2c8574`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68aeaebbf0603c0f28825078e2e4b8447ed3428a86335fa8606fcc0526ed9c5`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f56713fb3b0e3391646969776f24d722e09f71248381fac93342d065f53e7b`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fafbc7aee75d684bf66dee390a1550906b0b03d02fc52aea8bc1c1c09899ea`  
		Last Modified: Tue, 03 Jun 2025 07:46:23 GMT  
		Size: 353.6 MB (353635048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf75d686d811dc75815ad81e0ce70af8253eb7d1841fe14510f836633713a5c`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.3 MB (3256232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c922eb8a70edea13fb36e6dee6556a291eea92646c86729a7060f7ba3ef7e`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 467.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3260b5d7de87a2b28d0f825de1e5cd6f509bf9a3edbb9891ff5f5f3dd54f7`  
		Last Modified: Tue, 03 Jun 2025 07:46:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:9193f446c498fc928523191e3a14140f9f948d34baeda22b04694e24769f8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f683e3a26764e8c7d0cb8c697543f3e1a5308fda83eb96700d678c87bff15`

```dockerfile
```

-	Layers:
	-	`sha256:37497612c17d717e24b9829385961ad356b7c9bdfd1fb218068302135b470544`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.8 MB (3797657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109126a455a73b649e16502d1d3e465bbbb437f87d3a8c7bfd01faa8f6c3b462`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32.0-alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Fri, 23 May 2025 17:08:03 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Fri, 23 May 2025 17:09:28 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Fri, 23 May 2025 17:08:03 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Fri, 23 May 2025 17:07:57 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Fri, 23 May 2025 17:07:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Fri, 23 May 2025 17:09:28 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Fri, 23 May 2025 17:09:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Fri, 23 May 2025 17:09:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Fri, 23 May 2025 17:09:20 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:b1c9e4082ab9039aaf181425d1399551b74ce4078c5e2b22397407485908d3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:4902301eaa3b8e674065ee545f7d20b8052bce6419b0d561fbc5d77710d2d50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c309eb793b0627c106c8c47de95b23351a40cc97cd34046f5f5f5bc2500ffc5`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec65b0a960d876d89c4e336597de256371b2c39f8a70053a74a88f6432aa78d`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 16.1 MB (16146403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f6ebde483e5e55714fbed9a5d73ee34bcf3bd2098862ddbe020fc48fb9bd34`  
		Last Modified: Tue, 03 Jun 2025 04:16:10 GMT  
		Size: 52.9 MB (52891235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d914152eed4806d3ec7eb97d67feea997fc20d7ba8956d38359c128ef1f265`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b977c46889de2487c980399cba0fa6c04d3bd8fde596eb59cccf75b06684ea8`  
		Last Modified: Tue, 03 Jun 2025 04:16:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b534e2236d6ca10f8ab1fe5e66351b1c4fd4d229b732cd27bc6ae05207a402a0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63e4b5b057d247baaeb40e2710c7b3b743f633b365a30f0d26c53775f25b85`  
		Last Modified: Tue, 03 Jun 2025 05:13:38 GMT  
		Size: 353.6 MB (353635002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c858b74cb07bc3d83a5cc3275ff29c6701a18c7e7ecf8e05db65fc4d8aee5`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.5 MB (3514817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22df6c14824078b1524f367c45b7aa3a03e3cd21d08baf49e9582959e8c44f0`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595edb5fd896452773189f92924ee8e6d4b1f7f6fa27b321145eff165e5c292`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:a9c63ebd13f89a339b8585a605e145b799afdae1ad93cbb411c3d6be0c9af2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359bd50351b5d0b79a26efa3a7dee2f2d6abc6a43eacfd3169dc3602a97fd0b0`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a9680c7f2368fdf5d65a77c22f2e6d2e8c42b9fad6bb42de45a90d79393ee`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 3.8 MB (3797989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70c8e5075a6d85f3eebfb96cc35eb9f5092e5e4e0ac4b05c89b06e6dd92d15ef`  
		Last Modified: Tue, 03 Jun 2025 05:13:33 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:91995ece7abb19a84d48cfb9ec494dcf10e8721495e8824fdfd82f721c6a4bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452384855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7f9b42aa254582181786ea3a1dc78dd813564878dde7736dd65dd07a196296`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 04:36:48 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7fe9a9405de0a49e978e4e5c9f2e884543fdcf565c75e81408bba0e7f2148`  
		Last Modified: Tue, 03 Jun 2025 04:44:18 GMT  
		Size: 52.1 MB (52070735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edbdd8db42ec6c19f89c8dec4f8cb06ed32fa7627bf526b1b1ad0b37e2c8574`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68aeaebbf0603c0f28825078e2e4b8447ed3428a86335fa8606fcc0526ed9c5`  
		Last Modified: Tue, 03 Jun 2025 04:44:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f56713fb3b0e3391646969776f24d722e09f71248381fac93342d065f53e7b`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fafbc7aee75d684bf66dee390a1550906b0b03d02fc52aea8bc1c1c09899ea`  
		Last Modified: Tue, 03 Jun 2025 07:46:23 GMT  
		Size: 353.6 MB (353635048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf75d686d811dc75815ad81e0ce70af8253eb7d1841fe14510f836633713a5c`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.3 MB (3256232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c922eb8a70edea13fb36e6dee6556a291eea92646c86729a7060f7ba3ef7e`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 467.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3260b5d7de87a2b28d0f825de1e5cd6f509bf9a3edbb9891ff5f5f3dd54f7`  
		Last Modified: Tue, 03 Jun 2025 07:46:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:9193f446c498fc928523191e3a14140f9f948d34baeda22b04694e24769f8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f683e3a26764e8c7d0cb8c697543f3e1a5308fda83eb96700d678c87bff15`

```dockerfile
```

-	Layers:
	-	`sha256:37497612c17d717e24b9829385961ad356b7c9bdfd1fb218068302135b470544`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 3.8 MB (3797657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109126a455a73b649e16502d1d3e465bbbb437f87d3a8c7bfd01faa8f6c3b462`  
		Last Modified: Tue, 03 Jun 2025 07:46:15 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json
