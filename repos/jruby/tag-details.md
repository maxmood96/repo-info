<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jruby`

-	[`jruby:9`](#jruby9)
-	[`jruby:9-jdk`](#jruby9-jdk)
-	[`jruby:9-jdk8`](#jruby9-jdk8)
-	[`jruby:9.3`](#jruby93)
-	[`jruby:9.3-jdk`](#jruby93-jdk)
-	[`jruby:9.3-jdk11`](#jruby93-jdk11)
-	[`jruby:9.3-jdk17`](#jruby93-jdk17)
-	[`jruby:9.3-jdk8`](#jruby93-jdk8)
-	[`jruby:9.3-jre`](#jruby93-jre)
-	[`jruby:9.3-jre11`](#jruby93-jre11)
-	[`jruby:9.3-jre8`](#jruby93-jre8)
-	[`jruby:9.3.10`](#jruby9310)
-	[`jruby:9.3.10-jdk`](#jruby9310-jdk)
-	[`jruby:9.3.10-jdk11`](#jruby9310-jdk11)
-	[`jruby:9.3.10-jdk17`](#jruby9310-jdk17)
-	[`jruby:9.3.10-jdk8`](#jruby9310-jdk8)
-	[`jruby:9.3.10-jre`](#jruby9310-jre)
-	[`jruby:9.3.10-jre11`](#jruby9310-jre11)
-	[`jruby:9.3.10-jre8`](#jruby9310-jre8)
-	[`jruby:9.3.10.0`](#jruby93100)
-	[`jruby:9.3.10.0-jdk`](#jruby93100-jdk)
-	[`jruby:9.3.10.0-jdk11`](#jruby93100-jdk11)
-	[`jruby:9.3.10.0-jdk17`](#jruby93100-jdk17)
-	[`jruby:9.3.10.0-jdk8`](#jruby93100-jdk8)
-	[`jruby:9.3.10.0-jre`](#jruby93100-jre)
-	[`jruby:9.3.10.0-jre11`](#jruby93100-jre11)
-	[`jruby:9.3.10.0-jre8`](#jruby93100-jre8)
-	[`jruby:9.4`](#jruby94)
-	[`jruby:9.4-jdk`](#jruby94-jdk)
-	[`jruby:9.4-jdk11`](#jruby94-jdk11)
-	[`jruby:9.4-jdk17`](#jruby94-jdk17)
-	[`jruby:9.4-jdk8`](#jruby94-jdk8)
-	[`jruby:9.4-jre`](#jruby94-jre)
-	[`jruby:9.4-jre11`](#jruby94-jre11)
-	[`jruby:9.4-jre8`](#jruby94-jre8)
-	[`jruby:9.4.2`](#jruby942)
-	[`jruby:9.4.2-jdk`](#jruby942-jdk)
-	[`jruby:9.4.2-jdk11`](#jruby942-jdk11)
-	[`jruby:9.4.2-jdk17`](#jruby942-jdk17)
-	[`jruby:9.4.2-jdk8`](#jruby942-jdk8)
-	[`jruby:9.4.2-jre`](#jruby942-jre)
-	[`jruby:9.4.2-jre11`](#jruby942-jre11)
-	[`jruby:9.4.2-jre8`](#jruby942-jre8)
-	[`jruby:9.4.2.0`](#jruby9420)
-	[`jruby:9.4.2.0-jdk`](#jruby9420-jdk)
-	[`jruby:9.4.2.0-jdk11`](#jruby9420-jdk11)
-	[`jruby:9.4.2.0-jdk17`](#jruby9420-jdk17)
-	[`jruby:9.4.2.0-jdk8`](#jruby9420-jdk8)
-	[`jruby:9.4.2.0-jre`](#jruby9420-jre)
-	[`jruby:9.4.2.0-jre11`](#jruby9420-jre11)
-	[`jruby:9.4.2.0-jre8`](#jruby9420-jre8)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:8036666551cc4d91c7fa6b05d6059e30688c9d88b406ebf00a53152f7195f3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:1093c548fb1011cf24a81fd0ebe6b76d32b734ec88f1232f35a92137d0be287d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124429123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6d70119a0eb571b1bac667c0532ebe3fe278960902a8a59b67480c6b5ce17`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:29 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:37:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:37:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:37:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548519484b88477ab772a04bf9296e5d0e17fa5e97d0196ac81da68ed6477711`  
		Last Modified: Thu, 02 Mar 2023 09:41:15 GMT  
		Size: 29.5 MB (29520286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caeab7eb36ce42db49c9c8fa704fa5038a2a26177c589b22c7e20a878070966`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9544fae45a355b43c980e67e5763dc8730b12b885c7d41f99819ef8009059ef9`  
		Last Modified: Thu, 02 Mar 2023 09:41:13 GMT  
		Size: 1.1 MB (1095410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1ad41c22b626703a2c077f7e0414fead462195f572d72d6ad560ba6f486a9`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc355b60755824c38ca982f61a9f9cea34abf0e01766043f74579a0fab217cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e90de4d2847f48db1cdf86f8c5def1dd0ee8b770a40c5dcc3cdf1e0d2896735`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:05 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:06 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb95aed0bfff6ec7ea0874f0d35d6b05d913ff83175c2dc91ddbd3701d2460`  
		Last Modified: Thu, 02 Mar 2023 06:38:13 GMT  
		Size: 29.5 MB (29520125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1045ee4c980fb26c9507b6a0db37a6502d73802c2886ee70d2f69cff8a4d7e`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8892c6242c9a22ff7c2a3fc7fde5ec03f73a6f5f6db4ecc43711c01c45796`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 1.1 MB (1095355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dca95b6390402db17d2d849d8075cca2bf20bd9a8cc546874434059343b83f`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:485be14201a8a78791e5a89a620a4d2f8bc426d996c0b18c52cc362a33d40f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:10283ce3a21d5d8fe8d3fac6bf0e5d231fce39d634075e1271e7693269f6c39f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa763fb855a6e8a9c9d7db8f4ec8afacfb6d221ba9272b5dbb64d3121e238677`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:53 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:53 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:54 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:01 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b91d996b70d9d4d79336b4731dcb1b03cf663431c1ba08aa0c1392f36fcd3`  
		Last Modified: Thu, 02 Mar 2023 09:41:45 GMT  
		Size: 29.5 MB (29520214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5cb261cb0df0f6c7d056331e8bdb11042a382a699d93986ada8c5db9ae51b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af712ebf0a46fc5ca442112c7485321cbd344c305901ef0ff4956441ca94033`  
		Last Modified: Thu, 02 Mar 2023 09:41:43 GMT  
		Size: 1.1 MB (1095403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4402fe683a8d4cb0ac1361aa318c59891cdf1a30ba92a7f97cd2810f51460b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a643267990dfc4fa3d6c6ac998631b498331c914e9e766be58a78ef739566244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133784615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56102a9c77c8534d5f991f2462a7eb13c855bb14c11a441c7d728212db39fe9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:24 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:25 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:32 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:33 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a9e4e1062122c129268252b18e0ebf269641b9d8c8b93a4ad5843bd0646213`  
		Last Modified: Thu, 02 Mar 2023 06:38:44 GMT  
		Size: 29.5 MB (29520183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0a539f55165554ed9eecdfd0b0487bd89843161473e3ede72d36546137b72`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c088b8a51cb50e666767a2f7ca665b585661457fed07e7ac4a437b76f224b5`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 1.1 MB (1095359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be010112239a7b7b41dcb28798cf70fff82abaff20479c3e72654d44b7f216`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:485be14201a8a78791e5a89a620a4d2f8bc426d996c0b18c52cc362a33d40f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:10283ce3a21d5d8fe8d3fac6bf0e5d231fce39d634075e1271e7693269f6c39f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa763fb855a6e8a9c9d7db8f4ec8afacfb6d221ba9272b5dbb64d3121e238677`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:53 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:53 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:54 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:01 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b91d996b70d9d4d79336b4731dcb1b03cf663431c1ba08aa0c1392f36fcd3`  
		Last Modified: Thu, 02 Mar 2023 09:41:45 GMT  
		Size: 29.5 MB (29520214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5cb261cb0df0f6c7d056331e8bdb11042a382a699d93986ada8c5db9ae51b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af712ebf0a46fc5ca442112c7485321cbd344c305901ef0ff4956441ca94033`  
		Last Modified: Thu, 02 Mar 2023 09:41:43 GMT  
		Size: 1.1 MB (1095403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4402fe683a8d4cb0ac1361aa318c59891cdf1a30ba92a7f97cd2810f51460b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a643267990dfc4fa3d6c6ac998631b498331c914e9e766be58a78ef739566244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133784615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56102a9c77c8534d5f991f2462a7eb13c855bb14c11a441c7d728212db39fe9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:24 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:25 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:32 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:33 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a9e4e1062122c129268252b18e0ebf269641b9d8c8b93a4ad5843bd0646213`  
		Last Modified: Thu, 02 Mar 2023 06:38:44 GMT  
		Size: 29.5 MB (29520183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0a539f55165554ed9eecdfd0b0487bd89843161473e3ede72d36546137b72`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c088b8a51cb50e666767a2f7ca665b585661457fed07e7ac4a437b76f224b5`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 1.1 MB (1095359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be010112239a7b7b41dcb28798cf70fff82abaff20479c3e72654d44b7f216`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:9c6bd10bbd98dfe80588e0d2d77aa45fb7133ce2eceefd4e04ade695396e2c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cc278e349e46f1e3498909dec32853dd872fc294a8b16fb83f2aaf02a56ade55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1130b857ee178dd750cdc4835cfa92cdf264a18525fa3b05ab68cb51035418`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:02:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:02:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:02:39 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:35 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:58 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08750c2d3224972ecc7c10d279243a4725955da232a8adb15ac3a904e3aa61`  
		Last Modified: Thu, 02 Mar 2023 04:09:00 GMT  
		Size: 198.5 MB (198486475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d001150444c8847c8c1f9fad3af64a87698edd1ddfcc14f7a59210973fd1e`  
		Last Modified: Thu, 02 Mar 2023 04:08:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad95e702f7d05b28e30951cc6878a2d4c4f0974d00e814ea677e32407fb8f5d`  
		Last Modified: Thu, 02 Mar 2023 09:42:21 GMT  
		Size: 7.1 MB (7069154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00658c6571273ac0d13bdd816a081094d020099915e3c9037ba76a8b4347f3d1`  
		Last Modified: Thu, 02 Mar 2023 09:43:45 GMT  
		Size: 28.9 MB (28854054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353bed634b72595b734128083f702053c8295284db5f94b59b86ccda16cda89e`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2e99993114451dee43d5a042e6c7da1a07ba0332835b8e2ea89a38090005a8`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 1.1 MB (1064688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77347300b5c112f3440fa00aed085995305fc317ce48db5636baa115266a791`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a087186aa6c35824f65b0ece036126bd098cbc1f3ee9635d763e14be4a0ac4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274603394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf662106553340791b18588db902f174d529e1a8514fd1eb698eb27a0fac3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:28:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:28:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:28:45 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:35:55 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:00 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:01 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e65b9096e205827838903d72ad8853922690c7a9810284b4914e6bff5af6e6`  
		Last Modified: Thu, 02 Mar 2023 04:34:17 GMT  
		Size: 195.2 MB (195247148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942854036061a0907d59e9cbd049833dbe188ca4b124054e58b2b90ed288c60f`  
		Last Modified: Thu, 02 Mar 2023 04:34:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1484a7e498bcc146b58f5b3909d50bb76e2c0b00e47e51d34ce272d50549e26`  
		Last Modified: Thu, 02 Mar 2023 06:39:20 GMT  
		Size: 6.0 MB (6032219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b39eddf3bcbcd12a6e318cf0352687d4462ef288d432b2548fe14953cfee7b4`  
		Last Modified: Thu, 02 Mar 2023 06:40:45 GMT  
		Size: 28.9 MB (28854307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa00658fe93dd3aa2e96fa61a582dbc716b2f8baabc69733cb6c54fc108bfd3`  
		Last Modified: Thu, 02 Mar 2023 06:40:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440c216a9613b73d5e04d9d7437ed54ee5056d18ddba23b903b027145ca1b7a7`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 1.1 MB (1064622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c26d6dff30b0e7b59c5a22d12286b6297138f2f2a363c9daee7871d72e90ab`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:ad7f21811a96b82f336a364d59dff90ef3ce30e85e7b2ce43adf50a8f99eb367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:a00439cce140c9aacec057075b6440be25f5d9a90a0c9bba2b9eb72061450d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278108939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87052bdfcf97173632c8bf690dce670f3002f1bc47ea4b7dc3b1d7edcf81ac28`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:03:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:03:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:59 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:40:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:40:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:13 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2548829404a24408e385f432f5dcf1364d2d027a631388b2d7ffae095912d57e`  
		Last Modified: Thu, 02 Mar 2023 04:10:27 GMT  
		Size: 192.4 MB (192448038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648deea0f1d95f4a147cd47f868801085ae5652e54f9bec42b292fed0db4c11`  
		Last Modified: Thu, 02 Mar 2023 04:10:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a43766f7bf1125162ccce1cf6b2fd16ae3cda644c8f901274952a4a1aa11ac6`  
		Last Modified: Thu, 02 Mar 2023 09:42:34 GMT  
		Size: 7.1 MB (7071395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a936ec76a8f8b02fd0d603c1174cef164fc48234ad7ece060c2da840fa36664`  
		Last Modified: Thu, 02 Mar 2023 09:43:58 GMT  
		Size: 28.9 MB (28854345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d0b594499b6789547f4983ba61bc48846dc855c25ce5614fb4ffe245d44ba7`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9af204af49c4dacb053864b92dd75899366da21f6b7530b530c2838a39042b`  
		Last Modified: Thu, 02 Mar 2023 09:43:56 GMT  
		Size: 1.1 MB (1064660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a42c8c1387821febd9c354c206c758c72d9c867e478677fc59d50d5aea2e45`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:386e0c79e4957be90f868f27561aa0e795ed2f39708c4983898d7c2eec851113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275225570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b796a59f91473c5db071f53aad87c4a127833300fcd8aee2834c76e5729fe4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:29:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:29:35 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:29:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:29:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:36:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30249df1bda77f2171b754e4a76ef4c05cb50a40a6247b44ec30f654b9e5db4f`  
		Last Modified: Thu, 02 Mar 2023 04:35:24 GMT  
		Size: 20.8 MB (20810122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d009541900c02211c26f800cc060dd6862ccf839b4b3de0c58fa79004e52347`  
		Last Modified: Thu, 02 Mar 2023 04:35:32 GMT  
		Size: 191.3 MB (191267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb21286d602781c3885407902a84537861b872a08408b28ff832fbe0e31b3ad`  
		Last Modified: Thu, 02 Mar 2023 04:35:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c066c3b9e2adec7e9bca1bf2506f50fe954adc20fad465c4dac454064b37fb`  
		Last Modified: Thu, 02 Mar 2023 06:39:33 GMT  
		Size: 6.0 MB (6034293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2476f2399dd10629eec6c4ea974067e569cbb91eac82f179900d28e742ce6c06`  
		Last Modified: Thu, 02 Mar 2023 06:40:58 GMT  
		Size: 28.9 MB (28854319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110a1e232b241b2c882933bd8d0a9e568e82c5003d9db963c48cf2fef72d2ee`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486be8d8c2fa673f1f8a64f7e59fa99cad7bb7b041bae79ae4ba49d3b9f7bc17`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 1.1 MB (1064631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d38ca26f56e2f2ef97a5f5e81fb3bb57d04442c7ca753274ac63a9fedebb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:402097dd9ac0f60628e4296ef1f2242d130e630bcf14dcf5de31f3745b0385cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:f5aa7fd1f175fbd55b2fe3144919ef1ba15e846ea162b76cfc70fe5ecc5c3478
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128540434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be64a602b248cb233fb42cd77787d7903f70ee87e5fce5db5127b07af97e47f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 09:38:11 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:41 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:42 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b665fdae859de8574371cb2dbbec0e1104edf8327f0a48aa0d42dc7156361f`  
		Last Modified: Thu, 02 Mar 2023 09:42:08 GMT  
		Size: 7.1 MB (7069117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1f9a5c4c7c4001bad6627ec376cf2c8e53120b1a4fb4f1c531a44b5a0af25a`  
		Last Modified: Thu, 02 Mar 2023 09:43:32 GMT  
		Size: 28.9 MB (28854356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fab424e63f8bf4d6c8128354b5771922d4683358749e8f9d932a4fea9e25ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a7781c1d7b257158ce70133a02b25cbaf8a2b32dd103e4a0ef38981ed12ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:31 GMT  
		Size: 1.1 MB (1064638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06229ad992c76165c3203e197d38bd1b715b0300f1194e0193b1e77cb60ff95`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bba87e5670d5c6955a1969100c7f7e06149ab1c8206745c720af1ebf2b92e56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124335566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e16d9710ed1d8e0b390f285f3369cc6e05dd8fba9e2b2d10668b0e7e822323`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:29:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 06:35:39 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:49 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b550e0153d6633dc59f3ed4f76afd8953d647dfc2d7c7ead4e51d8b2841a143a`  
		Last Modified: Thu, 02 Mar 2023 04:34:58 GMT  
		Size: 45.0 MB (44979643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d760d96418bc955ac7bfd4587f53a1c25a45a19f8748622e538d3b1c79efe`  
		Last Modified: Thu, 02 Mar 2023 04:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c05cfc887522c4779b088b17d01ebb4b48a5c38f6e4e21148dd3f0d421d0dd`  
		Last Modified: Thu, 02 Mar 2023 06:39:07 GMT  
		Size: 6.0 MB (6032209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf6b88cc50dde4bb838f60f21e4c4e83511f412440f52284b148b70944bc86`  
		Last Modified: Thu, 02 Mar 2023 06:40:32 GMT  
		Size: 28.9 MB (28853975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4583377e4265e7d52aadc78ec72b19dba16da03ea43ff490a27e96f862367f`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e230247f7946d13dd5381063b837a8a96694ebc9959632e96826fd30d315e16`  
		Last Modified: Thu, 02 Mar 2023 06:40:31 GMT  
		Size: 1.1 MB (1064657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ef86f3b358ea79f61be0307075705d8abdafa2dccee77ee8f404fff6222e09`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk11`

```console
$ docker pull jruby@sha256:9c6bd10bbd98dfe80588e0d2d77aa45fb7133ce2eceefd4e04ade695396e2c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cc278e349e46f1e3498909dec32853dd872fc294a8b16fb83f2aaf02a56ade55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1130b857ee178dd750cdc4835cfa92cdf264a18525fa3b05ab68cb51035418`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:02:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:02:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:02:39 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:35 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:58 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08750c2d3224972ecc7c10d279243a4725955da232a8adb15ac3a904e3aa61`  
		Last Modified: Thu, 02 Mar 2023 04:09:00 GMT  
		Size: 198.5 MB (198486475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d001150444c8847c8c1f9fad3af64a87698edd1ddfcc14f7a59210973fd1e`  
		Last Modified: Thu, 02 Mar 2023 04:08:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad95e702f7d05b28e30951cc6878a2d4c4f0974d00e814ea677e32407fb8f5d`  
		Last Modified: Thu, 02 Mar 2023 09:42:21 GMT  
		Size: 7.1 MB (7069154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00658c6571273ac0d13bdd816a081094d020099915e3c9037ba76a8b4347f3d1`  
		Last Modified: Thu, 02 Mar 2023 09:43:45 GMT  
		Size: 28.9 MB (28854054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353bed634b72595b734128083f702053c8295284db5f94b59b86ccda16cda89e`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2e99993114451dee43d5a042e6c7da1a07ba0332835b8e2ea89a38090005a8`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 1.1 MB (1064688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77347300b5c112f3440fa00aed085995305fc317ce48db5636baa115266a791`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a087186aa6c35824f65b0ece036126bd098cbc1f3ee9635d763e14be4a0ac4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274603394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf662106553340791b18588db902f174d529e1a8514fd1eb698eb27a0fac3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:28:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:28:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:28:45 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:35:55 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:00 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:01 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e65b9096e205827838903d72ad8853922690c7a9810284b4914e6bff5af6e6`  
		Last Modified: Thu, 02 Mar 2023 04:34:17 GMT  
		Size: 195.2 MB (195247148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942854036061a0907d59e9cbd049833dbe188ca4b124054e58b2b90ed288c60f`  
		Last Modified: Thu, 02 Mar 2023 04:34:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1484a7e498bcc146b58f5b3909d50bb76e2c0b00e47e51d34ce272d50549e26`  
		Last Modified: Thu, 02 Mar 2023 06:39:20 GMT  
		Size: 6.0 MB (6032219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b39eddf3bcbcd12a6e318cf0352687d4462ef288d432b2548fe14953cfee7b4`  
		Last Modified: Thu, 02 Mar 2023 06:40:45 GMT  
		Size: 28.9 MB (28854307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa00658fe93dd3aa2e96fa61a582dbc716b2f8baabc69733cb6c54fc108bfd3`  
		Last Modified: Thu, 02 Mar 2023 06:40:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440c216a9613b73d5e04d9d7437ed54ee5056d18ddba23b903b027145ca1b7a7`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 1.1 MB (1064622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c26d6dff30b0e7b59c5a22d12286b6297138f2f2a363c9daee7871d72e90ab`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk17`

```console
$ docker pull jruby@sha256:ad7f21811a96b82f336a364d59dff90ef3ce30e85e7b2ce43adf50a8f99eb367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:a00439cce140c9aacec057075b6440be25f5d9a90a0c9bba2b9eb72061450d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278108939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87052bdfcf97173632c8bf690dce670f3002f1bc47ea4b7dc3b1d7edcf81ac28`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:03:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:03:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:59 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:40:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:40:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:13 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2548829404a24408e385f432f5dcf1364d2d027a631388b2d7ffae095912d57e`  
		Last Modified: Thu, 02 Mar 2023 04:10:27 GMT  
		Size: 192.4 MB (192448038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648deea0f1d95f4a147cd47f868801085ae5652e54f9bec42b292fed0db4c11`  
		Last Modified: Thu, 02 Mar 2023 04:10:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a43766f7bf1125162ccce1cf6b2fd16ae3cda644c8f901274952a4a1aa11ac6`  
		Last Modified: Thu, 02 Mar 2023 09:42:34 GMT  
		Size: 7.1 MB (7071395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a936ec76a8f8b02fd0d603c1174cef164fc48234ad7ece060c2da840fa36664`  
		Last Modified: Thu, 02 Mar 2023 09:43:58 GMT  
		Size: 28.9 MB (28854345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d0b594499b6789547f4983ba61bc48846dc855c25ce5614fb4ffe245d44ba7`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9af204af49c4dacb053864b92dd75899366da21f6b7530b530c2838a39042b`  
		Last Modified: Thu, 02 Mar 2023 09:43:56 GMT  
		Size: 1.1 MB (1064660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a42c8c1387821febd9c354c206c758c72d9c867e478677fc59d50d5aea2e45`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:386e0c79e4957be90f868f27561aa0e795ed2f39708c4983898d7c2eec851113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275225570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b796a59f91473c5db071f53aad87c4a127833300fcd8aee2834c76e5729fe4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:29:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:29:35 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:29:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:29:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:36:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30249df1bda77f2171b754e4a76ef4c05cb50a40a6247b44ec30f654b9e5db4f`  
		Last Modified: Thu, 02 Mar 2023 04:35:24 GMT  
		Size: 20.8 MB (20810122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d009541900c02211c26f800cc060dd6862ccf839b4b3de0c58fa79004e52347`  
		Last Modified: Thu, 02 Mar 2023 04:35:32 GMT  
		Size: 191.3 MB (191267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb21286d602781c3885407902a84537861b872a08408b28ff832fbe0e31b3ad`  
		Last Modified: Thu, 02 Mar 2023 04:35:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c066c3b9e2adec7e9bca1bf2506f50fe954adc20fad465c4dac454064b37fb`  
		Last Modified: Thu, 02 Mar 2023 06:39:33 GMT  
		Size: 6.0 MB (6034293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2476f2399dd10629eec6c4ea974067e569cbb91eac82f179900d28e742ce6c06`  
		Last Modified: Thu, 02 Mar 2023 06:40:58 GMT  
		Size: 28.9 MB (28854319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110a1e232b241b2c882933bd8d0a9e568e82c5003d9db963c48cf2fef72d2ee`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486be8d8c2fa673f1f8a64f7e59fa99cad7bb7b041bae79ae4ba49d3b9f7bc17`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 1.1 MB (1064631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d38ca26f56e2f2ef97a5f5e81fb3bb57d04442c7ca753274ac63a9fedebb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk8`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre11`

```console
$ docker pull jruby@sha256:402097dd9ac0f60628e4296ef1f2242d130e630bcf14dcf5de31f3745b0385cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:f5aa7fd1f175fbd55b2fe3144919ef1ba15e846ea162b76cfc70fe5ecc5c3478
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128540434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be64a602b248cb233fb42cd77787d7903f70ee87e5fce5db5127b07af97e47f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 09:38:11 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:41 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:42 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b665fdae859de8574371cb2dbbec0e1104edf8327f0a48aa0d42dc7156361f`  
		Last Modified: Thu, 02 Mar 2023 09:42:08 GMT  
		Size: 7.1 MB (7069117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1f9a5c4c7c4001bad6627ec376cf2c8e53120b1a4fb4f1c531a44b5a0af25a`  
		Last Modified: Thu, 02 Mar 2023 09:43:32 GMT  
		Size: 28.9 MB (28854356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fab424e63f8bf4d6c8128354b5771922d4683358749e8f9d932a4fea9e25ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a7781c1d7b257158ce70133a02b25cbaf8a2b32dd103e4a0ef38981ed12ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:31 GMT  
		Size: 1.1 MB (1064638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06229ad992c76165c3203e197d38bd1b715b0300f1194e0193b1e77cb60ff95`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bba87e5670d5c6955a1969100c7f7e06149ab1c8206745c720af1ebf2b92e56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124335566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e16d9710ed1d8e0b390f285f3369cc6e05dd8fba9e2b2d10668b0e7e822323`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:29:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 06:35:39 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:49 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b550e0153d6633dc59f3ed4f76afd8953d647dfc2d7c7ead4e51d8b2841a143a`  
		Last Modified: Thu, 02 Mar 2023 04:34:58 GMT  
		Size: 45.0 MB (44979643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d760d96418bc955ac7bfd4587f53a1c25a45a19f8748622e538d3b1c79efe`  
		Last Modified: Thu, 02 Mar 2023 04:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c05cfc887522c4779b088b17d01ebb4b48a5c38f6e4e21148dd3f0d421d0dd`  
		Last Modified: Thu, 02 Mar 2023 06:39:07 GMT  
		Size: 6.0 MB (6032209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf6b88cc50dde4bb838f60f21e4c4e83511f412440f52284b148b70944bc86`  
		Last Modified: Thu, 02 Mar 2023 06:40:32 GMT  
		Size: 28.9 MB (28853975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4583377e4265e7d52aadc78ec72b19dba16da03ea43ff490a27e96f862367f`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e230247f7946d13dd5381063b837a8a96694ebc9959632e96826fd30d315e16`  
		Last Modified: Thu, 02 Mar 2023 06:40:31 GMT  
		Size: 1.1 MB (1064657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ef86f3b358ea79f61be0307075705d8abdafa2dccee77ee8f404fff6222e09`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre8`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk11`

```console
$ docker pull jruby@sha256:9c6bd10bbd98dfe80588e0d2d77aa45fb7133ce2eceefd4e04ade695396e2c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cc278e349e46f1e3498909dec32853dd872fc294a8b16fb83f2aaf02a56ade55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1130b857ee178dd750cdc4835cfa92cdf264a18525fa3b05ab68cb51035418`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:02:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:02:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:02:39 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:35 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:56 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:58 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:07 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08750c2d3224972ecc7c10d279243a4725955da232a8adb15ac3a904e3aa61`  
		Last Modified: Thu, 02 Mar 2023 04:09:00 GMT  
		Size: 198.5 MB (198486475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d001150444c8847c8c1f9fad3af64a87698edd1ddfcc14f7a59210973fd1e`  
		Last Modified: Thu, 02 Mar 2023 04:08:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad95e702f7d05b28e30951cc6878a2d4c4f0974d00e814ea677e32407fb8f5d`  
		Last Modified: Thu, 02 Mar 2023 09:42:21 GMT  
		Size: 7.1 MB (7069154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00658c6571273ac0d13bdd816a081094d020099915e3c9037ba76a8b4347f3d1`  
		Last Modified: Thu, 02 Mar 2023 09:43:45 GMT  
		Size: 28.9 MB (28854054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353bed634b72595b734128083f702053c8295284db5f94b59b86ccda16cda89e`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2e99993114451dee43d5a042e6c7da1a07ba0332835b8e2ea89a38090005a8`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 1.1 MB (1064688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77347300b5c112f3440fa00aed085995305fc317ce48db5636baa115266a791`  
		Last Modified: Thu, 02 Mar 2023 09:43:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a087186aa6c35824f65b0ece036126bd098cbc1f3ee9635d763e14be4a0ac4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274603394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf662106553340791b18588db902f174d529e1a8514fd1eb698eb27a0fac3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:28:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:28:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:28:45 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:35:55 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:59 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:00 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:01 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e65b9096e205827838903d72ad8853922690c7a9810284b4914e6bff5af6e6`  
		Last Modified: Thu, 02 Mar 2023 04:34:17 GMT  
		Size: 195.2 MB (195247148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942854036061a0907d59e9cbd049833dbe188ca4b124054e58b2b90ed288c60f`  
		Last Modified: Thu, 02 Mar 2023 04:34:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1484a7e498bcc146b58f5b3909d50bb76e2c0b00e47e51d34ce272d50549e26`  
		Last Modified: Thu, 02 Mar 2023 06:39:20 GMT  
		Size: 6.0 MB (6032219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b39eddf3bcbcd12a6e318cf0352687d4462ef288d432b2548fe14953cfee7b4`  
		Last Modified: Thu, 02 Mar 2023 06:40:45 GMT  
		Size: 28.9 MB (28854307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa00658fe93dd3aa2e96fa61a582dbc716b2f8baabc69733cb6c54fc108bfd3`  
		Last Modified: Thu, 02 Mar 2023 06:40:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440c216a9613b73d5e04d9d7437ed54ee5056d18ddba23b903b027145ca1b7a7`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 1.1 MB (1064622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c26d6dff30b0e7b59c5a22d12286b6297138f2f2a363c9daee7871d72e90ab`  
		Last Modified: Thu, 02 Mar 2023 06:40:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk17`

```console
$ docker pull jruby@sha256:ad7f21811a96b82f336a364d59dff90ef3ce30e85e7b2ce43adf50a8f99eb367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:a00439cce140c9aacec057075b6440be25f5d9a90a0c9bba2b9eb72061450d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278108939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87052bdfcf97173632c8bf690dce670f3002f1bc47ea4b7dc3b1d7edcf81ac28`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:03:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:03:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:59 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:40:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:40:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:40:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:13 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:40:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:40:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:40:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2548829404a24408e385f432f5dcf1364d2d027a631388b2d7ffae095912d57e`  
		Last Modified: Thu, 02 Mar 2023 04:10:27 GMT  
		Size: 192.4 MB (192448038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648deea0f1d95f4a147cd47f868801085ae5652e54f9bec42b292fed0db4c11`  
		Last Modified: Thu, 02 Mar 2023 04:10:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a43766f7bf1125162ccce1cf6b2fd16ae3cda644c8f901274952a4a1aa11ac6`  
		Last Modified: Thu, 02 Mar 2023 09:42:34 GMT  
		Size: 7.1 MB (7071395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a936ec76a8f8b02fd0d603c1174cef164fc48234ad7ece060c2da840fa36664`  
		Last Modified: Thu, 02 Mar 2023 09:43:58 GMT  
		Size: 28.9 MB (28854345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d0b594499b6789547f4983ba61bc48846dc855c25ce5614fb4ffe245d44ba7`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9af204af49c4dacb053864b92dd75899366da21f6b7530b530c2838a39042b`  
		Last Modified: Thu, 02 Mar 2023 09:43:56 GMT  
		Size: 1.1 MB (1064660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a42c8c1387821febd9c354c206c758c72d9c867e478677fc59d50d5aea2e45`  
		Last Modified: Thu, 02 Mar 2023 09:43:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:386e0c79e4957be90f868f27561aa0e795ed2f39708c4983898d7c2eec851113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275225570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b796a59f91473c5db071f53aad87c4a127833300fcd8aee2834c76e5729fe4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:29:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:29:35 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:29:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:29:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:36:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:37:10 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:37:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:37:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:37:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:37:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:37:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:37:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30249df1bda77f2171b754e4a76ef4c05cb50a40a6247b44ec30f654b9e5db4f`  
		Last Modified: Thu, 02 Mar 2023 04:35:24 GMT  
		Size: 20.8 MB (20810122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d009541900c02211c26f800cc060dd6862ccf839b4b3de0c58fa79004e52347`  
		Last Modified: Thu, 02 Mar 2023 04:35:32 GMT  
		Size: 191.3 MB (191267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb21286d602781c3885407902a84537861b872a08408b28ff832fbe0e31b3ad`  
		Last Modified: Thu, 02 Mar 2023 04:35:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c066c3b9e2adec7e9bca1bf2506f50fe954adc20fad465c4dac454064b37fb`  
		Last Modified: Thu, 02 Mar 2023 06:39:33 GMT  
		Size: 6.0 MB (6034293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2476f2399dd10629eec6c4ea974067e569cbb91eac82f179900d28e742ce6c06`  
		Last Modified: Thu, 02 Mar 2023 06:40:58 GMT  
		Size: 28.9 MB (28854319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110a1e232b241b2c882933bd8d0a9e568e82c5003d9db963c48cf2fef72d2ee`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486be8d8c2fa673f1f8a64f7e59fa99cad7bb7b041bae79ae4ba49d3b9f7bc17`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 1.1 MB (1064631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d38ca26f56e2f2ef97a5f5e81fb3bb57d04442c7ca753274ac63a9fedebb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk8`

```console
$ docker pull jruby@sha256:dfcf62a35362b122ec8d988fbf83c2d514741bbccd677ebea1a1d4d8c6614311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4eda4b7498363f0bed2c64f2bdb3a6d7237cbd87b062cc7e738906a93002fc27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136543977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16aeded2f8e00bb5f58988e5eb3aacfb6b2f16e0f4822b3c87c91752d16fef7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:27 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:30 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb317bbc38ae85844b9c127e59277840fb003c3d8227f151cabf8f4c23bbde6`  
		Last Modified: Thu, 02 Mar 2023 09:43:14 GMT  
		Size: 28.9 MB (28854349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0a207aa594e2de6c7e083e52f33fe7cc82fe94bbe3bb8218a26f6a7625875`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d83d213d743c249c81dd61d12375c94c25d5966915edb81a21ee6bf3d485c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 1.1 MB (1064669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bbc33e02141ccb1de04d1d88ae58906c3a95019f744be197da9664b000923c`  
		Last Modified: Thu, 02 Mar 2023 09:43:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:39ca4d423d4ddd56dff6775ab6a9c9a6f4ac7f37e059696c1652359fe17ac33f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133088071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15407eb6255efa34aaae90b268388a9a6d07c41a9a8b54e45dbddb7abc1f1656`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:36 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:45 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b66c6e7260455842e049b5d4f349fa81371a76c0574e102fc36e54b9dc1fb7`  
		Last Modified: Thu, 02 Mar 2023 06:40:13 GMT  
		Size: 28.9 MB (28854343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3a7be06374c5255dd40a483dc43ee5c131a1ee815392b5f222698f8498662`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b53e8c692043b2daf1e65ffa4cb95c63fd503e901a9e39bcef387a6de5715`  
		Last Modified: Thu, 02 Mar 2023 06:40:12 GMT  
		Size: 1.1 MB (1064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb740500be0672f7dd8947cc047eabb1edaa9269c9e708d6ead901199b2779`  
		Last Modified: Thu, 02 Mar 2023 06:40:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre11`

```console
$ docker pull jruby@sha256:402097dd9ac0f60628e4296ef1f2242d130e630bcf14dcf5de31f3745b0385cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:f5aa7fd1f175fbd55b2fe3144919ef1ba15e846ea162b76cfc70fe5ecc5c3478
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128540434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be64a602b248cb233fb42cd77787d7903f70ee87e5fce5db5127b07af97e47f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 09:38:11 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:41 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:42 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:52 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b665fdae859de8574371cb2dbbec0e1104edf8327f0a48aa0d42dc7156361f`  
		Last Modified: Thu, 02 Mar 2023 09:42:08 GMT  
		Size: 7.1 MB (7069117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1f9a5c4c7c4001bad6627ec376cf2c8e53120b1a4fb4f1c531a44b5a0af25a`  
		Last Modified: Thu, 02 Mar 2023 09:43:32 GMT  
		Size: 28.9 MB (28854356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fab424e63f8bf4d6c8128354b5771922d4683358749e8f9d932a4fea9e25ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a7781c1d7b257158ce70133a02b25cbaf8a2b32dd103e4a0ef38981ed12ec`  
		Last Modified: Thu, 02 Mar 2023 09:43:31 GMT  
		Size: 1.1 MB (1064638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06229ad992c76165c3203e197d38bd1b715b0300f1194e0193b1e77cb60ff95`  
		Last Modified: Thu, 02 Mar 2023 09:43:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bba87e5670d5c6955a1969100c7f7e06149ab1c8206745c720af1ebf2b92e56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124335566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e16d9710ed1d8e0b390f285f3369cc6e05dd8fba9e2b2d10668b0e7e822323`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:29:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 06:35:39 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:47 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:49 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:49 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b550e0153d6633dc59f3ed4f76afd8953d647dfc2d7c7ead4e51d8b2841a143a`  
		Last Modified: Thu, 02 Mar 2023 04:34:58 GMT  
		Size: 45.0 MB (44979643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d760d96418bc955ac7bfd4587f53a1c25a45a19f8748622e538d3b1c79efe`  
		Last Modified: Thu, 02 Mar 2023 04:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c05cfc887522c4779b088b17d01ebb4b48a5c38f6e4e21148dd3f0d421d0dd`  
		Last Modified: Thu, 02 Mar 2023 06:39:07 GMT  
		Size: 6.0 MB (6032209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf6b88cc50dde4bb838f60f21e4c4e83511f412440f52284b148b70944bc86`  
		Last Modified: Thu, 02 Mar 2023 06:40:32 GMT  
		Size: 28.9 MB (28853975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4583377e4265e7d52aadc78ec72b19dba16da03ea43ff490a27e96f862367f`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e230247f7946d13dd5381063b837a8a96694ebc9959632e96826fd30d315e16`  
		Last Modified: Thu, 02 Mar 2023 06:40:31 GMT  
		Size: 1.1 MB (1064657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ef86f3b358ea79f61be0307075705d8abdafa2dccee77ee8f404fff6222e09`  
		Last Modified: Thu, 02 Mar 2023 06:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre8`

```console
$ docker pull jruby@sha256:f935a1e30e449503ef74a19fec4bb49f60a16db96ee1829b77a6959f0102a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:099a6c78470e3b2d7e15a0977da1453cf773de5af7ee19d0e127e36abed0a605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123732440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364139da18c570ab4b2f5a999fbbdf6138ffd345d825cbc5076318ab34b7a389`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 09:39:13 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 09:39:15 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:16 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:24 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333433354cc8f5fc09bf1631e21b3aebe281cf08920d23689d3293d6937368`  
		Last Modified: Thu, 02 Mar 2023 09:42:47 GMT  
		Size: 28.9 MB (28854322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa718dc12da3e8ecfb18c0b53c1bcd5265d5ad19f7e84e3d5d4007c055f77fc`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f39f6ad12e70075814afbb7cdc77be3c854763064625b4d680688fc3516f9`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 1.1 MB (1064693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c93f043bfeeb9304747e1732d85922ec2d06ba9b108b55fbed08352921a06c`  
		Last Modified: Thu, 02 Mar 2023 09:42:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:b079271eb58fe62c510403cc54d0a765398dbf09dae9ed6c8a968beb52c07ca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120164984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a2e09e79fa063d9df8a6e8424d11776f4ce8296f7d0dcc557dd277290f77f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_VERSION=9.3.10.0
# Thu, 02 Mar 2023 06:36:24 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9f3028fb94beac9874d1421e7b62ceed4cbd20c8416ef4689476a7a00a53a`  
		Last Modified: Thu, 02 Mar 2023 06:39:48 GMT  
		Size: 28.9 MB (28854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33eaba3e58c4ab8ccaf12a4405734bccb1d93e02200e17f3dbfb2ab81c8cb7`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9137c59431f50aacef841a28ea3574735670180e5a0d5d4ed49b7319ebbec`  
		Last Modified: Thu, 02 Mar 2023 06:39:46 GMT  
		Size: 1.1 MB (1064647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fe0b5f5df8449bd0f213c3dcce8a23d35a4560425837c312244691a3da2282`  
		Last Modified: Thu, 02 Mar 2023 06:39:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4`

```console
$ docker pull jruby@sha256:8036666551cc4d91c7fa6b05d6059e30688c9d88b406ebf00a53152f7195f3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4` - linux; amd64

```console
$ docker pull jruby@sha256:1093c548fb1011cf24a81fd0ebe6b76d32b734ec88f1232f35a92137d0be287d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124429123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6d70119a0eb571b1bac667c0532ebe3fe278960902a8a59b67480c6b5ce17`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:29 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:37:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:37:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:37:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548519484b88477ab772a04bf9296e5d0e17fa5e97d0196ac81da68ed6477711`  
		Last Modified: Thu, 02 Mar 2023 09:41:15 GMT  
		Size: 29.5 MB (29520286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caeab7eb36ce42db49c9c8fa704fa5038a2a26177c589b22c7e20a878070966`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9544fae45a355b43c980e67e5763dc8730b12b885c7d41f99819ef8009059ef9`  
		Last Modified: Thu, 02 Mar 2023 09:41:13 GMT  
		Size: 1.1 MB (1095410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1ad41c22b626703a2c077f7e0414fead462195f572d72d6ad560ba6f486a9`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc355b60755824c38ca982f61a9f9cea34abf0e01766043f74579a0fab217cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e90de4d2847f48db1cdf86f8c5def1dd0ee8b770a40c5dcc3cdf1e0d2896735`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:05 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:06 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb95aed0bfff6ec7ea0874f0d35d6b05d913ff83175c2dc91ddbd3701d2460`  
		Last Modified: Thu, 02 Mar 2023 06:38:13 GMT  
		Size: 29.5 MB (29520125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1045ee4c980fb26c9507b6a0db37a6502d73802c2886ee70d2f69cff8a4d7e`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8892c6242c9a22ff7c2a3fc7fde5ec03f73a6f5f6db4ecc43711c01c45796`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 1.1 MB (1095355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dca95b6390402db17d2d849d8075cca2bf20bd9a8cc546874434059343b83f`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk`

```console
$ docker pull jruby@sha256:485be14201a8a78791e5a89a620a4d2f8bc426d996c0b18c52cc362a33d40f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:10283ce3a21d5d8fe8d3fac6bf0e5d231fce39d634075e1271e7693269f6c39f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa763fb855a6e8a9c9d7db8f4ec8afacfb6d221ba9272b5dbb64d3121e238677`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:53 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:53 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:54 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:01 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b91d996b70d9d4d79336b4731dcb1b03cf663431c1ba08aa0c1392f36fcd3`  
		Last Modified: Thu, 02 Mar 2023 09:41:45 GMT  
		Size: 29.5 MB (29520214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5cb261cb0df0f6c7d056331e8bdb11042a382a699d93986ada8c5db9ae51b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af712ebf0a46fc5ca442112c7485321cbd344c305901ef0ff4956441ca94033`  
		Last Modified: Thu, 02 Mar 2023 09:41:43 GMT  
		Size: 1.1 MB (1095403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4402fe683a8d4cb0ac1361aa318c59891cdf1a30ba92a7f97cd2810f51460b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a643267990dfc4fa3d6c6ac998631b498331c914e9e766be58a78ef739566244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133784615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56102a9c77c8534d5f991f2462a7eb13c855bb14c11a441c7d728212db39fe9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:24 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:25 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:32 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:33 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a9e4e1062122c129268252b18e0ebf269641b9d8c8b93a4ad5843bd0646213`  
		Last Modified: Thu, 02 Mar 2023 06:38:44 GMT  
		Size: 29.5 MB (29520183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0a539f55165554ed9eecdfd0b0487bd89843161473e3ede72d36546137b72`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c088b8a51cb50e666767a2f7ca665b585661457fed07e7ac4a437b76f224b5`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 1.1 MB (1095359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be010112239a7b7b41dcb28798cf70fff82abaff20479c3e72654d44b7f216`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk11`

```console
$ docker pull jruby@sha256:7abba7a8577fd2cd9201c227a568e637b8ebe6e6fe963b0297fe7e4adf8c2e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:08dd3dae81dfb9fdc9116d24fc6f6058ddd54ce0458c07f5bc6864f8d7a976b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281091334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ca36fae6a12aeb496c5b9758d758fb45231f3931fdb9341ee37ffe1db1fef4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:02:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:02:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:02:39 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:35 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:38:35 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:38:35 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:38:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:38:37 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:47 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:47 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08750c2d3224972ecc7c10d279243a4725955da232a8adb15ac3a904e3aa61`  
		Last Modified: Thu, 02 Mar 2023 04:09:00 GMT  
		Size: 198.5 MB (198486475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d001150444c8847c8c1f9fad3af64a87698edd1ddfcc14f7a59210973fd1e`  
		Last Modified: Thu, 02 Mar 2023 04:08:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad95e702f7d05b28e30951cc6878a2d4c4f0974d00e814ea677e32407fb8f5d`  
		Last Modified: Thu, 02 Mar 2023 09:42:21 GMT  
		Size: 7.1 MB (7069154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18de864977a9e02b413ce3008ad8a6783ab5b8354dd6873f1c7905136cd49dc`  
		Last Modified: Thu, 02 Mar 2023 09:42:22 GMT  
		Size: 29.5 MB (29520282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352416c69413eae74033f48b4bf53aaa0b1a5d17a4ac0b25a11322d9b7c54aaf`  
		Last Modified: Thu, 02 Mar 2023 09:42:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807c4ce40f92572dd7144d52ef17308aff1c9762b65d662bd27720329f95dcc0`  
		Last Modified: Thu, 02 Mar 2023 09:42:20 GMT  
		Size: 1.1 MB (1095361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be32194509f4da14f21f03a32e279541ee4b033918ecbc376b28655be94211ff`  
		Last Modified: Thu, 02 Mar 2023 09:42:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4735a3ccfa8f706ccb63f55a4bb248125d4ead18fcfd27ce52eb7ada9c0b8ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275300010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d3e9f50aea0844cf79ac94b56d8030fccf278224b0c31ff7c0abfa37107092`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:28:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:28:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:28:45 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:35:55 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:55 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:55 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:05 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:05 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e65b9096e205827838903d72ad8853922690c7a9810284b4914e6bff5af6e6`  
		Last Modified: Thu, 02 Mar 2023 04:34:17 GMT  
		Size: 195.2 MB (195247148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942854036061a0907d59e9cbd049833dbe188ca4b124054e58b2b90ed288c60f`  
		Last Modified: Thu, 02 Mar 2023 04:34:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1484a7e498bcc146b58f5b3909d50bb76e2c0b00e47e51d34ce272d50549e26`  
		Last Modified: Thu, 02 Mar 2023 06:39:20 GMT  
		Size: 6.0 MB (6032219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cca61a0682f055af59b1a8385955c174c8bb5ef2f30387413b8c899ea7a951`  
		Last Modified: Thu, 02 Mar 2023 06:39:21 GMT  
		Size: 29.5 MB (29520185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e8e6715b795bf53fffce095fadd3925460a0aaea95c3f9a55843b1c80316e1`  
		Last Modified: Thu, 02 Mar 2023 06:39:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530fa0573412ae5c0dca10d9f09b3cc244f84571c5693c53d5e965ab47b54bbf`  
		Last Modified: Thu, 02 Mar 2023 06:39:20 GMT  
		Size: 1.1 MB (1095361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ae3a7b5d10fef17c4b48b8baa55b6708c3dc78651c86a37f45e1d2c74e3f6`  
		Last Modified: Thu, 02 Mar 2023 06:39:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk17`

```console
$ docker pull jruby@sha256:b497409bb99cd4fb67f7d384fa85967705a01b34247cac99f6f02bcced00589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:12886a5569ce56a46c2a3b3bbe8091b8d1125ae97aa05f8a488c955b993ddad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278805536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2166be768bab8c33e76e2add0208b016737f54da04b1655b30bcfea4729ea643`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:03:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:03:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 09:38:59 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:38:59 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:38:59 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:39:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:02 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:39:10 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:39:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:39:10 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:39:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:39:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2548829404a24408e385f432f5dcf1364d2d027a631388b2d7ffae095912d57e`  
		Last Modified: Thu, 02 Mar 2023 04:10:27 GMT  
		Size: 192.4 MB (192448038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648deea0f1d95f4a147cd47f868801085ae5652e54f9bec42b292fed0db4c11`  
		Last Modified: Thu, 02 Mar 2023 04:10:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a43766f7bf1125162ccce1cf6b2fd16ae3cda644c8f901274952a4a1aa11ac6`  
		Last Modified: Thu, 02 Mar 2023 09:42:34 GMT  
		Size: 7.1 MB (7071395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424bbcdaaf5ccdd62c4b576b260041f48d0a3b3e3447ac2ef137e35e7e97a35d`  
		Last Modified: Thu, 02 Mar 2023 09:42:35 GMT  
		Size: 29.5 MB (29520245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1e06cadafaa4d3fca89aeff5fc9a7e66f5629b444654af73a174cfabf5d0d5`  
		Last Modified: Thu, 02 Mar 2023 09:42:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7daad4c68e64e08918ee16e55e1baa6993ed4541b2a23f9b0ff553ca1cda066`  
		Last Modified: Thu, 02 Mar 2023 09:42:33 GMT  
		Size: 1.1 MB (1095356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbd0f92d719c5e5aac6fe16ed681c300f0fc39aba9aef7d90135910eb116a`  
		Last Modified: Thu, 02 Mar 2023 09:42:33 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:400a4c0d2747f727e86e375b455c7b873ba788137f3ad6ab6f248c92d3c9943d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275922177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e905ff56ddc008e49bceee1cbf6db94cae37e2313e09c62102d96e31c164041`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:29:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:29:35 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:29:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 04:29:52 GMT
CMD ["jshell"]
# Thu, 02 Mar 2023 06:36:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:36:12 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:36:12 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:36:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:36:14 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:14 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:36:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:36:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:36:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:36:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:36:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30249df1bda77f2171b754e4a76ef4c05cb50a40a6247b44ec30f654b9e5db4f`  
		Last Modified: Thu, 02 Mar 2023 04:35:24 GMT  
		Size: 20.8 MB (20810122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d009541900c02211c26f800cc060dd6862ccf839b4b3de0c58fa79004e52347`  
		Last Modified: Thu, 02 Mar 2023 04:35:32 GMT  
		Size: 191.3 MB (191267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb21286d602781c3885407902a84537861b872a08408b28ff832fbe0e31b3ad`  
		Last Modified: Thu, 02 Mar 2023 04:35:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c066c3b9e2adec7e9bca1bf2506f50fe954adc20fad465c4dac454064b37fb`  
		Last Modified: Thu, 02 Mar 2023 06:39:33 GMT  
		Size: 6.0 MB (6034293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dead708776322745d3483494d630d294f97804543d47591834c8abf0e629ae6`  
		Last Modified: Thu, 02 Mar 2023 06:39:35 GMT  
		Size: 29.5 MB (29520192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21568502a93e3d009296e3cce8cc8287c7d9d15c57030ab8958d01ec2728ceb9`  
		Last Modified: Thu, 02 Mar 2023 06:39:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba573fa1d8e2e256663fe6cc96989c9294d3db31a26a358375b984659107f8e`  
		Last Modified: Thu, 02 Mar 2023 06:39:32 GMT  
		Size: 1.1 MB (1095365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0470a03d15f911424a9b6dd56bfc4fb54366bfa9381a12b824e8a6b70e8188e2`  
		Last Modified: Thu, 02 Mar 2023 06:39:32 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk8`

```console
$ docker pull jruby@sha256:485be14201a8a78791e5a89a620a4d2f8bc426d996c0b18c52cc362a33d40f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:10283ce3a21d5d8fe8d3fac6bf0e5d231fce39d634075e1271e7693269f6c39f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa763fb855a6e8a9c9d7db8f4ec8afacfb6d221ba9272b5dbb64d3121e238677`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:01:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:51 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:51 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:53 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:53 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:54 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:01 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a604468dcc8d2ddeebed9e273d813bd3892d92f1bfa2412f265d951970e091`  
		Last Modified: Thu, 02 Mar 2023 04:07:46 GMT  
		Size: 54.6 MB (54635765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1e7a239e8ee2630f44b7a29f2440d9d6f89ff9db20129e63a6a9a1c25991be`  
		Last Modified: Thu, 02 Mar 2023 04:07:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f398851bbb10c8d7e71ec5d9cfcaf96d985658347fc0e0d5a6e0263cbde2a`  
		Last Modified: Thu, 02 Mar 2023 09:41:44 GMT  
		Size: 7.1 MB (7069147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b91d996b70d9d4d79336b4731dcb1b03cf663431c1ba08aa0c1392f36fcd3`  
		Last Modified: Thu, 02 Mar 2023 09:41:45 GMT  
		Size: 29.5 MB (29520214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f5cb261cb0df0f6c7d056331e8bdb11042a382a699d93986ada8c5db9ae51b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af712ebf0a46fc5ca442112c7485321cbd344c305901ef0ff4956441ca94033`  
		Last Modified: Thu, 02 Mar 2023 09:41:43 GMT  
		Size: 1.1 MB (1095403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4402fe683a8d4cb0ac1361aa318c59891cdf1a30ba92a7f97cd2810f51460b`  
		Last Modified: Thu, 02 Mar 2023 09:41:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a643267990dfc4fa3d6c6ac998631b498331c914e9e766be58a78ef739566244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133784615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56102a9c77c8534d5f991f2462a7eb13c855bb14c11a441c7d728212db39fe9c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:27:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:23 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:23 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:24 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:25 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:32 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:33 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2352937d1109a4a81f3c5e9ff477d3821c71cbfc7201c71efb4e1ecb69776`  
		Last Modified: Thu, 02 Mar 2023 04:33:12 GMT  
		Size: 53.7 MB (53731789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb83fae65015c81b751082d23371b3c50009dcf1cdb0a5cb3caf277f3c1387`  
		Last Modified: Thu, 02 Mar 2023 04:33:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53330ab9d982ead5a1b7ca9dcbd4378293e12207b9cb91b5cf1d5007eabf9b26`  
		Last Modified: Thu, 02 Mar 2023 06:38:43 GMT  
		Size: 6.0 MB (6032201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a9e4e1062122c129268252b18e0ebf269641b9d8c8b93a4ad5843bd0646213`  
		Last Modified: Thu, 02 Mar 2023 06:38:44 GMT  
		Size: 29.5 MB (29520183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0a539f55165554ed9eecdfd0b0487bd89843161473e3ede72d36546137b72`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c088b8a51cb50e666767a2f7ca665b585661457fed07e7ac4a437b76f224b5`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 1.1 MB (1095359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be010112239a7b7b41dcb28798cf70fff82abaff20479c3e72654d44b7f216`  
		Last Modified: Thu, 02 Mar 2023 06:38:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre`

```console
$ docker pull jruby@sha256:8036666551cc4d91c7fa6b05d6059e30688c9d88b406ebf00a53152f7195f3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1093c548fb1011cf24a81fd0ebe6b76d32b734ec88f1232f35a92137d0be287d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124429123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6d70119a0eb571b1bac667c0532ebe3fe278960902a8a59b67480c6b5ce17`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:29 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:37:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:37:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:37:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548519484b88477ab772a04bf9296e5d0e17fa5e97d0196ac81da68ed6477711`  
		Last Modified: Thu, 02 Mar 2023 09:41:15 GMT  
		Size: 29.5 MB (29520286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caeab7eb36ce42db49c9c8fa704fa5038a2a26177c589b22c7e20a878070966`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9544fae45a355b43c980e67e5763dc8730b12b885c7d41f99819ef8009059ef9`  
		Last Modified: Thu, 02 Mar 2023 09:41:13 GMT  
		Size: 1.1 MB (1095410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1ad41c22b626703a2c077f7e0414fead462195f572d72d6ad560ba6f486a9`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc355b60755824c38ca982f61a9f9cea34abf0e01766043f74579a0fab217cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e90de4d2847f48db1cdf86f8c5def1dd0ee8b770a40c5dcc3cdf1e0d2896735`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:05 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:06 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb95aed0bfff6ec7ea0874f0d35d6b05d913ff83175c2dc91ddbd3701d2460`  
		Last Modified: Thu, 02 Mar 2023 06:38:13 GMT  
		Size: 29.5 MB (29520125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1045ee4c980fb26c9507b6a0db37a6502d73802c2886ee70d2f69cff8a4d7e`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8892c6242c9a22ff7c2a3fc7fde5ec03f73a6f5f6db4ecc43711c01c45796`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 1.1 MB (1095355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dca95b6390402db17d2d849d8075cca2bf20bd9a8cc546874434059343b83f`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre11`

```console
$ docker pull jruby@sha256:d262a1a936dcb5a36f10891e578b68ddd6ab429d36ef5f91f91e99c2d9a24259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:8d395a69ce98401e611152f5f32ea1fc3583462500ee3c7783169b2e5fc74701
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129237091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35907aafea63cf49cfc2a2c9c56ed0445ae1b8b19e266f8b38bec6af63427d7d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 09:38:11 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:38:11 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:38:11 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:38:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:38:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:38:22 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:38:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:38:23 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:38:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:38:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b665fdae859de8574371cb2dbbec0e1104edf8327f0a48aa0d42dc7156361f`  
		Last Modified: Thu, 02 Mar 2023 09:42:08 GMT  
		Size: 7.1 MB (7069117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649eb30b280113087b4104056e1f4421ed387619ba0268f7ce406dcb43db7d28`  
		Last Modified: Thu, 02 Mar 2023 09:42:09 GMT  
		Size: 29.5 MB (29520275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957f1ccb121bf3d18788c035b8946d5295e3ac4f4752bc82d1eae07edffc026e`  
		Last Modified: Thu, 02 Mar 2023 09:42:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd8231563690dbf1366270749a0e520f1309c0c6ca837193363a3c624991517`  
		Last Modified: Thu, 02 Mar 2023 09:42:07 GMT  
		Size: 1.1 MB (1095379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e2380713ffda589209eeb791974f664963032244b72ea623bbb50d3ebf6fe9`  
		Last Modified: Thu, 02 Mar 2023 09:42:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:465521e12ba698f55e812a04770cebcfa71140707027fec3c9294bbaa7a47416
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125032544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd645654fa14c70e4550955498e1027e2d658bc44a3f41d7f9d5964fd736f831`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:28:24 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:29:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:29:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 06:35:39 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:39 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:39 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:40 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:41 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:41 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:48 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b550e0153d6633dc59f3ed4f76afd8953d647dfc2d7c7ead4e51d8b2841a143a`  
		Last Modified: Thu, 02 Mar 2023 04:34:58 GMT  
		Size: 45.0 MB (44979643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d760d96418bc955ac7bfd4587f53a1c25a45a19f8748622e538d3b1c79efe`  
		Last Modified: Thu, 02 Mar 2023 04:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c05cfc887522c4779b088b17d01ebb4b48a5c38f6e4e21148dd3f0d421d0dd`  
		Last Modified: Thu, 02 Mar 2023 06:39:07 GMT  
		Size: 6.0 MB (6032209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7f5fe5a5ffe596b8e773bc48a4e991f682ab7a7a2267a40e4b697a4e068632`  
		Last Modified: Thu, 02 Mar 2023 06:39:08 GMT  
		Size: 29.5 MB (29520222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddacd3c4861b16974ae50d5b7a88e91a5217eddd78bcb30bb44a607a6b2abef`  
		Last Modified: Thu, 02 Mar 2023 06:39:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae1448ce4f78142cc8a84176e779e4edf7d0c2b874afd698a870e45b356449d`  
		Last Modified: Thu, 02 Mar 2023 06:39:06 GMT  
		Size: 1.1 MB (1095389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fd967b2a9a866b5d4f58ac3e2f7cf59343eb8594ce59e4b28883207e2c7a58`  
		Last Modified: Thu, 02 Mar 2023 06:39:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre8`

```console
$ docker pull jruby@sha256:8036666551cc4d91c7fa6b05d6059e30688c9d88b406ebf00a53152f7195f3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1093c548fb1011cf24a81fd0ebe6b76d32b734ec88f1232f35a92137d0be287d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124429123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6d70119a0eb571b1bac667c0532ebe3fe278960902a8a59b67480c6b5ce17`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:29 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:37:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:37:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:37:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548519484b88477ab772a04bf9296e5d0e17fa5e97d0196ac81da68ed6477711`  
		Last Modified: Thu, 02 Mar 2023 09:41:15 GMT  
		Size: 29.5 MB (29520286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caeab7eb36ce42db49c9c8fa704fa5038a2a26177c589b22c7e20a878070966`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9544fae45a355b43c980e67e5763dc8730b12b885c7d41f99819ef8009059ef9`  
		Last Modified: Thu, 02 Mar 2023 09:41:13 GMT  
		Size: 1.1 MB (1095410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1ad41c22b626703a2c077f7e0414fead462195f572d72d6ad560ba6f486a9`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc355b60755824c38ca982f61a9f9cea34abf0e01766043f74579a0fab217cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e90de4d2847f48db1cdf86f8c5def1dd0ee8b770a40c5dcc3cdf1e0d2896735`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:05 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:06 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb95aed0bfff6ec7ea0874f0d35d6b05d913ff83175c2dc91ddbd3701d2460`  
		Last Modified: Thu, 02 Mar 2023 06:38:13 GMT  
		Size: 29.5 MB (29520125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1045ee4c980fb26c9507b6a0db37a6502d73802c2886ee70d2f69cff8a4d7e`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8892c6242c9a22ff7c2a3fc7fde5ec03f73a6f5f6db4ecc43711c01c45796`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 1.1 MB (1095355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dca95b6390402db17d2d849d8075cca2bf20bd9a8cc546874434059343b83f`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.2`

**does not exist** (yet?)

## `jruby:9.4.2-jdk`

**does not exist** (yet?)

## `jruby:9.4.2-jdk11`

**does not exist** (yet?)

## `jruby:9.4.2-jdk17`

**does not exist** (yet?)

## `jruby:9.4.2-jdk8`

**does not exist** (yet?)

## `jruby:9.4.2-jre`

**does not exist** (yet?)

## `jruby:9.4.2-jre11`

**does not exist** (yet?)

## `jruby:9.4.2-jre8`

**does not exist** (yet?)

## `jruby:9.4.2.0`

**does not exist** (yet?)

## `jruby:9.4.2.0-jdk`

**does not exist** (yet?)

## `jruby:9.4.2.0-jdk11`

**does not exist** (yet?)

## `jruby:9.4.2.0-jdk17`

**does not exist** (yet?)

## `jruby:9.4.2.0-jdk8`

**does not exist** (yet?)

## `jruby:9.4.2.0-jre`

**does not exist** (yet?)

## `jruby:9.4.2.0-jre11`

**does not exist** (yet?)

## `jruby:9.4.2.0-jre8`

**does not exist** (yet?)

## `jruby:latest`

```console
$ docker pull jruby@sha256:8036666551cc4d91c7fa6b05d6059e30688c9d88b406ebf00a53152f7195f3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:1093c548fb1011cf24a81fd0ebe6b76d32b734ec88f1232f35a92137d0be287d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124429123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6d70119a0eb571b1bac667c0532ebe3fe278960902a8a59b67480c6b5ce17`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:01:25 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:02:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:02:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 09:37:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 09:37:26 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 09:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 09:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:29 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 09:37:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 09:37:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 09:37:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 09:37:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 09:37:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f153beee3524c1bc9661095592c903191f04b8ef3698a9521e77e52e0ca368`  
		Last Modified: Thu, 02 Mar 2023 04:08:21 GMT  
		Size: 41.8 MB (41824184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba0921a1f8f7441b2c3b8b01a8cd7bf0b310630be3dd9245196ebccc60b7053`  
		Last Modified: Thu, 02 Mar 2023 04:08:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887b319e99d8c9f905ca4fe2ebb389aa8c9218f4fe09c0125055b3e8ed89792`  
		Last Modified: Thu, 02 Mar 2023 09:41:14 GMT  
		Size: 7.1 MB (7069195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548519484b88477ab772a04bf9296e5d0e17fa5e97d0196ac81da68ed6477711`  
		Last Modified: Thu, 02 Mar 2023 09:41:15 GMT  
		Size: 29.5 MB (29520286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caeab7eb36ce42db49c9c8fa704fa5038a2a26177c589b22c7e20a878070966`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9544fae45a355b43c980e67e5763dc8730b12b885c7d41f99819ef8009059ef9`  
		Last Modified: Thu, 02 Mar 2023 09:41:13 GMT  
		Size: 1.1 MB (1095410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b1ad41c22b626703a2c077f7e0414fead462195f572d72d6ad560ba6f486a9`  
		Last Modified: Thu, 02 Mar 2023 09:41:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc355b60755824c38ca982f61a9f9cea34abf0e01766043f74579a0fab217cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120861494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e90de4d2847f48db1cdf86f8c5def1dd0ee8b770a40c5dcc3cdf1e0d2896735`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:35:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 06:35:05 GMT
ENV JRUBY_VERSION=9.4.1.0
# Thu, 02 Mar 2023 06:35:06 GMT
ENV JRUBY_SHA256=5e0cce40b7c42f8ad0f619fdd906460fe3ef13444707f70eb8abfc6481e0d6b6
# Thu, 02 Mar 2023 06:35:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 02 Mar 2023 06:35:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 02 Mar 2023 06:35:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 02 Mar 2023 06:35:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Mar 2023 06:35:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:35:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Mar 2023 06:35:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796e89d82b655ddd723e1654b7639b7ff68bf20ac2ac68467c4e2fdd00fd2267`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 6.0 MB (6032107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb95aed0bfff6ec7ea0874f0d35d6b05d913ff83175c2dc91ddbd3701d2460`  
		Last Modified: Thu, 02 Mar 2023 06:38:13 GMT  
		Size: 29.5 MB (29520125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1045ee4c980fb26c9507b6a0db37a6502d73802c2886ee70d2f69cff8a4d7e`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a8892c6242c9a22ff7c2a3fc7fde5ec03f73a6f5f6db4ecc43711c01c45796`  
		Last Modified: Thu, 02 Mar 2023 06:38:12 GMT  
		Size: 1.1 MB (1095355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dca95b6390402db17d2d849d8075cca2bf20bd9a8cc546874434059343b83f`  
		Last Modified: Thu, 02 Mar 2023 06:38:11 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
