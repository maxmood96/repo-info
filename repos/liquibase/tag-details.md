<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.29`](#liquibase429)
-	[`liquibase:4.29-alpine`](#liquibase429-alpine)
-	[`liquibase:4.29.1`](#liquibase4291)
-	[`liquibase:4.29.1-alpine`](#liquibase4291-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.29`

```console
$ docker pull liquibase@sha256:5b290675caef41847597ea5280e65df38b336356fc70b07a0851dea540856af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29` - linux; amd64

```console
$ docker pull liquibase@sha256:f3b9df1fc511bf4cc1dadd71976d9994b9e28bdef5bbb1c01a5b2302dde0707d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256434588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734703d225f9f3ee8329298306b5715fca8b67571f1e02d067755ee8e5a2207`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:11:35 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:11:42 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:11:59 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:11:59 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:12:00 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:12:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:12:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eca7d84c4f90ab0cd2f92a6db1013c1627e1122723c86a3017a43e0e217e4c`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65621e1ebd3867beb09e4b57b0a218cbc8b25fb96c38feea94843abea6b0b78d`  
		Last Modified: Sat, 17 Aug 2024 02:12:18 GMT  
		Size: 159.4 MB (159381739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483b686df2386554d1dbf1cf11abeb23bbbe9ae9c2a8de006f478e0567801b50`  
		Last Modified: Sat, 17 Aug 2024 02:12:13 GMT  
		Size: 6.5 MB (6456520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad0da9ddcf22157db359a332460aa69db78410104e5808660b4c470bc5db792`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa75822a18331fe39bbd3b34cefd89a0193c3852c25b2b0306552fdda3d514aa`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9ee07feac6cdd28c32d7fa82ea5cb75e6790260dcee9b718d0b6a9e62e0ce186
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253412984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4c75f208e998297af4e6e549ddb4751332194605c9d25494ed679143195e25`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:30 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:03:38 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:03:45 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:03:45 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:46 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560407f77d279e68f72a6b12199439583872a1ea3f7441297485cd75f35c2820`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dec1926495611b720c1a1d388d7b0d5ed3da6f69b5fc74f71421273f78c350`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6c42847b35ab5f9a3c427b90ed18660ce9002f66de7635f7dede2c72d73394`  
		Last Modified: Sat, 17 Aug 2024 02:04:02 GMT  
		Size: 159.4 MB (159381752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5093af0d6c86d09d100aa4d1989ba734cd29a82acb76187a1955880c1609fd`  
		Last Modified: Sat, 17 Aug 2024 02:03:57 GMT  
		Size: 6.1 MB (6069989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9c0953efd13bbf9f5f69b58f941cfc55bcf2ee74ae702c8e1d5c6b123f157b`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa591c6a11ab6f2e748c89b8c51dc29954f3e3b4bce94deebd8ae8cc82a3df`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29-alpine`

```console
$ docker pull liquibase@sha256:d796db17f96fd85187cfb689abf080c65c18eb7804c13199c71aa475bcfdd6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:499f4e54fd376a52d1d3a16c04bed41858e5d6d56a2b390efc608187702cfc50
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231743935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f5732baf94b8f5b7f7244e434c9456fa93bc14403d17e03fb9ac0e441502c8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:05:38 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Tue, 23 Jul 2024 04:05:42 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Tue, 23 Jul 2024 04:05:43 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:41 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:44 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:45 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6757eddc9ce0ab1a85b3f990c6d9ca9b68598a52fce93e60d3aa5ec44ee582dd`  
		Last Modified: Tue, 23 Jul 2024 04:06:20 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa81c294df45132eb82f9223f5ddfc333b786f666ff4438fb87191ff695d5d2b`  
		Last Modified: Tue, 23 Jul 2024 04:06:26 GMT  
		Size: 62.6 MB (62569151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e83bfd133da3dcb7908e0fe27e2cb6d1bc3b924dea8c0396ea15ea465e9b45`  
		Last Modified: Thu, 01 Aug 2024 17:21:21 GMT  
		Size: 159.4 MB (159400107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f8734ce8aff113e0a99bb2d52b9b80eeea7ecf16d9a30809e39c26565ea799`  
		Last Modified: Thu, 01 Aug 2024 17:21:15 GMT  
		Size: 6.2 MB (6150149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f480dc64b6753db2a274d4f5191dbe1cfb07f6d1f1bc8d8fb00e468fd8dca0`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d311b37461466e7899a8f58ed2705af583aee7fbfc61776eded1ff0a6ec69`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d6dc87262b55599a930cfd62d1f5b6e6bed04a44264cf031b36e5bb61667c13a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231524486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07a43cd89987cbdd98c76e816aef44c4883d39eb80c0115b7722c618a6b2f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:29:14 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Mon, 22 Jul 2024 23:29:17 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Mon, 22 Jul 2024 23:29:18 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:40:25 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:28 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:29 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c89a30270dba2df842d3f9e23002f26048cfa8ca5eed67892fa8efeddb70e54`  
		Last Modified: Mon, 22 Jul 2024 23:29:41 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc126da2d7c5b5a4e469417f0e9090ee72833875043a214101ff3d9c876d782`  
		Last Modified: Mon, 22 Jul 2024 23:29:46 GMT  
		Size: 62.3 MB (62276010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf01605e9734bb64fee0d8a53b2355a1f151e291f49cf491c009cf7dac413c0`  
		Last Modified: Thu, 01 Aug 2024 17:41:00 GMT  
		Size: 159.4 MB (159400209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c69e260be002f8a97744c41a8886dbc2841638889c1eb4b464c544bfea2dc7`  
		Last Modified: Thu, 01 Aug 2024 17:40:55 GMT  
		Size: 5.8 MB (5759699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f12bda5bd8ffb590974bacc3ec800c78ccebf9296729aac629af1ad768be7b`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aefa573ad1157b5f0b31654cf8933734c979805dbfc1d23535630f940ece33`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29.1`

```console
$ docker pull liquibase@sha256:5b290675caef41847597ea5280e65df38b336356fc70b07a0851dea540856af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29.1` - linux; amd64

```console
$ docker pull liquibase@sha256:f3b9df1fc511bf4cc1dadd71976d9994b9e28bdef5bbb1c01a5b2302dde0707d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256434588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734703d225f9f3ee8329298306b5715fca8b67571f1e02d067755ee8e5a2207`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:11:35 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:11:42 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:11:59 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:11:59 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:12:00 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:12:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:12:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eca7d84c4f90ab0cd2f92a6db1013c1627e1122723c86a3017a43e0e217e4c`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65621e1ebd3867beb09e4b57b0a218cbc8b25fb96c38feea94843abea6b0b78d`  
		Last Modified: Sat, 17 Aug 2024 02:12:18 GMT  
		Size: 159.4 MB (159381739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483b686df2386554d1dbf1cf11abeb23bbbe9ae9c2a8de006f478e0567801b50`  
		Last Modified: Sat, 17 Aug 2024 02:12:13 GMT  
		Size: 6.5 MB (6456520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad0da9ddcf22157db359a332460aa69db78410104e5808660b4c470bc5db792`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa75822a18331fe39bbd3b34cefd89a0193c3852c25b2b0306552fdda3d514aa`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9ee07feac6cdd28c32d7fa82ea5cb75e6790260dcee9b718d0b6a9e62e0ce186
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253412984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4c75f208e998297af4e6e549ddb4751332194605c9d25494ed679143195e25`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:30 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:03:38 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:03:45 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:03:45 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:46 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560407f77d279e68f72a6b12199439583872a1ea3f7441297485cd75f35c2820`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dec1926495611b720c1a1d388d7b0d5ed3da6f69b5fc74f71421273f78c350`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6c42847b35ab5f9a3c427b90ed18660ce9002f66de7635f7dede2c72d73394`  
		Last Modified: Sat, 17 Aug 2024 02:04:02 GMT  
		Size: 159.4 MB (159381752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5093af0d6c86d09d100aa4d1989ba734cd29a82acb76187a1955880c1609fd`  
		Last Modified: Sat, 17 Aug 2024 02:03:57 GMT  
		Size: 6.1 MB (6069989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9c0953efd13bbf9f5f69b58f941cfc55bcf2ee74ae702c8e1d5c6b123f157b`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa591c6a11ab6f2e748c89b8c51dc29954f3e3b4bce94deebd8ae8cc82a3df`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29.1-alpine`

```console
$ docker pull liquibase@sha256:d796db17f96fd85187cfb689abf080c65c18eb7804c13199c71aa475bcfdd6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:499f4e54fd376a52d1d3a16c04bed41858e5d6d56a2b390efc608187702cfc50
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231743935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f5732baf94b8f5b7f7244e434c9456fa93bc14403d17e03fb9ac0e441502c8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:05:38 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Tue, 23 Jul 2024 04:05:42 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Tue, 23 Jul 2024 04:05:43 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:41 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:44 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:45 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6757eddc9ce0ab1a85b3f990c6d9ca9b68598a52fce93e60d3aa5ec44ee582dd`  
		Last Modified: Tue, 23 Jul 2024 04:06:20 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa81c294df45132eb82f9223f5ddfc333b786f666ff4438fb87191ff695d5d2b`  
		Last Modified: Tue, 23 Jul 2024 04:06:26 GMT  
		Size: 62.6 MB (62569151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e83bfd133da3dcb7908e0fe27e2cb6d1bc3b924dea8c0396ea15ea465e9b45`  
		Last Modified: Thu, 01 Aug 2024 17:21:21 GMT  
		Size: 159.4 MB (159400107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f8734ce8aff113e0a99bb2d52b9b80eeea7ecf16d9a30809e39c26565ea799`  
		Last Modified: Thu, 01 Aug 2024 17:21:15 GMT  
		Size: 6.2 MB (6150149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f480dc64b6753db2a274d4f5191dbe1cfb07f6d1f1bc8d8fb00e468fd8dca0`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d311b37461466e7899a8f58ed2705af583aee7fbfc61776eded1ff0a6ec69`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d6dc87262b55599a930cfd62d1f5b6e6bed04a44264cf031b36e5bb61667c13a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231524486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07a43cd89987cbdd98c76e816aef44c4883d39eb80c0115b7722c618a6b2f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:29:14 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Mon, 22 Jul 2024 23:29:17 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Mon, 22 Jul 2024 23:29:18 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:40:25 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:28 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:29 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c89a30270dba2df842d3f9e23002f26048cfa8ca5eed67892fa8efeddb70e54`  
		Last Modified: Mon, 22 Jul 2024 23:29:41 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc126da2d7c5b5a4e469417f0e9090ee72833875043a214101ff3d9c876d782`  
		Last Modified: Mon, 22 Jul 2024 23:29:46 GMT  
		Size: 62.3 MB (62276010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf01605e9734bb64fee0d8a53b2355a1f151e291f49cf491c009cf7dac413c0`  
		Last Modified: Thu, 01 Aug 2024 17:41:00 GMT  
		Size: 159.4 MB (159400209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c69e260be002f8a97744c41a8886dbc2841638889c1eb4b464c544bfea2dc7`  
		Last Modified: Thu, 01 Aug 2024 17:40:55 GMT  
		Size: 5.8 MB (5759699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f12bda5bd8ffb590974bacc3ec800c78ccebf9296729aac629af1ad768be7b`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aefa573ad1157b5f0b31654cf8933734c979805dbfc1d23535630f940ece33`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:d796db17f96fd85187cfb689abf080c65c18eb7804c13199c71aa475bcfdd6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:499f4e54fd376a52d1d3a16c04bed41858e5d6d56a2b390efc608187702cfc50
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231743935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f5732baf94b8f5b7f7244e434c9456fa93bc14403d17e03fb9ac0e441502c8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 04:05:38 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Tue, 23 Jul 2024 04:05:42 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Tue, 23 Jul 2024 04:05:43 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:34 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:41 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:42 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:44 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:44 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:44 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:45 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6757eddc9ce0ab1a85b3f990c6d9ca9b68598a52fce93e60d3aa5ec44ee582dd`  
		Last Modified: Tue, 23 Jul 2024 04:06:20 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa81c294df45132eb82f9223f5ddfc333b786f666ff4438fb87191ff695d5d2b`  
		Last Modified: Tue, 23 Jul 2024 04:06:26 GMT  
		Size: 62.6 MB (62569151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e83bfd133da3dcb7908e0fe27e2cb6d1bc3b924dea8c0396ea15ea465e9b45`  
		Last Modified: Thu, 01 Aug 2024 17:21:21 GMT  
		Size: 159.4 MB (159400107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f8734ce8aff113e0a99bb2d52b9b80eeea7ecf16d9a30809e39c26565ea799`  
		Last Modified: Thu, 01 Aug 2024 17:21:15 GMT  
		Size: 6.2 MB (6150149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f480dc64b6753db2a274d4f5191dbe1cfb07f6d1f1bc8d8fb00e468fd8dca0`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d311b37461466e7899a8f58ed2705af583aee7fbfc61776eded1ff0a6ec69`  
		Last Modified: Thu, 01 Aug 2024 17:21:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d6dc87262b55599a930cfd62d1f5b6e6bed04a44264cf031b36e5bb61667c13a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231524486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07a43cd89987cbdd98c76e816aef44c4883d39eb80c0115b7722c618a6b2f8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:29:14 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Mon, 22 Jul 2024 23:29:17 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Mon, 22 Jul 2024 23:29:18 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:40:18 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:40:25 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:40:26 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:28 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:28 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:29 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c89a30270dba2df842d3f9e23002f26048cfa8ca5eed67892fa8efeddb70e54`  
		Last Modified: Mon, 22 Jul 2024 23:29:41 GMT  
		Size: 982.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc126da2d7c5b5a4e469417f0e9090ee72833875043a214101ff3d9c876d782`  
		Last Modified: Mon, 22 Jul 2024 23:29:46 GMT  
		Size: 62.3 MB (62276010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf01605e9734bb64fee0d8a53b2355a1f151e291f49cf491c009cf7dac413c0`  
		Last Modified: Thu, 01 Aug 2024 17:41:00 GMT  
		Size: 159.4 MB (159400209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c69e260be002f8a97744c41a8886dbc2841638889c1eb4b464c544bfea2dc7`  
		Last Modified: Thu, 01 Aug 2024 17:40:55 GMT  
		Size: 5.8 MB (5759699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f12bda5bd8ffb590974bacc3ec800c78ccebf9296729aac629af1ad768be7b`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aefa573ad1157b5f0b31654cf8933734c979805dbfc1d23535630f940ece33`  
		Last Modified: Thu, 01 Aug 2024 17:40:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:5b290675caef41847597ea5280e65df38b336356fc70b07a0851dea540856af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:f3b9df1fc511bf4cc1dadd71976d9994b9e28bdef5bbb1c01a5b2302dde0707d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256434588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734703d225f9f3ee8329298306b5715fca8b67571f1e02d067755ee8e5a2207`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:11:35 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:11:35 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:11:42 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:11:43 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:11:59 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:11:59 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:11:59 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:12:00 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:12:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:12:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eca7d84c4f90ab0cd2f92a6db1013c1627e1122723c86a3017a43e0e217e4c`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65621e1ebd3867beb09e4b57b0a218cbc8b25fb96c38feea94843abea6b0b78d`  
		Last Modified: Sat, 17 Aug 2024 02:12:18 GMT  
		Size: 159.4 MB (159381739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483b686df2386554d1dbf1cf11abeb23bbbe9ae9c2a8de006f478e0567801b50`  
		Last Modified: Sat, 17 Aug 2024 02:12:13 GMT  
		Size: 6.5 MB (6456520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad0da9ddcf22157db359a332460aa69db78410104e5808660b4c470bc5db792`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa75822a18331fe39bbd3b34cefd89a0193c3852c25b2b0306552fdda3d514aa`  
		Last Modified: Sat, 17 Aug 2024 02:12:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:9ee07feac6cdd28c32d7fa82ea5cb75e6790260dcee9b718d0b6a9e62e0ce186
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253412984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4c75f208e998297af4e6e549ddb4751332194605c9d25494ed679143195e25`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:30 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
WORKDIR /liquibase
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Sat, 17 Aug 2024 02:03:30 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Sat, 17 Aug 2024 02:03:38 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_VERSION=0.2.7
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Sat, 17 Aug 2024 02:03:38 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Sat, 17 Aug 2024 02:03:45 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Sat, 17 Aug 2024 02:03:45 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Sat, 17 Aug 2024 02:03:45 GMT
USER liquibase:liquibase
# Sat, 17 Aug 2024 02:03:45 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 17 Aug 2024 02:03:46 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560407f77d279e68f72a6b12199439583872a1ea3f7441297485cd75f35c2820`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dec1926495611b720c1a1d388d7b0d5ed3da6f69b5fc74f71421273f78c350`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6c42847b35ab5f9a3c427b90ed18660ce9002f66de7635f7dede2c72d73394`  
		Last Modified: Sat, 17 Aug 2024 02:04:02 GMT  
		Size: 159.4 MB (159381752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5093af0d6c86d09d100aa4d1989ba734cd29a82acb76187a1955880c1609fd`  
		Last Modified: Sat, 17 Aug 2024 02:03:57 GMT  
		Size: 6.1 MB (6069989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9c0953efd13bbf9f5f69b58f941cfc55bcf2ee74ae702c8e1d5c6b123f157b`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa591c6a11ab6f2e748c89b8c51dc29954f3e3b4bce94deebd8ae8cc82a3df`  
		Last Modified: Sat, 17 Aug 2024 02:03:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
