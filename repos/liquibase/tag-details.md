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
$ docker pull liquibase@sha256:5bda6750633396a7082f806fe9170cda670d394ee3600344a934615eec36f744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29` - linux; amd64

```console
$ docker pull liquibase@sha256:b76549527b647806e524ec3b66fe28b61b6f0a90bc52c529402a07a6cec0749a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256433835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febc5de5626210b8214a2c486b3f67e20c2e62e31236a7e6cc51e354e1ea481c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
# Thu, 25 Jul 2024 17:57:10 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 17:57:10 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:15 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:26 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29200f0ca873c251fc1d04587802ff9cc275bdc6e108f2d9a4988233692aed7a`  
		Last Modified: Thu, 25 Jul 2024 17:57:47 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee00faa6f058447b5885bc0b4ac33b59209e42c7a0cb2b9169b61b16f6dda5f`  
		Last Modified: Thu, 01 Aug 2024 17:21:05 GMT  
		Size: 159.4 MB (159381720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e023fad92b9dea1db85ded6c9a8a310c907e0e92b5ce26ac42705611807d61`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 6.5 MB (6456491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8043a93c019f02780f96de72f1fdfa7acf4bfea761ca311d4721b0c6fff4a72`  
		Last Modified: Thu, 01 Aug 2024 17:20:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f1782f280922d4691c48fdc9a5f7de76eb1b130824bda28b02d2ecd12fdb2c`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:cf2d41bc3dcaeeab68328519b520dab32469099c7ed11b3a0793db7d3115c242
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253416748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813a92a076e6dc1d51ee782eadebb2a2d8b8fbf5c063b920020461291d9c73d8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
# Thu, 25 Jul 2024 18:11:28 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 18:11:29 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:39:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:10 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254df85c65cc285fa065945e147a07d290e57f430e9874aa3ce4613529993d1e`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a0cf91c66f914d10fb765e06a0df349eaf1580daa5a61e99ea76ac0834e8db`  
		Last Modified: Thu, 01 Aug 2024 17:40:44 GMT  
		Size: 159.4 MB (159381725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735a8ef600e97f7f16c62c62357d550cfc8de1286a56a0cffdcda7bcf0f602c9`  
		Last Modified: Thu, 01 Aug 2024 17:40:39 GMT  
		Size: 6.1 MB (6070030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e72bceddfd252c7966104db3e0478c9b538904c08e6b3e8259ee87b828af9f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1083dc4f1bc28fdc2be06ec75fffd39601997fba40d006e41174151595202f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
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
$ docker pull liquibase@sha256:5bda6750633396a7082f806fe9170cda670d394ee3600344a934615eec36f744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:4.29.1` - linux; amd64

```console
$ docker pull liquibase@sha256:b76549527b647806e524ec3b66fe28b61b6f0a90bc52c529402a07a6cec0749a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256433835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febc5de5626210b8214a2c486b3f67e20c2e62e31236a7e6cc51e354e1ea481c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
# Thu, 25 Jul 2024 17:57:10 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 17:57:10 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:15 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:26 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29200f0ca873c251fc1d04587802ff9cc275bdc6e108f2d9a4988233692aed7a`  
		Last Modified: Thu, 25 Jul 2024 17:57:47 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee00faa6f058447b5885bc0b4ac33b59209e42c7a0cb2b9169b61b16f6dda5f`  
		Last Modified: Thu, 01 Aug 2024 17:21:05 GMT  
		Size: 159.4 MB (159381720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e023fad92b9dea1db85ded6c9a8a310c907e0e92b5ce26ac42705611807d61`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 6.5 MB (6456491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8043a93c019f02780f96de72f1fdfa7acf4bfea761ca311d4721b0c6fff4a72`  
		Last Modified: Thu, 01 Aug 2024 17:20:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f1782f280922d4691c48fdc9a5f7de76eb1b130824bda28b02d2ecd12fdb2c`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:4.29.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:cf2d41bc3dcaeeab68328519b520dab32469099c7ed11b3a0793db7d3115c242
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253416748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813a92a076e6dc1d51ee782eadebb2a2d8b8fbf5c063b920020461291d9c73d8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
# Thu, 25 Jul 2024 18:11:28 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 18:11:29 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:39:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:10 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254df85c65cc285fa065945e147a07d290e57f430e9874aa3ce4613529993d1e`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a0cf91c66f914d10fb765e06a0df349eaf1580daa5a61e99ea76ac0834e8db`  
		Last Modified: Thu, 01 Aug 2024 17:40:44 GMT  
		Size: 159.4 MB (159381725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735a8ef600e97f7f16c62c62357d550cfc8de1286a56a0cffdcda7bcf0f602c9`  
		Last Modified: Thu, 01 Aug 2024 17:40:39 GMT  
		Size: 6.1 MB (6070030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e72bceddfd252c7966104db3e0478c9b538904c08e6b3e8259ee87b828af9f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1083dc4f1bc28fdc2be06ec75fffd39601997fba40d006e41174151595202f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
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
$ docker pull liquibase@sha256:5bda6750633396a7082f806fe9170cda670d394ee3600344a934615eec36f744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:b76549527b647806e524ec3b66fe28b61b6f0a90bc52c529402a07a6cec0749a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256433835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febc5de5626210b8214a2c486b3f67e20c2e62e31236a7e6cc51e354e1ea481c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
# Thu, 25 Jul 2024 17:57:10 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 17:57:10 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:20:05 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:20:15 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:20:15 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:20:26 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:20:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:20:27 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:20:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:20:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29200f0ca873c251fc1d04587802ff9cc275bdc6e108f2d9a4988233692aed7a`  
		Last Modified: Thu, 25 Jul 2024 17:57:47 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee00faa6f058447b5885bc0b4ac33b59209e42c7a0cb2b9169b61b16f6dda5f`  
		Last Modified: Thu, 01 Aug 2024 17:21:05 GMT  
		Size: 159.4 MB (159381720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e023fad92b9dea1db85ded6c9a8a310c907e0e92b5ce26ac42705611807d61`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 6.5 MB (6456491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8043a93c019f02780f96de72f1fdfa7acf4bfea761ca311d4721b0c6fff4a72`  
		Last Modified: Thu, 01 Aug 2024 17:20:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f1782f280922d4691c48fdc9a5f7de76eb1b130824bda28b02d2ecd12fdb2c`  
		Last Modified: Thu, 01 Aug 2024 17:20:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:cf2d41bc3dcaeeab68328519b520dab32469099c7ed11b3a0793db7d3115c242
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253416748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813a92a076e6dc1d51ee782eadebb2a2d8b8fbf5c063b920020461291d9c73d8`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
# Thu, 25 Jul 2024 18:11:28 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 25 Jul 2024 18:11:29 GMT
WORKDIR /liquibase
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LIQUIBASE_VERSION=4.29.1
# Thu, 01 Aug 2024 17:39:38 GMT
ARG LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117
# Thu, 01 Aug 2024 17:39:44 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_VERSION=0.2.7
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 01 Aug 2024 17:39:45 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 01 Aug 2024 17:40:10 GMT
# ARGS: LB_SHA256=30524ff1c1be1aac46b774bcc7e2d5488eb217c174e9ff82f0bac244feb9b117 LIQUIBASE_VERSION=4.29.1 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 01 Aug 2024 17:40:10 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 01 Aug 2024 17:40:10 GMT
USER liquibase:liquibase
# Thu, 01 Aug 2024 17:40:10 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 01 Aug 2024 17:40:10 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254df85c65cc285fa065945e147a07d290e57f430e9874aa3ce4613529993d1e`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a0cf91c66f914d10fb765e06a0df349eaf1580daa5a61e99ea76ac0834e8db`  
		Last Modified: Thu, 01 Aug 2024 17:40:44 GMT  
		Size: 159.4 MB (159381725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735a8ef600e97f7f16c62c62357d550cfc8de1286a56a0cffdcda7bcf0f602c9`  
		Last Modified: Thu, 01 Aug 2024 17:40:39 GMT  
		Size: 6.1 MB (6070030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e72bceddfd252c7966104db3e0478c9b538904c08e6b3e8259ee87b828af9f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1083dc4f1bc28fdc2be06ec75fffd39601997fba40d006e41174151595202f`  
		Last Modified: Thu, 01 Aug 2024 17:40:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
