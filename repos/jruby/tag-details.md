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
-	[`jruby:9.4.3`](#jruby943)
-	[`jruby:9.4.3-jdk`](#jruby943-jdk)
-	[`jruby:9.4.3-jdk11`](#jruby943-jdk11)
-	[`jruby:9.4.3-jdk17`](#jruby943-jdk17)
-	[`jruby:9.4.3-jdk8`](#jruby943-jdk8)
-	[`jruby:9.4.3-jre`](#jruby943-jre)
-	[`jruby:9.4.3-jre11`](#jruby943-jre11)
-	[`jruby:9.4.3-jre8`](#jruby943-jre8)
-	[`jruby:9.4.3.0`](#jruby9430)
-	[`jruby:9.4.3.0-jdk`](#jruby9430-jdk)
-	[`jruby:9.4.3.0-jdk11`](#jruby9430-jdk11)
-	[`jruby:9.4.3.0-jdk17`](#jruby9430-jdk17)
-	[`jruby:9.4.3.0-jdk8`](#jruby9430-jdk8)
-	[`jruby:9.4.3.0-jre`](#jruby9430-jre)
-	[`jruby:9.4.3.0-jre11`](#jruby9430-jre11)
-	[`jruby:9.4.3.0-jre8`](#jruby9430-jre8)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:66306bca9ceaa13fb16cf5333f9b692e78db1864940e8a0143880afb31970bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:2b05d7405cecd432bff8a57907d4cdaeda5e0ecbffe0f2c26819a62900b42335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226787983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52994997c6881e809024f134f44687242fdb8fad8c7468fd87bf58f7ea1c1f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:56:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8eaded9fd7ab0bb2ad9d16c0a39facde3435075a399df5f0f66f916ec91a9`  
		Last Modified: Wed, 26 Jul 2023 01:57:45 GMT  
		Size: 28.9 MB (28854390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a44854ecc98a9c80981c115192ab89daf6428642e89439281497613286b9b6`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed181e74af30293bb7e9f92d6a4339610cdc1d8cb15fded75f2a7e71c71a657`  
		Last Modified: Wed, 26 Jul 2023 01:57:43 GMT  
		Size: 1.1 MB (1069976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2e6c0960b685dff655c9ab99af676c440d2dda8739f85809d5b719bf4f3d19`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:065b16bbef2ca339c8a6d5a2ecafb75c56b80bf7c4b9460d73af4799234114d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220959579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f059416d62b80ca9778f7c2a2e0f5ef8162a0472a8c7692174976c9249fe0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:25:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:25:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:25:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450d297c7a0460afe7ee218bd8b4a851f415b713ee158e9b662c8a8699453f4`  
		Last Modified: Wed, 26 Jul 2023 01:26:31 GMT  
		Size: 28.9 MB (28854410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9412739df651bc20cb83519973a52e05c0ba41d0faebbde2cacffc41164c37`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6f4e725d40cfd129ec8f7c32b53a4dc429b4feee4303fb65d809b6ed4a3239`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 1.1 MB (1069946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe47351228ab01f81d91b9606a38abeb6666dc46ed27172ad9d10858ea07ea88`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:6cc510b53c721db5e3918367a588fbf1fa64cb3232b9b2a68528cc8480d603c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:d556604e6418e8cda27088a01a27c801fcaed9e083f20c94541e254d3ac1ebcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230475115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e7de586b2752960bcaa355b475229f2868df9c45b57a85c9ec77ccb353b67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 00:13:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b491a8b27fca621093866ef555c3a383fed8b88f5d401148ece1169fd103bc3f`  
		Last Modified: Wed, 26 Jul 2023 00:14:43 GMT  
		Size: 28.9 MB (28854263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868d3cebbb970e293b7b72f4642c30219f980971c5883697e07233a990f11035`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16203320dcf03054e18ec7ae0228b8c11be52d714f92bc1f030f30118fa4c8`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 1.1 MB (1069928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03f051359f48e8e6965174c89dafdc34df3b62fa914042f9a5b8439af9375ee`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:181411fca332ea5eef939cf3e3f0bdb6d826f8997f087932405a2f307060e3de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227545792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13833d40f4a8bec1ef5a4a08890db5ac5264a558d7b5d4ace050d0423683577`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:34:16 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e17a8e4750733909641fb52757eecfd0b6ef617f72532f4c9ee5016c97230`  
		Last Modified: Tue, 25 Jul 2023 23:35:22 GMT  
		Size: 28.9 MB (28854423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7bb5ea1c2797b34c11845cc93dbda5e7218add26d679665261ce79ebc450ba`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4e7e673ccb80f64b2eaaf15102448928d282ce12679a180b3f31f8f3d41988`  
		Last Modified: Tue, 25 Jul 2023 23:35:21 GMT  
		Size: 1.1 MB (1069929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5be76963e89fea07c78f3e1c9b589af4d666ae0c4c699280357e069efa95d05`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:1e35354615d007a9137ff0d4be4e1aa241c519b1f4a1b289d28573baa4a95b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:5077842747f3cb8fb39fb75afe928b0d6759675c104a8882b28da27483d4a411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700e87fb9363288b4cbacc8c7e96eee439b9b37b17810bba710ca7b405cc642b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:55:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:05 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523551d5bc275982837df84b380b18ef54034a6f786a9d94f25f3adbf21de92c`  
		Last Modified: Wed, 26 Jul 2023 01:57:31 GMT  
		Size: 28.9 MB (28854420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1be206236793ebf534310f343053aba22215e3529144de57ff99b55cc8749bd`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78731de877c61fcbe359153a2a5a23cc776b9ae363c45f07ef1d169c79cd0d1`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 1.1 MB (1069939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8af2b8476e2fb2e1f82f97afdcc2cfe1df8f64f57d72cb60a623c3947e7ca5`  
		Last Modified: Wed, 26 Jul 2023 01:57:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:f5bc79d3eeaea69c402014c7bbdc3ad87b993b91ce6954b3cd8cadee79ebc306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124578222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c240b2aac2fd9790695b14dce75719812de3a6614427e49e38e0697039bf0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:48 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d0203824d7162e3de4aa4cc83338902560330f1cc77a9010e5138b38a6eb5`  
		Last Modified: Wed, 26 Jul 2023 01:26:19 GMT  
		Size: 28.9 MB (28854428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2734919a6267c5f034ab0ae896acf5211a46ece6a07480f80dc4cf094a860191`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56484fae4d60cda285a9e7fa974d213df329bcb9d7b24012b256b64618f92a02`  
		Last Modified: Wed, 26 Jul 2023 01:26:18 GMT  
		Size: 1.1 MB (1069954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46000b281c43e86df0c875d70282273d203a4e5868fb18116382b79db56b14a3`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk11`

```console
$ docker pull jruby@sha256:66306bca9ceaa13fb16cf5333f9b692e78db1864940e8a0143880afb31970bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:2b05d7405cecd432bff8a57907d4cdaeda5e0ecbffe0f2c26819a62900b42335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226787983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52994997c6881e809024f134f44687242fdb8fad8c7468fd87bf58f7ea1c1f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:56:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8eaded9fd7ab0bb2ad9d16c0a39facde3435075a399df5f0f66f916ec91a9`  
		Last Modified: Wed, 26 Jul 2023 01:57:45 GMT  
		Size: 28.9 MB (28854390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a44854ecc98a9c80981c115192ab89daf6428642e89439281497613286b9b6`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed181e74af30293bb7e9f92d6a4339610cdc1d8cb15fded75f2a7e71c71a657`  
		Last Modified: Wed, 26 Jul 2023 01:57:43 GMT  
		Size: 1.1 MB (1069976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2e6c0960b685dff655c9ab99af676c440d2dda8739f85809d5b719bf4f3d19`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:065b16bbef2ca339c8a6d5a2ecafb75c56b80bf7c4b9460d73af4799234114d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220959579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f059416d62b80ca9778f7c2a2e0f5ef8162a0472a8c7692174976c9249fe0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:25:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:25:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:25:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450d297c7a0460afe7ee218bd8b4a851f415b713ee158e9b662c8a8699453f4`  
		Last Modified: Wed, 26 Jul 2023 01:26:31 GMT  
		Size: 28.9 MB (28854410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9412739df651bc20cb83519973a52e05c0ba41d0faebbde2cacffc41164c37`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6f4e725d40cfd129ec8f7c32b53a4dc429b4feee4303fb65d809b6ed4a3239`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 1.1 MB (1069946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe47351228ab01f81d91b9606a38abeb6666dc46ed27172ad9d10858ea07ea88`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk17`

```console
$ docker pull jruby@sha256:6cc510b53c721db5e3918367a588fbf1fa64cb3232b9b2a68528cc8480d603c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:d556604e6418e8cda27088a01a27c801fcaed9e083f20c94541e254d3ac1ebcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230475115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e7de586b2752960bcaa355b475229f2868df9c45b57a85c9ec77ccb353b67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 00:13:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b491a8b27fca621093866ef555c3a383fed8b88f5d401148ece1169fd103bc3f`  
		Last Modified: Wed, 26 Jul 2023 00:14:43 GMT  
		Size: 28.9 MB (28854263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868d3cebbb970e293b7b72f4642c30219f980971c5883697e07233a990f11035`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16203320dcf03054e18ec7ae0228b8c11be52d714f92bc1f030f30118fa4c8`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 1.1 MB (1069928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03f051359f48e8e6965174c89dafdc34df3b62fa914042f9a5b8439af9375ee`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:181411fca332ea5eef939cf3e3f0bdb6d826f8997f087932405a2f307060e3de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227545792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13833d40f4a8bec1ef5a4a08890db5ac5264a558d7b5d4ace050d0423683577`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:34:16 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e17a8e4750733909641fb52757eecfd0b6ef617f72532f4c9ee5016c97230`  
		Last Modified: Tue, 25 Jul 2023 23:35:22 GMT  
		Size: 28.9 MB (28854423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7bb5ea1c2797b34c11845cc93dbda5e7218add26d679665261ce79ebc450ba`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4e7e673ccb80f64b2eaaf15102448928d282ce12679a180b3f31f8f3d41988`  
		Last Modified: Tue, 25 Jul 2023 23:35:21 GMT  
		Size: 1.1 MB (1069929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5be76963e89fea07c78f3e1c9b589af4d666ae0c4c699280357e069efa95d05`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jdk8`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre11`

```console
$ docker pull jruby@sha256:1e35354615d007a9137ff0d4be4e1aa241c519b1f4a1b289d28573baa4a95b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:5077842747f3cb8fb39fb75afe928b0d6759675c104a8882b28da27483d4a411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700e87fb9363288b4cbacc8c7e96eee439b9b37b17810bba710ca7b405cc642b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:55:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:05 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523551d5bc275982837df84b380b18ef54034a6f786a9d94f25f3adbf21de92c`  
		Last Modified: Wed, 26 Jul 2023 01:57:31 GMT  
		Size: 28.9 MB (28854420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1be206236793ebf534310f343053aba22215e3529144de57ff99b55cc8749bd`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78731de877c61fcbe359153a2a5a23cc776b9ae363c45f07ef1d169c79cd0d1`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 1.1 MB (1069939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8af2b8476e2fb2e1f82f97afdcc2cfe1df8f64f57d72cb60a623c3947e7ca5`  
		Last Modified: Wed, 26 Jul 2023 01:57:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:f5bc79d3eeaea69c402014c7bbdc3ad87b993b91ce6954b3cd8cadee79ebc306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124578222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c240b2aac2fd9790695b14dce75719812de3a6614427e49e38e0697039bf0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:48 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d0203824d7162e3de4aa4cc83338902560330f1cc77a9010e5138b38a6eb5`  
		Last Modified: Wed, 26 Jul 2023 01:26:19 GMT  
		Size: 28.9 MB (28854428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2734919a6267c5f034ab0ae896acf5211a46ece6a07480f80dc4cf094a860191`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56484fae4d60cda285a9e7fa974d213df329bcb9d7b24012b256b64618f92a02`  
		Last Modified: Wed, 26 Jul 2023 01:26:18 GMT  
		Size: 1.1 MB (1069954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46000b281c43e86df0c875d70282273d203a4e5868fb18116382b79db56b14a3`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10-jre8`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk11`

```console
$ docker pull jruby@sha256:66306bca9ceaa13fb16cf5333f9b692e78db1864940e8a0143880afb31970bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:2b05d7405cecd432bff8a57907d4cdaeda5e0ecbffe0f2c26819a62900b42335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226787983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f52994997c6881e809024f134f44687242fdb8fad8c7468fd87bf58f7ea1c1f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:56:09 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:56:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8eaded9fd7ab0bb2ad9d16c0a39facde3435075a399df5f0f66f916ec91a9`  
		Last Modified: Wed, 26 Jul 2023 01:57:45 GMT  
		Size: 28.9 MB (28854390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a44854ecc98a9c80981c115192ab89daf6428642e89439281497613286b9b6`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed181e74af30293bb7e9f92d6a4339610cdc1d8cb15fded75f2a7e71c71a657`  
		Last Modified: Wed, 26 Jul 2023 01:57:43 GMT  
		Size: 1.1 MB (1069976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2e6c0960b685dff655c9ab99af676c440d2dda8739f85809d5b719bf4f3d19`  
		Last Modified: Wed, 26 Jul 2023 01:57:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:065b16bbef2ca339c8a6d5a2ecafb75c56b80bf7c4b9460d73af4799234114d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220959579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f059416d62b80ca9778f7c2a2e0f5ef8162a0472a8c7692174976c9249fe0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:57 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:25:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:25:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:25:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:25:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:25:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450d297c7a0460afe7ee218bd8b4a851f415b713ee158e9b662c8a8699453f4`  
		Last Modified: Wed, 26 Jul 2023 01:26:31 GMT  
		Size: 28.9 MB (28854410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9412739df651bc20cb83519973a52e05c0ba41d0faebbde2cacffc41164c37`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6f4e725d40cfd129ec8f7c32b53a4dc429b4feee4303fb65d809b6ed4a3239`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 1.1 MB (1069946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe47351228ab01f81d91b9606a38abeb6666dc46ed27172ad9d10858ea07ea88`  
		Last Modified: Wed, 26 Jul 2023 01:26:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk17`

```console
$ docker pull jruby@sha256:6cc510b53c721db5e3918367a588fbf1fa64cb3232b9b2a68528cc8480d603c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:d556604e6418e8cda27088a01a27c801fcaed9e083f20c94541e254d3ac1ebcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230475115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e7de586b2752960bcaa355b475229f2868df9c45b57a85c9ec77ccb353b67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 00:13:33 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 00:13:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b491a8b27fca621093866ef555c3a383fed8b88f5d401148ece1169fd103bc3f`  
		Last Modified: Wed, 26 Jul 2023 00:14:43 GMT  
		Size: 28.9 MB (28854263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868d3cebbb970e293b7b72f4642c30219f980971c5883697e07233a990f11035`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16203320dcf03054e18ec7ae0228b8c11be52d714f92bc1f030f30118fa4c8`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 1.1 MB (1069928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03f051359f48e8e6965174c89dafdc34df3b62fa914042f9a5b8439af9375ee`  
		Last Modified: Wed, 26 Jul 2023 00:14:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:181411fca332ea5eef939cf3e3f0bdb6d826f8997f087932405a2f307060e3de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227545792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13833d40f4a8bec1ef5a4a08890db5ac5264a558d7b5d4ace050d0423683577`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 25 Jul 2023 23:34:14 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:34:16 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:16 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:23 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e17a8e4750733909641fb52757eecfd0b6ef617f72532f4c9ee5016c97230`  
		Last Modified: Tue, 25 Jul 2023 23:35:22 GMT  
		Size: 28.9 MB (28854423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7bb5ea1c2797b34c11845cc93dbda5e7218add26d679665261ce79ebc450ba`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4e7e673ccb80f64b2eaaf15102448928d282ce12679a180b3f31f8f3d41988`  
		Last Modified: Tue, 25 Jul 2023 23:35:21 GMT  
		Size: 1.1 MB (1069929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5be76963e89fea07c78f3e1c9b589af4d666ae0c4c699280357e069efa95d05`  
		Last Modified: Tue, 25 Jul 2023 23:35:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jdk8`

```console
$ docker pull jruby@sha256:53f9a131ec6e4ea4a261f8f21f02f0612a5a3eee7a16257c247859faaf4ccc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:cbd8462aba009c2eebd72692b1cdb2e57dbbea1a796a45441ac06a0fa84084ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185538945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d7bf052eddf5258301d35c8dea1f980326600af6d987d44130707df68637c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:28:05 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:28:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:28:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:08 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:15 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3a7afcec4423e625ca0845569e53ac488ef60650edc776cfc9eae5de91e64c`  
		Last Modified: Tue, 01 Aug 2023 22:30:12 GMT  
		Size: 28.9 MB (28854281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3964120bdaec530548036f771747865c736dc20d902b0aff5ce9ecb04c32c40`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cec813742cda3caa18695d2a7ea408d3f33c3b2605d92238ad5de55f2f8192`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 1.1 MB (1069925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923a1003471dce72e2dd5ff505d1f800816efce47d550ac944feeb2ee335ac7`  
		Last Modified: Tue, 01 Aug 2023 22:30:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4bf010fd689596a26f432c57d113a2d62ab95cb11b67e68939e24b24279d428d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182077760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b089d56d4d29102557c49c6e1813a110e450d21119f63308ff40d9f0456737`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:40:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:40:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:40:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:40:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:40:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb5c511a8e0a7c71ec42a728ae2f46148252f984a2328418f4be32019772dfc`  
		Last Modified: Tue, 01 Aug 2023 22:41:58 GMT  
		Size: 28.9 MB (28854474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9682e0a34a15ff1e0fcb7c09627fc6d5dd9849ba4d1d5f30d018e6404bc9d495`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f88460787189f3f09695b6e110878bd6eafecd5c1dc9528e18784390a87d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:57 GMT  
		Size: 1.1 MB (1069956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d9ef95a36ef40881e28a293cea83de1a02cc29149b01f3c7ba18b906225c9`  
		Last Modified: Tue, 01 Aug 2023 22:41:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre11`

```console
$ docker pull jruby@sha256:1e35354615d007a9137ff0d4be4e1aa241c519b1f4a1b289d28573baa4a95b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:5077842747f3cb8fb39fb75afe928b0d6759675c104a8882b28da27483d4a411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700e87fb9363288b4cbacc8c7e96eee439b9b37b17810bba710ca7b405cc642b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:55:54 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:55:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:56:05 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:56:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:56:05 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:56:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:56:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523551d5bc275982837df84b380b18ef54034a6f786a9d94f25f3adbf21de92c`  
		Last Modified: Wed, 26 Jul 2023 01:57:31 GMT  
		Size: 28.9 MB (28854420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1be206236793ebf534310f343053aba22215e3529144de57ff99b55cc8749bd`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78731de877c61fcbe359153a2a5a23cc776b9ae363c45f07ef1d169c79cd0d1`  
		Last Modified: Wed, 26 Jul 2023 01:57:29 GMT  
		Size: 1.1 MB (1069939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8af2b8476e2fb2e1f82f97afdcc2cfe1df8f64f57d72cb60a623c3947e7ca5`  
		Last Modified: Wed, 26 Jul 2023 01:57:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:f5bc79d3eeaea69c402014c7bbdc3ad87b993b91ce6954b3cd8cadee79ebc306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124578222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c240b2aac2fd9790695b14dce75719812de3a6614427e49e38e0697039bf0a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_VERSION=9.3.10.0
# Wed, 26 Jul 2023 01:24:46 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:48 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:48 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:55 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d0203824d7162e3de4aa4cc83338902560330f1cc77a9010e5138b38a6eb5`  
		Last Modified: Wed, 26 Jul 2023 01:26:19 GMT  
		Size: 28.9 MB (28854428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2734919a6267c5f034ab0ae896acf5211a46ece6a07480f80dc4cf094a860191`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56484fae4d60cda285a9e7fa974d213df329bcb9d7b24012b256b64618f92a02`  
		Last Modified: Wed, 26 Jul 2023 01:26:18 GMT  
		Size: 1.1 MB (1069954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46000b281c43e86df0c875d70282273d203a4e5868fb18116382b79db56b14a3`  
		Last Modified: Wed, 26 Jul 2023 01:26:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.10.0-jre8`

```console
$ docker pull jruby@sha256:d48adb1bb03d6ad0664162c82c0fcd21c1b8316d5ebfc5a53d20594eadad2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.10.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1679cb8678405b5590c60c8582a2a86389ea6a154399972969015bc8d255eb50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123803410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44e9800ed4b1689baef503d7de5815ac3c6da5152229b60ace152e09ca65db`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:27:50 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:27:52 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:53 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:28:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:28:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:28:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:28:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:28:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdf0ee48c73ed2d797bb263fa5c515be8ef1ec789f353a364a0cf40f215017b`  
		Last Modified: Tue, 01 Aug 2023 22:29:47 GMT  
		Size: 28.9 MB (28854458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691d97e17ea198f97085162db77c9d7c4fdfc3421d2586ddd774b099f37b8fe`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c36a91e0e00031427dd00e186cdcbaa9016185e1ccc0e53f31f53e5ba0e8f9`  
		Last Modified: Tue, 01 Aug 2023 22:29:45 GMT  
		Size: 1.1 MB (1069966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc871ddb9eeeb88bb9bb38e1be0f754074b9fa46b6bfdc35909b65ea2293ca2`  
		Last Modified: Tue, 01 Aug 2023 22:29:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.10.0-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a75a4c8eabe32a9b3218aca2a1be4c7c54012cf271bb9f6af3c709a92cfa6460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120233383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f51f89ab2b58d3ec549b2f396483e3f925b97f0578cdc6df5189b426bbc370`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_VERSION=9.3.10.0
# Tue, 01 Aug 2023 22:39:43 GMT
ENV JRUBY_SHA256=c78c127e0aa166f257eeab03c4733ba3d96a445314eff7e5dc1f8154d2b5ae45
# Tue, 01 Aug 2023 22:39:44 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:44 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:45 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e0778afb4a6a75e69d9468a16cae18346857ce737929b23cd5e964aabd39a7`  
		Last Modified: Tue, 01 Aug 2023 22:41:34 GMT  
		Size: 28.9 MB (28854381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8c27ed789cda6f2d78b6b345e39bbcb5ee8e2988c646f949647da6ea983d9`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b27794003314ed8fe6e39f58e60cd5f18228296ebf146f6de449d98980e9c`  
		Last Modified: Tue, 01 Aug 2023 22:41:33 GMT  
		Size: 1.1 MB (1069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac17794610b6958bfecf718dc420a2df78f893e32cc6dad79ff0d8d01ec3391`  
		Last Modified: Tue, 01 Aug 2023 22:41:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk11`

```console
$ docker pull jruby@sha256:a941fc4092910c7a12d35574f373f66adfa87b4d4a8bf9cb70ae9818a87715ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:ce789ed9f56181bad90e941d22769c88f1e53e71a86d4ab041503e3f723a8206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227503082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42b2ca3e31b9fe4009babe6f27e57b95301dfa4224f24fc150f123278c56f5b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0ec5cfad5b00a6128754ec510903e08c79f342cf2e18b416d38d2552d09016`  
		Last Modified: Wed, 26 Jul 2023 01:57:11 GMT  
		Size: 29.5 MB (29539338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fac1ec3e238938bbaedcb135f49d76d1180ca537abadf8d7086488b015a9da`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd772265857ac8b5117b3e96c108cc870951b451902eac6a9dfe821b65d0e729`  
		Last Modified: Wed, 26 Jul 2023 01:57:09 GMT  
		Size: 1.1 MB (1100126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eadc8a378daac9136328ad742a707f8a722ec7f0f360eb68fc7fe740c2ac8a6`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:991cfd2764737ebab3d38f0f0d44f7fcaef8b7ca9186a62a451ea894a438f933
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221675004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030e6311d1305af20d2e8469f27343cce30b99c5914b25ea4e5632c7198bfdb`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:32 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87896e85536ba668146a9f372a863686354cb28de682e255cc0d8f78a564dc4`  
		Last Modified: Wed, 26 Jul 2023 01:26:01 GMT  
		Size: 29.5 MB (29539677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec9eaa15d7a03adddf73cb381bec2c371b73bb067fe4c12fc52ab687cbc0d44`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b507a1b34388bed9650a7b96b7f99da9000492b2f18959119ce791d226b08`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 1.1 MB (1100103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17649402895b0eec71a0e356ce4ea1d104a03e978754310f65bb503fec25b14`  
		Last Modified: Wed, 26 Jul 2023 01:25:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk17`

```console
$ docker pull jruby@sha256:b75546574eb04c349e750a96f6a3c9002f2407ca0baab5a1e973ff09798bb810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:193ca668794fde1efedb545f271060b38118514e0d1eaf51785fa14ca183ea08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231190350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937ab75327519400a0f91bcc66dbd5e25cc44de9e818266c6f8c0cff7ca282a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 00:13:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5957ba348ae1f04c4bc185298a949ebafa9aa4c9601e78e2d327526a3c75efa`  
		Last Modified: Wed, 26 Jul 2023 00:14:22 GMT  
		Size: 29.5 MB (29539343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570bef3a25cfc27fa312fbe48615ef79b161cf41a85a898fed49578c0d0a571`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33446f8da514c3301f0e610d4a9cb5b51894b540ba0dcc2ee63ca808b696df29`  
		Last Modified: Wed, 26 Jul 2023 00:14:20 GMT  
		Size: 1.1 MB (1100079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f015df5b6e7603162b39731d24cff69516ea3339eb9c4893a622575e2ffe8049`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bd4e197ee65933d69e5fbbcb90ac7c1120f77edfdcf74f2968097e8b64f4184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228261489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90f7a0ba56f7eed3510f2004448f55b5f091ba02094a320ab6590671916fdb3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 25 Jul 2023 23:33:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:33:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:33:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4410f32115459f628473c85de746fa8482308b2549f71b2b1c65724623c6982`  
		Last Modified: Tue, 25 Jul 2023 23:35:01 GMT  
		Size: 29.5 MB (29539930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac61c5c11785e7077b1199db0dd20cd554beca1e86f0ce3b48ab74e8a0ba38`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25539f95568decc183b4d8e2ed5ba659a6c49fce7355ae8018838e2ac9b49edf`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 1.1 MB (1100121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a41796c1ea3f7c6f0baf6ece6bc9e634feeaa1dde36065f0162a73730e2fca`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jdk8`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre11`

```console
$ docker pull jruby@sha256:139b13e46c20cc52e3241e8b15ff28266b194b94374a15eb7e9346556d165d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:391671fb7cba71b6b929a37836e70ab9451692321116d4a90b68fe982633b8a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129530740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7059f9fb74e5a8f3995a56673b93f5a33d77be2480881496da573f69b0386a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad4be7c23ad938c5647309ec38feecfedfb969522b0a716c6d9641e1def546`  
		Last Modified: Wed, 26 Jul 2023 01:56:58 GMT  
		Size: 29.5 MB (29539912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ecb530fc949ec40f1c43686cc4576a40942881b012cb21dc651bb46640792`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbb6b155b9b7cdf1e7ceea83d3f82bc9af2a57e2d3f17d024876c8d8f272109`  
		Last Modified: Wed, 26 Jul 2023 01:56:56 GMT  
		Size: 1.1 MB (1100123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda6ab8b57ff71a2cfa36cec47d338fe8c78a06c0ad2567f69de8c15fe4ec92e`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4e335b4f6c28a33a11afa6b01bd2903963d0f6835fb87ed285392132b5086e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125293887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efa942d13c0b603bf0672d975b1abddc99b3730bc08b4299b47f74c5b7dd0a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:14 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01635db58f5aea4dbd45f618c7c0aca1067034bfcb2c468749aa7e97dce6141d`  
		Last Modified: Wed, 26 Jul 2023 01:25:47 GMT  
		Size: 29.5 MB (29539954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bd0ff2013c4eaa430be8a1607cb0daf4e12d970dc3b3dd07b8550919979f93`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17ef5720962210438493834c131926df408c549282c0c4b3e06a9fba3030fd`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 1.1 MB (1100096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee10f7b7b9cdfa9be8e1ccb36e13995bf12aa6afab65c79664f220838ffdaf`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4-jre8`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jdk`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jdk11`

```console
$ docker pull jruby@sha256:a941fc4092910c7a12d35574f373f66adfa87b4d4a8bf9cb70ae9818a87715ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:ce789ed9f56181bad90e941d22769c88f1e53e71a86d4ab041503e3f723a8206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227503082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42b2ca3e31b9fe4009babe6f27e57b95301dfa4224f24fc150f123278c56f5b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0ec5cfad5b00a6128754ec510903e08c79f342cf2e18b416d38d2552d09016`  
		Last Modified: Wed, 26 Jul 2023 01:57:11 GMT  
		Size: 29.5 MB (29539338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fac1ec3e238938bbaedcb135f49d76d1180ca537abadf8d7086488b015a9da`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd772265857ac8b5117b3e96c108cc870951b451902eac6a9dfe821b65d0e729`  
		Last Modified: Wed, 26 Jul 2023 01:57:09 GMT  
		Size: 1.1 MB (1100126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eadc8a378daac9136328ad742a707f8a722ec7f0f360eb68fc7fe740c2ac8a6`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:991cfd2764737ebab3d38f0f0d44f7fcaef8b7ca9186a62a451ea894a438f933
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221675004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030e6311d1305af20d2e8469f27343cce30b99c5914b25ea4e5632c7198bfdb`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:32 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87896e85536ba668146a9f372a863686354cb28de682e255cc0d8f78a564dc4`  
		Last Modified: Wed, 26 Jul 2023 01:26:01 GMT  
		Size: 29.5 MB (29539677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec9eaa15d7a03adddf73cb381bec2c371b73bb067fe4c12fc52ab687cbc0d44`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b507a1b34388bed9650a7b96b7f99da9000492b2f18959119ce791d226b08`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 1.1 MB (1100103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17649402895b0eec71a0e356ce4ea1d104a03e978754310f65bb503fec25b14`  
		Last Modified: Wed, 26 Jul 2023 01:25:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jdk17`

```console
$ docker pull jruby@sha256:b75546574eb04c349e750a96f6a3c9002f2407ca0baab5a1e973ff09798bb810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:193ca668794fde1efedb545f271060b38118514e0d1eaf51785fa14ca183ea08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231190350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937ab75327519400a0f91bcc66dbd5e25cc44de9e818266c6f8c0cff7ca282a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 00:13:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5957ba348ae1f04c4bc185298a949ebafa9aa4c9601e78e2d327526a3c75efa`  
		Last Modified: Wed, 26 Jul 2023 00:14:22 GMT  
		Size: 29.5 MB (29539343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570bef3a25cfc27fa312fbe48615ef79b161cf41a85a898fed49578c0d0a571`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33446f8da514c3301f0e610d4a9cb5b51894b540ba0dcc2ee63ca808b696df29`  
		Last Modified: Wed, 26 Jul 2023 00:14:20 GMT  
		Size: 1.1 MB (1100079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f015df5b6e7603162b39731d24cff69516ea3339eb9c4893a622575e2ffe8049`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bd4e197ee65933d69e5fbbcb90ac7c1120f77edfdcf74f2968097e8b64f4184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228261489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90f7a0ba56f7eed3510f2004448f55b5f091ba02094a320ab6590671916fdb3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 25 Jul 2023 23:33:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:33:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:33:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4410f32115459f628473c85de746fa8482308b2549f71b2b1c65724623c6982`  
		Last Modified: Tue, 25 Jul 2023 23:35:01 GMT  
		Size: 29.5 MB (29539930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac61c5c11785e7077b1199db0dd20cd554beca1e86f0ce3b48ab74e8a0ba38`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25539f95568decc183b4d8e2ed5ba659a6c49fce7355ae8018838e2ac9b49edf`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 1.1 MB (1100121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a41796c1ea3f7c6f0baf6ece6bc9e634feeaa1dde36065f0162a73730e2fca`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jdk8`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jre`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jre11`

```console
$ docker pull jruby@sha256:139b13e46c20cc52e3241e8b15ff28266b194b94374a15eb7e9346556d165d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:391671fb7cba71b6b929a37836e70ab9451692321116d4a90b68fe982633b8a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129530740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7059f9fb74e5a8f3995a56673b93f5a33d77be2480881496da573f69b0386a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad4be7c23ad938c5647309ec38feecfedfb969522b0a716c6d9641e1def546`  
		Last Modified: Wed, 26 Jul 2023 01:56:58 GMT  
		Size: 29.5 MB (29539912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ecb530fc949ec40f1c43686cc4576a40942881b012cb21dc651bb46640792`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbb6b155b9b7cdf1e7ceea83d3f82bc9af2a57e2d3f17d024876c8d8f272109`  
		Last Modified: Wed, 26 Jul 2023 01:56:56 GMT  
		Size: 1.1 MB (1100123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda6ab8b57ff71a2cfa36cec47d338fe8c78a06c0ad2567f69de8c15fe4ec92e`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4e335b4f6c28a33a11afa6b01bd2903963d0f6835fb87ed285392132b5086e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125293887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efa942d13c0b603bf0672d975b1abddc99b3730bc08b4299b47f74c5b7dd0a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:14 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01635db58f5aea4dbd45f618c7c0aca1067034bfcb2c468749aa7e97dce6141d`  
		Last Modified: Wed, 26 Jul 2023 01:25:47 GMT  
		Size: 29.5 MB (29539954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bd0ff2013c4eaa430be8a1607cb0daf4e12d970dc3b3dd07b8550919979f93`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17ef5720962210438493834c131926df408c549282c0c4b3e06a9fba3030fd`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 1.1 MB (1100096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee10f7b7b9cdfa9be8e1ccb36e13995bf12aa6afab65c79664f220838ffdaf`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3-jre8`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jdk`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jdk11`

```console
$ docker pull jruby@sha256:a941fc4092910c7a12d35574f373f66adfa87b4d4a8bf9cb70ae9818a87715ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:ce789ed9f56181bad90e941d22769c88f1e53e71a86d4ab041503e3f723a8206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227503082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42b2ca3e31b9fe4009babe6f27e57b95301dfa4224f24fc150f123278c56f5b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:53:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:53:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:53:23 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:55:32 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:33 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daae480059467f2b0a36e532fe779a07360bc5e7ff1eae8bd380a013d9be66d`  
		Last Modified: Wed, 26 Jul 2023 00:57:40 GMT  
		Size: 144.8 MB (144837915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c823d0e77873c206a8df54d8111ec16beb862b8a4380d06744390bab52cb8`  
		Last Modified: Wed, 26 Jul 2023 00:57:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af57d4934d508b4e8dcfe69b51ffbea8ec6b0ba80dfda16d37de2985dfd5edb`  
		Last Modified: Wed, 26 Jul 2023 01:57:10 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0ec5cfad5b00a6128754ec510903e08c79f342cf2e18b416d38d2552d09016`  
		Last Modified: Wed, 26 Jul 2023 01:57:11 GMT  
		Size: 29.5 MB (29539338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fac1ec3e238938bbaedcb135f49d76d1180ca537abadf8d7086488b015a9da`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd772265857ac8b5117b3e96c108cc870951b451902eac6a9dfe821b65d0e729`  
		Last Modified: Wed, 26 Jul 2023 01:57:09 GMT  
		Size: 1.1 MB (1100126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eadc8a378daac9136328ad742a707f8a722ec7f0f360eb68fc7fe740c2ac8a6`  
		Last Modified: Wed, 26 Jul 2023 01:57:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:991cfd2764737ebab3d38f0f0d44f7fcaef8b7ca9186a62a451ea894a438f933
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221675004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030e6311d1305af20d2e8469f27343cce30b99c5914b25ea4e5632c7198bfdb`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='fdf98d94ac3fd49a73a534fd88cf60e757e885c04791d15f76ccfcecb43a25e0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:37:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:19 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 01:24:29 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:29 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:32 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01667d51126eb3547a25ed4ab4d0727aa63d686cfe86a64fc49d6e31bcd8e749`  
		Last Modified: Wed, 26 Jul 2023 00:39:45 GMT  
		Size: 141.6 MB (141571670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba568dc03cb84e46293cb29d636585e3d0f5c390d072fa1314f03d6b2fca2774`  
		Last Modified: Wed, 26 Jul 2023 00:39:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d0f86b943e95fb4937133b7ffc4154835c91ae5a71539a061631a2dd7fb5fe`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 6.0 MB (5996498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87896e85536ba668146a9f372a863686354cb28de682e255cc0d8f78a564dc4`  
		Last Modified: Wed, 26 Jul 2023 01:26:01 GMT  
		Size: 29.5 MB (29539677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec9eaa15d7a03adddf73cb381bec2c371b73bb067fe4c12fc52ab687cbc0d44`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b507a1b34388bed9650a7b96b7f99da9000492b2f18959119ce791d226b08`  
		Last Modified: Wed, 26 Jul 2023 01:25:59 GMT  
		Size: 1.1 MB (1100103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17649402895b0eec71a0e356ce4ea1d104a03e978754310f65bb503fec25b14`  
		Last Modified: Wed, 26 Jul 2023 01:25:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jdk17`

```console
$ docker pull jruby@sha256:b75546574eb04c349e750a96f6a3c9002f2407ca0baab5a1e973ff09798bb810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:193ca668794fde1efedb545f271060b38118514e0d1eaf51785fa14ca183ea08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231190350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937ab75327519400a0f91bcc66dbd5e25cc44de9e818266c6f8c0cff7ca282a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:20:53 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:04 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 00:13:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 00:13:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 00:13:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:12 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 00:13:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 00:13:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 00:13:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 00:13:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 00:13:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08078e9064c587c750374f300707fa21025a3a2ad077a093b0c32792084ac9c`  
		Last Modified: Tue, 25 Jul 2023 22:26:23 GMT  
		Size: 144.8 MB (144780786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375f5661b61ee3e40f25bf14586f0d2ffedaedeb7c2affa1f17e73f672d5d67e`  
		Last Modified: Tue, 25 Jul 2023 22:26:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9abbb24c49407995a097b0c29908555fa69768418c924b2c741717ff11ecc0`  
		Last Modified: Wed, 26 Jul 2023 00:14:21 GMT  
		Size: 7.0 MB (7033988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5957ba348ae1f04c4bc185298a949ebafa9aa4c9601e78e2d327526a3c75efa`  
		Last Modified: Wed, 26 Jul 2023 00:14:22 GMT  
		Size: 29.5 MB (29539343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570bef3a25cfc27fa312fbe48615ef79b161cf41a85a898fed49578c0d0a571`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33446f8da514c3301f0e610d4a9cb5b51894b540ba0dcc2ee63ca808b696df29`  
		Last Modified: Wed, 26 Jul 2023 00:14:20 GMT  
		Size: 1.1 MB (1100079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f015df5b6e7603162b39731d24cff69516ea3339eb9c4893a622575e2ffe8049`  
		Last Modified: Wed, 26 Jul 2023 00:14:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:6bd4e197ee65933d69e5fbbcb90ac7c1120f77edfdcf74f2968097e8b64f4184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228261489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90f7a0ba56f7eed3510f2004448f55b5f091ba02094a320ab6590671916fdb3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:33:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 25 Jul 2023 23:33:54 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 25 Jul 2023 23:33:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 25 Jul 2023 23:33:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:33:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Tue, 25 Jul 2023 23:34:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 25 Jul 2023 23:34:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Jul 2023 23:34:03 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:34:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Jul 2023 23:34:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab09b0d6369460f4b6bbcfdb30ae5c92b12d970b61f12c9ac882d04473e3449`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 6.0 MB (5998609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4410f32115459f628473c85de746fa8482308b2549f71b2b1c65724623c6982`  
		Last Modified: Tue, 25 Jul 2023 23:35:01 GMT  
		Size: 29.5 MB (29539930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac61c5c11785e7077b1199db0dd20cd554beca1e86f0ce3b48ab74e8a0ba38`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25539f95568decc183b4d8e2ed5ba659a6c49fce7355ae8018838e2ac9b49edf`  
		Last Modified: Tue, 25 Jul 2023 23:35:00 GMT  
		Size: 1.1 MB (1100121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a41796c1ea3f7c6f0baf6ece6bc9e634feeaa1dde36065f0162a73730e2fca`  
		Last Modified: Tue, 25 Jul 2023 23:34:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jdk8`

```console
$ docker pull jruby@sha256:0956fefaa738255b3af83c20a283950cc080778943e04f28b984ee49329bd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:644319d9380cc4b61d7615a4fdaf69456722d3af67dd246e8a3ceb6303b8efeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186254755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73a9c53cdc526287a0411248e0166b112278aeb5e418eefd231c1d5ebde67`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:28 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:38 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24841dfb612046bc99e019f8e111a4e6e213ee863092a9c29be743c3284e19f4`  
		Last Modified: Tue, 01 Aug 2023 21:24:35 GMT  
		Size: 103.6 MB (103589049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5337e871aa0682916358ded49c4dcc9a77ab62247692cf79870b3d9768400940`  
		Last Modified: Tue, 01 Aug 2023 21:24:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb594657e1608d02ea90026f2c418bcab630ddb2c724b8eb23df1837b98920bf`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 7.0 MB (7031649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73c9028d936ebb05c70b5a3e59d9c4fe6542f7930ee87010fb915abbaaebe7`  
		Last Modified: Tue, 01 Aug 2023 22:29:21 GMT  
		Size: 29.5 MB (29539907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d3cd3c1ae8383cdb867cacf6bf9d00901d578197718d72a18807cf896463d`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6953926e2b38e8be0d5680330e7f4b7ba3f90d7f37af2dda1e34054074499a0`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 1.1 MB (1100109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f158b5a6c38e95a0f9809ccb46098fbb8d09162ecad886d522cfa8d7602aa25`  
		Last Modified: Tue, 01 Aug 2023 22:29:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:71261be75a193e727f04a5be4560b00b5ad32a8ce7c429438c94e98777c945fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182793136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6d41ab5b3e895964071779d491f48b6c4151635366f65aea9c0f170930c54`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:39:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:39:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:25 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:25 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:27 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:27 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f464a50ffa9d53851d7ba423e766bbfdc0eb7554d0eb4e666371308c0c5e04a`  
		Last Modified: Tue, 01 Aug 2023 21:41:55 GMT  
		Size: 102.7 MB (102689811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846de271f159db5665333363bfc1d584f82fd1b7db9925166ccb9ea27dc60ce`  
		Last Modified: Tue, 01 Aug 2023 21:41:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef72721beb962cd1ffca9dbfa84db55217e5de6cc7669315355223a098233c58`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 6.0 MB (5996479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b38a6583f2dd719b0684908ae343354fd06f24c874f5edeeee4dd50da6b270`  
		Last Modified: Tue, 01 Aug 2023 22:41:08 GMT  
		Size: 29.5 MB (29539701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0cf5e7ac3d33f7fb2c47451766462fabe218541edfe3e2fd12c56d4939bf5`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8806e857ee9f69287be6e054ab45de8151b99c43297746cb103789c6c681a`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 1.1 MB (1100106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad94cb0b365eb36dc48f5c37b375767a23736facc8a681874afdd36232d89469`  
		Last Modified: Tue, 01 Aug 2023 22:41:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jre`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jre11`

```console
$ docker pull jruby@sha256:139b13e46c20cc52e3241e8b15ff28266b194b94374a15eb7e9346556d165d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:391671fb7cba71b6b929a37836e70ab9451692321116d4a90b68fe982633b8a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129530740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7059f9fb74e5a8f3995a56673b93f5a33d77be2480881496da573f69b0386a`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:53:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:54:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:55:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:55:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:55:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:55:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:55:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:55:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:55:20 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:55:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:55:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde9eedfcf905df2b091edc9c91d78dca4b5e2b0bf1ddf3293b268670a53462`  
		Last Modified: Wed, 26 Jul 2023 00:59:25 GMT  
		Size: 46.9 MB (46865103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9366cd6de72cdc95143f1aa2f895bf5972bdb10e8e7acf9dcec2730314e53`  
		Last Modified: Wed, 26 Jul 2023 00:59:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f242f5aa64988ce758f1c32188ae8357df26cf7f74a4f1caae5b82abcae05d`  
		Last Modified: Wed, 26 Jul 2023 01:56:57 GMT  
		Size: 7.0 MB (7031562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad4be7c23ad938c5647309ec38feecfedfb969522b0a716c6d9641e1def546`  
		Last Modified: Wed, 26 Jul 2023 01:56:58 GMT  
		Size: 29.5 MB (29539912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ecb530fc949ec40f1c43686cc4576a40942881b012cb21dc651bb46640792`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbb6b155b9b7cdf1e7ceea83d3f82bc9af2a57e2d3f17d024876c8d8f272109`  
		Last Modified: Wed, 26 Jul 2023 01:56:56 GMT  
		Size: 1.1 MB (1100123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda6ab8b57ff71a2cfa36cec47d338fe8c78a06c0ad2567f69de8c15fe4ec92e`  
		Last Modified: Wed, 26 Jul 2023 01:56:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:4e335b4f6c28a33a11afa6b01bd2903963d0f6835fb87ed285392132b5086e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125293887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efa942d13c0b603bf0672d975b1abddc99b3730bc08b4299b47f74c5b7dd0a3`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 00:37:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:38:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Jul 2023 00:38:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 01:24:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_VERSION=9.4.3.0
# Wed, 26 Jul 2023 01:24:12 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Wed, 26 Jul 2023 01:24:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 26 Jul 2023 01:24:14 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 26 Jul 2023 01:24:20 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 26 Jul 2023 01:24:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Jul 2023 01:24:21 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:24:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Jul 2023 01:24:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a4235397c270e2335b3509f62d601799ccdc3bd51f28d24e2b7bb91de9226f`  
		Last Modified: Wed, 26 Jul 2023 00:41:07 GMT  
		Size: 45.2 MB (45190304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396b3bbd3701767ce04edbb2711d737f7cb2bb166d86dc64d85262c9f4915b08`  
		Last Modified: Wed, 26 Jul 2023 00:41:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd4743bd9a6c51b2ce06814c567e0efe0a5d279f7e3331ef81648263be80d8`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 6.0 MB (5996497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01635db58f5aea4dbd45f618c7c0aca1067034bfcb2c468749aa7e97dce6141d`  
		Last Modified: Wed, 26 Jul 2023 01:25:47 GMT  
		Size: 29.5 MB (29539954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bd0ff2013c4eaa430be8a1607cb0daf4e12d970dc3b3dd07b8550919979f93`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17ef5720962210438493834c131926df408c549282c0c4b3e06a9fba3030fd`  
		Last Modified: Wed, 26 Jul 2023 01:25:46 GMT  
		Size: 1.1 MB (1100096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aee10f7b7b9cdfa9be8e1ccb36e13995bf12aa6afab65c79664f220838ffdaf`  
		Last Modified: Wed, 26 Jul 2023 01:25:45 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.4.3.0-jre8`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.4.3.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.4.3.0-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:cfd91932ce9955f0764d5177bd9de52c62cea5f1fde10536f167deb698fb20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:6ad3add5868f8f8092fa04d42a067730596907a49535c481026f36911165acdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124519021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd649dfef68a78de390a95163656a38a68b7d23ba338ede70d718aa1c7473e8d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:33:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:21:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:21:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:27:07 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:27:07 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:27:09 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:27:09 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:10 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:27:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:27:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:27:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:27:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:27:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c6314534fa2a3b454bddc0f12350fdd16cce9b09f979ce4c7fafd5ec679a69`  
		Last Modified: Tue, 04 Jul 2023 20:38:50 GMT  
		Size: 16.4 MB (16413467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834cc23602939e7ead7280a97ceba183c702c4bea3c83a69f592de734ad7a2c`  
		Last Modified: Tue, 01 Aug 2023 21:26:09 GMT  
		Size: 41.9 MB (41853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88510c7ec326e489a1e4a6823baa370bba41b7341573710a2eca80616138da56`  
		Last Modified: Tue, 01 Aug 2023 21:26:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e31d3363c0a4a86afca11ce50e89fa0d6ed6e2e13432f329d4435b87954353`  
		Last Modified: Tue, 01 Aug 2023 22:28:51 GMT  
		Size: 7.0 MB (7031607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24521de2f24b13b17365a542b22c61cfbe2f602ade14104d25139c7e62ab1e03`  
		Last Modified: Tue, 01 Aug 2023 22:28:52 GMT  
		Size: 29.5 MB (29539920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20922c3b301682a1abc694ddb13321e5ea6e4498d694b6a54626d91222d813b`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc56d9aa51e2ca7568ad3bce2de733c461585aa13b6a53d44615a2c73fcc39`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 1.1 MB (1100113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163d6babd723262c320b1148c6727f8efabf4221b7448134f377545845de4ff`  
		Last Modified: Tue, 01 Aug 2023 22:28:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:10eddf1f4179b5452cc37727848041098ce1702d626f9749275b395bf837cdbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120948843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46883c46cd8364eb05bd7e1826cbb528eafaa09c476232d69c15d532383b173`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:39:28 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:40:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 22:39:09 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_VERSION=9.4.3.0
# Tue, 01 Aug 2023 22:39:09 GMT
ENV JRUBY_SHA256=b097e08c5669e8a188288e113911d12b4ad2bd67a2c209d6dfa8445d63a4d8c9
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Tue, 01 Aug 2023 22:39:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:11 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Tue, 01 Aug 2023 22:39:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Tue, 01 Aug 2023 22:39:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 01 Aug 2023 22:39:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:39:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 01 Aug 2023 22:39:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a6ed3004a374532e52161ba803de458ea0c89faf66c28c12d9858ee1796c1`  
		Last Modified: Tue, 04 Jul 2023 15:36:40 GMT  
		Size: 16.3 MB (16268149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852509c55e7e128b5c053e59e5f23f271d018baeee937d706b714bbd663e532e`  
		Last Modified: Tue, 01 Aug 2023 21:43:05 GMT  
		Size: 40.8 MB (40845613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6552b81246ffd8ccd60d1e2311244e1e1e0a9ab5d4ee8179792a38a257b287f`  
		Last Modified: Tue, 01 Aug 2023 21:43:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd59c8b3e9cce1b86fc90c90f77ba63f9fd5025b76d45179f44f37dd5083b0`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 6.0 MB (5996391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e4ca04127712c3df27c20bdfb8ed3ae62366477565d7443dd5472a3f747b64`  
		Last Modified: Tue, 01 Aug 2023 22:40:40 GMT  
		Size: 29.5 MB (29539711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d4435ce3b44e283b2c3c4187799760911ef5093ebfec51a3f5fb45a2ea0708`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eada08ddb059e9601a8ae40a6c593d22ddfbf178ed2114ef9c1733be5f809f`  
		Last Modified: Tue, 01 Aug 2023 22:40:37 GMT  
		Size: 1.1 MB (1100086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abbb91f34ff1a262ddc4dbcb093e682210b859997a3b477a83720f57478595f`  
		Last Modified: Tue, 01 Aug 2023 22:40:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
