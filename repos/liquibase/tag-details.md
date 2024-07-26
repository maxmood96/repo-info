<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.29`](#liquibase429)
-	[`liquibase:4.29-alpine`](#liquibase429-alpine)
-	[`liquibase:4.29.0`](#liquibase4290)
-	[`liquibase:4.29.0-alpine`](#liquibase4290-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.29`

```console
$ docker pull liquibase@sha256:3200c051f380bd5474b0691d65540e8c66c397fc3873fbbde156caa32cf11aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `liquibase:4.29` - linux; amd64

```console
$ docker pull liquibase@sha256:06f486859f565953444595e870c025fc91fe8533b9f998e85e7171ea6e157e90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256424798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01955e3f38f46103205a8a6410649b5a5654e485e6abe5a24d41dddc35ac3eb4`
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
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:09 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:19 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:20 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:20 GMT
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
	-	`sha256:b4fab9c8bd4b694093594bf93ae3a6aa471b63aaa9abb6866a265590f2a5c332`  
		Last Modified: Fri, 26 Jul 2024 18:20:56 GMT  
		Size: 159.4 MB (159372694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358763244c79133d9d1fda0a36ee34c9ee9549707a949f17367e56388b422e5f`  
		Last Modified: Fri, 26 Jul 2024 18:20:50 GMT  
		Size: 6.5 MB (6456480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d469f2a46400f1606700e55ba0c42cc79faca7d4f069b83c23fd7514302517f4`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b06df65429398af55e95d4c26c38f400d045f5e1c6e872493ca304251b3cd`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29-alpine`

```console
$ docker pull liquibase@sha256:e9fcf36a6f6ff43ca5edfcffcb8f7885873fa38c7f798485de4eaf0a82483964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `liquibase:4.29-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:313df8795d37099c2a5a9b6d3a6d013745da7a112d20eed27f597ee2a9b48ac1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231741487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b134f8da57da5f7c146505801303ef5dc2bba6a9e7f02c1efe796e648349f255`
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
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:34 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:37 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:37 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:37 GMT
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
	-	`sha256:b224479de04126dec14faee60b7f54b5cd10e78bc201cca1f6f04a70342c2d6c`  
		Last Modified: Fri, 26 Jul 2024 18:21:13 GMT  
		Size: 159.4 MB (159397665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218c0f31d77277a62a6f52407ecddf48efde7fe8bc1805c4ab40cd12205750c3`  
		Last Modified: Fri, 26 Jul 2024 18:21:07 GMT  
		Size: 6.2 MB (6150143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506ed5c1815bce074d122db421dd32cea493b3ebc3c5d1faa75688fb5231c70c`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f03ab83772bbfad96e40bbda14e8ca0feff31bbe05464a6ba7002a4d54d66e`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29.0`

```console
$ docker pull liquibase@sha256:3200c051f380bd5474b0691d65540e8c66c397fc3873fbbde156caa32cf11aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `liquibase:4.29.0` - linux; amd64

```console
$ docker pull liquibase@sha256:06f486859f565953444595e870c025fc91fe8533b9f998e85e7171ea6e157e90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256424798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01955e3f38f46103205a8a6410649b5a5654e485e6abe5a24d41dddc35ac3eb4`
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
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:09 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:19 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:20 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:20 GMT
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
	-	`sha256:b4fab9c8bd4b694093594bf93ae3a6aa471b63aaa9abb6866a265590f2a5c332`  
		Last Modified: Fri, 26 Jul 2024 18:20:56 GMT  
		Size: 159.4 MB (159372694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358763244c79133d9d1fda0a36ee34c9ee9549707a949f17367e56388b422e5f`  
		Last Modified: Fri, 26 Jul 2024 18:20:50 GMT  
		Size: 6.5 MB (6456480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d469f2a46400f1606700e55ba0c42cc79faca7d4f069b83c23fd7514302517f4`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b06df65429398af55e95d4c26c38f400d045f5e1c6e872493ca304251b3cd`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:4.29.0-alpine`

```console
$ docker pull liquibase@sha256:e9fcf36a6f6ff43ca5edfcffcb8f7885873fa38c7f798485de4eaf0a82483964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `liquibase:4.29.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:313df8795d37099c2a5a9b6d3a6d013745da7a112d20eed27f597ee2a9b48ac1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231741487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b134f8da57da5f7c146505801303ef5dc2bba6a9e7f02c1efe796e648349f255`
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
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:34 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:37 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:37 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:37 GMT
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
	-	`sha256:b224479de04126dec14faee60b7f54b5cd10e78bc201cca1f6f04a70342c2d6c`  
		Last Modified: Fri, 26 Jul 2024 18:21:13 GMT  
		Size: 159.4 MB (159397665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218c0f31d77277a62a6f52407ecddf48efde7fe8bc1805c4ab40cd12205750c3`  
		Last Modified: Fri, 26 Jul 2024 18:21:07 GMT  
		Size: 6.2 MB (6150143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506ed5c1815bce074d122db421dd32cea493b3ebc3c5d1faa75688fb5231c70c`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f03ab83772bbfad96e40bbda14e8ca0feff31bbe05464a6ba7002a4d54d66e`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:b0b7af15d59ef8d5538a12555ec4de62dc414eced91ca5de4b79972f38af08c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:313df8795d37099c2a5a9b6d3a6d013745da7a112d20eed27f597ee2a9b48ac1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231741487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b134f8da57da5f7c146505801303ef5dc2bba6a9e7f02c1efe796e648349f255`
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
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:25 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:34 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:35 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:37 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:37 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:37 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:37 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:37 GMT
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
	-	`sha256:b224479de04126dec14faee60b7f54b5cd10e78bc201cca1f6f04a70342c2d6c`  
		Last Modified: Fri, 26 Jul 2024 18:21:13 GMT  
		Size: 159.4 MB (159397665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218c0f31d77277a62a6f52407ecddf48efde7fe8bc1805c4ab40cd12205750c3`  
		Last Modified: Fri, 26 Jul 2024 18:21:07 GMT  
		Size: 6.2 MB (6150143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506ed5c1815bce074d122db421dd32cea493b3ebc3c5d1faa75688fb5231c70c`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f03ab83772bbfad96e40bbda14e8ca0feff31bbe05464a6ba7002a4d54d66e`  
		Last Modified: Fri, 26 Jul 2024 18:21:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:4a0dce3b2be75ceea666d931cd7c9e7337878ec3a7987bce0841e20882d5ff1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180300078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3dd8c6f8a13e8f5260176e6307d7426a441f3fbe551133c4ad057be5b75b4b`
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
# Mon, 22 Jul 2024 23:29:18 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Mon, 22 Jul 2024 23:29:18 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Mon, 22 Jul 2024 23:29:24 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Mon, 22 Jul 2024 23:29:24 GMT
ARG LPM_VERSION=0.2.7
# Mon, 22 Jul 2024 23:29:24 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Mon, 22 Jul 2024 23:29:24 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Mon, 22 Jul 2024 23:29:26 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Mon, 22 Jul 2024 23:29:26 GMT
ENV LIQUIBASE_HOME=/liquibase
# Mon, 22 Jul 2024 23:29:26 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Mon, 22 Jul 2024 23:29:26 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Mon, 22 Jul 2024 23:29:27 GMT
USER liquibase:liquibase
# Mon, 22 Jul 2024 23:29:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:29:27 GMT
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
	-	`sha256:acd5f09d06327ce421b26e9c1083497e48c24c64724c15ce2d636de06d86fd12`  
		Last Modified: Mon, 22 Jul 2024 23:29:43 GMT  
		Size: 108.2 MB (108175804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f8eb014ccc992c91b4b4f0ac0cf4372a66d07bd3b8ea0ec79fd7bb095adb09`  
		Last Modified: Mon, 22 Jul 2024 23:29:40 GMT  
		Size: 5.8 MB (5759696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b405201e43be78e5b8b368ce11b5d272df8551cc280ed6899ae9f1dc9618d3c0`  
		Last Modified: Mon, 22 Jul 2024 23:29:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9d3d1e8b38b5761ba9e3dcf415d9be21582b331b8bc7945a70d4a5dd5747bb`  
		Last Modified: Mon, 22 Jul 2024 23:29:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:3d13480a0fe11b90bf874ae492a1d0e36a376010d66d073f7ffedf65b30bd92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:06f486859f565953444595e870c025fc91fe8533b9f998e85e7171ea6e157e90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256424798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01955e3f38f46103205a8a6410649b5a5654e485e6abe5a24d41dddc35ac3eb4`
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
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LIQUIBASE_VERSION=4.29.0
# Fri, 26 Jul 2024 18:20:01 GMT
ARG LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0
# Fri, 26 Jul 2024 18:20:09 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_VERSION=0.2.7
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 26 Jul 2024 18:20:10 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 26 Jul 2024 18:20:19 GMT
# ARGS: LB_SHA256=0883b4975fc2f0a2f0180614cb156cea3c453057e6ec185c01550ec67030d8d0 LIQUIBASE_VERSION=4.29.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 26 Jul 2024 18:20:20 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 26 Jul 2024 18:20:20 GMT
USER liquibase:liquibase
# Fri, 26 Jul 2024 18:20:20 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 26 Jul 2024 18:20:20 GMT
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
	-	`sha256:b4fab9c8bd4b694093594bf93ae3a6aa471b63aaa9abb6866a265590f2a5c332`  
		Last Modified: Fri, 26 Jul 2024 18:20:56 GMT  
		Size: 159.4 MB (159372694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358763244c79133d9d1fda0a36ee34c9ee9549707a949f17367e56388b422e5f`  
		Last Modified: Fri, 26 Jul 2024 18:20:50 GMT  
		Size: 6.5 MB (6456480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d469f2a46400f1606700e55ba0c42cc79faca7d4f069b83c23fd7514302517f4`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b06df65429398af55e95d4c26c38f400d045f5e1c6e872493ca304251b3cd`  
		Last Modified: Fri, 26 Jul 2024 18:20:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:86781af9412f660d4706abd627e0310d7a86f58a906fd2e780e9dcf75214f9d6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202189398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d152c6ba327dfdd89f5f2db348884d12861d1645e2c73e28bd86aaaddf0fac0`
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
# Thu, 25 Jul 2024 18:11:29 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 25 Jul 2024 18:11:29 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 25 Jul 2024 18:11:34 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 25 Jul 2024 18:11:34 GMT
ARG LPM_VERSION=0.2.7
# Thu, 25 Jul 2024 18:11:34 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Thu, 25 Jul 2024 18:11:34 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Thu, 25 Jul 2024 18:12:07 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 25 Jul 2024 18:12:07 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 25 Jul 2024 18:12:07 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 25 Jul 2024 18:12:07 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 25 Jul 2024 18:12:07 GMT
USER liquibase:liquibase
# Thu, 25 Jul 2024 18:12:07 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 25 Jul 2024 18:12:07 GMT
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
	-	`sha256:73cab91b18aa614c7546a3333b54cd22d844b3f649da9bbdb587cc2d10a9df25`  
		Last Modified: Thu, 25 Jul 2024 18:12:28 GMT  
		Size: 108.2 MB (108154403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1be431834a5b8a29949257991d0ec3141235daee5116d7030b4e75a26d94e62`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 6.1 MB (6070003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b1f65ebbf7dfcc024aa88f6b6da444f31188cd10c5f560c3dcde92a4baee7`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0e728a5ba6831c5c180e05656ef00539d47e3efdf9eb93a8fa5a91503fa47e`  
		Last Modified: Thu, 25 Jul 2024 18:12:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
