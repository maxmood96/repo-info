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
$ docker pull liquibase@sha256:a27dff4cba3f0c99f00b0598786c500f978c986c69d83c223400f56e9ede8257
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32` - linux; amd64

```console
$ docker pull liquibase@sha256:0d350aa925f8e546a8d8d399c15d4608c6b5509c7e74fb26dacaa065911ab3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f45e786a35019a591e5b60e8f27c508a17898f3e31b520cb5a98c536751ec6d`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882ea02fb5c855bf43fdc95ed1014a31bed0f381b9c67d0c48fa6f4739b1b37`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 16.1 MB (16146129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca298b922759e55496c02c3046c177b262e098e2f246425d6ac38dcef5556b`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 52.9 MB (52891233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca81fa2d6cd8292d9a604b62d9bb2d5e109095de9d716b30ac6f8b00547bf63`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f097bb5d471697950a9be820f9ea4aee721a780ff33e2d096c0e549e0b5281f`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958e98e9bd688fdc1dc7c847c6543d8680472aa6caa924fa0b7aaf1dca4211f`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee521cb2acb6c741b13e6f865a721f64c60465ee171ef1d97247fe595056f93`  
		Last Modified: Fri, 23 May 2025 17:08:01 GMT  
		Size: 353.6 MB (353635053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a4db002fb2318ae0f456dff5ae4263df1ee59d6529ace2034ae748e2f22e25`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.5 MB (3514953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c3f8066e579ead62154482f01200f2f295e043bdaa6d0e2cf497fccefaa95`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac01b82f1bd883e890dcfa3c3579f676f279d5466c45e8f83f94a4b88e6bf79`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:90b6ea7fffa78b6249f892fa66d619319745b66f74861ba086f992af76da2e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a54a66087f09fd1f279c9969b6102e5a5b03c1087effa7a7b3caf72dce395`

```dockerfile
```

-	Layers:
	-	`sha256:8f55be1ec26432186bb5caaaf035887675cc2e6a324b56d655cda1682a947c73`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.8 MB (3797977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80706024593596d75ebe100ca946d4245a8a538463257a297bf187be1bcef8f0`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e1e71f1cbe92874fd3f6c871b1672b3b6b62271e3d4befd8c2f4ea5fe19294d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452383345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79763a44eed71f0da68679852185fec6d41bbea210e2657c8c8c42b6a07ec0b7`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc2e83745f5161ac5876e1e145987a65feb3f11b8d6957c1e6011f3cb9d42a8`  
		Last Modified: Mon, 05 May 2025 16:58:07 GMT  
		Size: 52.1 MB (52070754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac615b4401d254f31aceacac2a102ab32b6eee92e74b4df225dd7d441c7adf2e`  
		Last Modified: Mon, 05 May 2025 16:58:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e772fc7223005edf5117652fbb5f4ba65fad1fa4035b6b61068823847fdfbc`  
		Last Modified: Mon, 05 May 2025 16:58:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f9235bfe7aa59babdef142a63fb93aa3456c37921d672a0cab72ed4599d78d`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173cd0f721e967d12ff75eb4ec296f271be1e51f181bf08fa8f3c25a34754860`  
		Last Modified: Fri, 23 May 2025 17:08:31 GMT  
		Size: 353.6 MB (353635052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2d39e0c486fd31fb9b828c6d59859550e0f93ad53ed501a26132a078068aac`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.3 MB (3256292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99ce3c41aa39aac3a5829d9fe83bb1872813c7b103629e0f674ca9e21efb73`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1dc20e7529a8ae97ef2c694fa6e36808b3e17745781cc5103f277ad92fce7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:04b2be41aeb65f1f12680713dbb6d70a3ed79a240e2238eed8f0453a1c4de31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19890be5465186e8792a71eada4a03a6e9a01b04248594358fd55cfcd87955ff`

```dockerfile
```

-	Layers:
	-	`sha256:4f7475d95baba7852355b534f8c865af31e431f70e3261fe4ef3e0e055cc32f7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.8 MB (3797645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44dd890efcbf74f1aec7b6798bb0fb4185985f29013bc932414e6de300ba358a`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
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
$ docker pull liquibase@sha256:a27dff4cba3f0c99f00b0598786c500f978c986c69d83c223400f56e9ede8257
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32.0` - linux; amd64

```console
$ docker pull liquibase@sha256:0d350aa925f8e546a8d8d399c15d4608c6b5509c7e74fb26dacaa065911ab3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f45e786a35019a591e5b60e8f27c508a17898f3e31b520cb5a98c536751ec6d`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882ea02fb5c855bf43fdc95ed1014a31bed0f381b9c67d0c48fa6f4739b1b37`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 16.1 MB (16146129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca298b922759e55496c02c3046c177b262e098e2f246425d6ac38dcef5556b`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 52.9 MB (52891233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca81fa2d6cd8292d9a604b62d9bb2d5e109095de9d716b30ac6f8b00547bf63`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f097bb5d471697950a9be820f9ea4aee721a780ff33e2d096c0e549e0b5281f`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958e98e9bd688fdc1dc7c847c6543d8680472aa6caa924fa0b7aaf1dca4211f`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee521cb2acb6c741b13e6f865a721f64c60465ee171ef1d97247fe595056f93`  
		Last Modified: Fri, 23 May 2025 17:08:01 GMT  
		Size: 353.6 MB (353635053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a4db002fb2318ae0f456dff5ae4263df1ee59d6529ace2034ae748e2f22e25`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.5 MB (3514953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c3f8066e579ead62154482f01200f2f295e043bdaa6d0e2cf497fccefaa95`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac01b82f1bd883e890dcfa3c3579f676f279d5466c45e8f83f94a4b88e6bf79`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:90b6ea7fffa78b6249f892fa66d619319745b66f74861ba086f992af76da2e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a54a66087f09fd1f279c9969b6102e5a5b03c1087effa7a7b3caf72dce395`

```dockerfile
```

-	Layers:
	-	`sha256:8f55be1ec26432186bb5caaaf035887675cc2e6a324b56d655cda1682a947c73`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.8 MB (3797977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80706024593596d75ebe100ca946d4245a8a538463257a297bf187be1bcef8f0`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e1e71f1cbe92874fd3f6c871b1672b3b6b62271e3d4befd8c2f4ea5fe19294d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452383345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79763a44eed71f0da68679852185fec6d41bbea210e2657c8c8c42b6a07ec0b7`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc2e83745f5161ac5876e1e145987a65feb3f11b8d6957c1e6011f3cb9d42a8`  
		Last Modified: Mon, 05 May 2025 16:58:07 GMT  
		Size: 52.1 MB (52070754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac615b4401d254f31aceacac2a102ab32b6eee92e74b4df225dd7d441c7adf2e`  
		Last Modified: Mon, 05 May 2025 16:58:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e772fc7223005edf5117652fbb5f4ba65fad1fa4035b6b61068823847fdfbc`  
		Last Modified: Mon, 05 May 2025 16:58:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f9235bfe7aa59babdef142a63fb93aa3456c37921d672a0cab72ed4599d78d`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173cd0f721e967d12ff75eb4ec296f271be1e51f181bf08fa8f3c25a34754860`  
		Last Modified: Fri, 23 May 2025 17:08:31 GMT  
		Size: 353.6 MB (353635052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2d39e0c486fd31fb9b828c6d59859550e0f93ad53ed501a26132a078068aac`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.3 MB (3256292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99ce3c41aa39aac3a5829d9fe83bb1872813c7b103629e0f674ca9e21efb73`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1dc20e7529a8ae97ef2c694fa6e36808b3e17745781cc5103f277ad92fce7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:04b2be41aeb65f1f12680713dbb6d70a3ed79a240e2238eed8f0453a1c4de31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19890be5465186e8792a71eada4a03a6e9a01b04248594358fd55cfcd87955ff`

```dockerfile
```

-	Layers:
	-	`sha256:4f7475d95baba7852355b534f8c865af31e431f70e3261fe4ef3e0e055cc32f7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.8 MB (3797645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44dd890efcbf74f1aec7b6798bb0fb4185985f29013bc932414e6de300ba358a`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
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
$ docker pull liquibase@sha256:a27dff4cba3f0c99f00b0598786c500f978c986c69d83c223400f56e9ede8257
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:0d350aa925f8e546a8d8d399c15d4608c6b5509c7e74fb26dacaa065911ab3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455727405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f45e786a35019a591e5b60e8f27c508a17898f3e31b520cb5a98c536751ec6d`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882ea02fb5c855bf43fdc95ed1014a31bed0f381b9c67d0c48fa6f4739b1b37`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 16.1 MB (16146129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca298b922759e55496c02c3046c177b262e098e2f246425d6ac38dcef5556b`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 52.9 MB (52891233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca81fa2d6cd8292d9a604b62d9bb2d5e109095de9d716b30ac6f8b00547bf63`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f097bb5d471697950a9be820f9ea4aee721a780ff33e2d096c0e549e0b5281f`  
		Last Modified: Mon, 05 May 2025 16:34:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958e98e9bd688fdc1dc7c847c6543d8680472aa6caa924fa0b7aaf1dca4211f`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee521cb2acb6c741b13e6f865a721f64c60465ee171ef1d97247fe595056f93`  
		Last Modified: Fri, 23 May 2025 17:08:01 GMT  
		Size: 353.6 MB (353635053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a4db002fb2318ae0f456dff5ae4263df1ee59d6529ace2034ae748e2f22e25`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.5 MB (3514953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c3f8066e579ead62154482f01200f2f295e043bdaa6d0e2cf497fccefaa95`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac01b82f1bd883e890dcfa3c3579f676f279d5466c45e8f83f94a4b88e6bf79`  
		Last Modified: Fri, 23 May 2025 17:07:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:90b6ea7fffa78b6249f892fa66d619319745b66f74861ba086f992af76da2e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a54a66087f09fd1f279c9969b6102e5a5b03c1087effa7a7b3caf72dce395`

```dockerfile
```

-	Layers:
	-	`sha256:8f55be1ec26432186bb5caaaf035887675cc2e6a324b56d655cda1682a947c73`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 3.8 MB (3797977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80706024593596d75ebe100ca946d4245a8a538463257a297bf187be1bcef8f0`  
		Last Modified: Fri, 23 May 2025 17:07:55 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e1e71f1cbe92874fd3f6c871b1672b3b6b62271e3d4befd8c2f4ea5fe19294d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452383345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79763a44eed71f0da68679852185fec6d41bbea210e2657c8c8c42b6a07ec0b7`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc2e83745f5161ac5876e1e145987a65feb3f11b8d6957c1e6011f3cb9d42a8`  
		Last Modified: Mon, 05 May 2025 16:58:07 GMT  
		Size: 52.1 MB (52070754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac615b4401d254f31aceacac2a102ab32b6eee92e74b4df225dd7d441c7adf2e`  
		Last Modified: Mon, 05 May 2025 16:58:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e772fc7223005edf5117652fbb5f4ba65fad1fa4035b6b61068823847fdfbc`  
		Last Modified: Mon, 05 May 2025 16:58:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f9235bfe7aa59babdef142a63fb93aa3456c37921d672a0cab72ed4599d78d`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173cd0f721e967d12ff75eb4ec296f271be1e51f181bf08fa8f3c25a34754860`  
		Last Modified: Fri, 23 May 2025 17:08:31 GMT  
		Size: 353.6 MB (353635052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2d39e0c486fd31fb9b828c6d59859550e0f93ad53ed501a26132a078068aac`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.3 MB (3256292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99ce3c41aa39aac3a5829d9fe83bb1872813c7b103629e0f674ca9e21efb73`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1dc20e7529a8ae97ef2c694fa6e36808b3e17745781cc5103f277ad92fce7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:04b2be41aeb65f1f12680713dbb6d70a3ed79a240e2238eed8f0453a1c4de31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19890be5465186e8792a71eada4a03a6e9a01b04248594358fd55cfcd87955ff`

```dockerfile
```

-	Layers:
	-	`sha256:4f7475d95baba7852355b534f8c865af31e431f70e3261fe4ef3e0e055cc32f7`  
		Last Modified: Fri, 23 May 2025 17:08:24 GMT  
		Size: 3.8 MB (3797645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44dd890efcbf74f1aec7b6798bb0fb4185985f29013bc932414e6de300ba358a`  
		Last Modified: Fri, 23 May 2025 17:08:23 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json
