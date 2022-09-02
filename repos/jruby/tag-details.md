<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jruby`

-	[`jruby:9`](#jruby9)
-	[`jruby:9-jdk`](#jruby9-jdk)
-	[`jruby:9-jdk8`](#jruby9-jdk8)
-	[`jruby:9.2`](#jruby92)
-	[`jruby:9.2-jdk`](#jruby92-jdk)
-	[`jruby:9.2-jdk11`](#jruby92-jdk11)
-	[`jruby:9.2-jdk17`](#jruby92-jdk17)
-	[`jruby:9.2-jdk8`](#jruby92-jdk8)
-	[`jruby:9.2-jre`](#jruby92-jre)
-	[`jruby:9.2-jre11`](#jruby92-jre11)
-	[`jruby:9.2-jre8`](#jruby92-jre8)
-	[`jruby:9.2-onbuild`](#jruby92-onbuild)
-	[`jruby:9.2.21`](#jruby9221)
-	[`jruby:9.2.21-jdk`](#jruby9221-jdk)
-	[`jruby:9.2.21-jdk11`](#jruby9221-jdk11)
-	[`jruby:9.2.21-jdk17`](#jruby9221-jdk17)
-	[`jruby:9.2.21-jdk8`](#jruby9221-jdk8)
-	[`jruby:9.2.21-jre`](#jruby9221-jre)
-	[`jruby:9.2.21-jre11`](#jruby9221-jre11)
-	[`jruby:9.2.21-jre8`](#jruby9221-jre8)
-	[`jruby:9.2.21-onbuild`](#jruby9221-onbuild)
-	[`jruby:9.2.21.0`](#jruby92210)
-	[`jruby:9.2.21.0-jdk`](#jruby92210-jdk)
-	[`jruby:9.2.21.0-jdk11`](#jruby92210-jdk11)
-	[`jruby:9.2.21.0-jdk17`](#jruby92210-jdk17)
-	[`jruby:9.2.21.0-jdk8`](#jruby92210-jdk8)
-	[`jruby:9.2.21.0-jre`](#jruby92210-jre)
-	[`jruby:9.2.21.0-jre11`](#jruby92210-jre11)
-	[`jruby:9.2.21.0-jre8`](#jruby92210-jre8)
-	[`jruby:9.2.21.0-onbuild`](#jruby92210-onbuild)
-	[`jruby:9.3`](#jruby93)
-	[`jruby:9.3-jdk`](#jruby93-jdk)
-	[`jruby:9.3-jdk11`](#jruby93-jdk11)
-	[`jruby:9.3-jdk17`](#jruby93-jdk17)
-	[`jruby:9.3-jdk8`](#jruby93-jdk8)
-	[`jruby:9.3-jre`](#jruby93-jre)
-	[`jruby:9.3-jre11`](#jruby93-jre11)
-	[`jruby:9.3-jre8`](#jruby93-jre8)
-	[`jruby:9.3.7`](#jruby937)
-	[`jruby:9.3.7-jdk`](#jruby937-jdk)
-	[`jruby:9.3.7-jdk11`](#jruby937-jdk11)
-	[`jruby:9.3.7-jdk17`](#jruby937-jdk17)
-	[`jruby:9.3.7-jdk8`](#jruby937-jdk8)
-	[`jruby:9.3.7-jre`](#jruby937-jre)
-	[`jruby:9.3.7-jre11`](#jruby937-jre11)
-	[`jruby:9.3.7-jre8`](#jruby937-jre8)
-	[`jruby:9.3.7.0`](#jruby9370)
-	[`jruby:9.3.7.0-jdk`](#jruby9370-jdk)
-	[`jruby:9.3.7.0-jdk11`](#jruby9370-jdk11)
-	[`jruby:9.3.7.0-jdk17`](#jruby9370-jdk17)
-	[`jruby:9.3.7.0-jdk8`](#jruby9370-jdk8)
-	[`jruby:9.3.7.0-jre`](#jruby9370-jre)
-	[`jruby:9.3.7.0-jre11`](#jruby9370-jre11)
-	[`jruby:9.3.7.0-jre8`](#jruby9370-jre8)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk11`

```console
$ docker pull jruby@sha256:d46b667c3b28a7db6b78fc471eb095ca004b94459ba4a53bf72006b8e9b56f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:f994c6c3d205cdc7183aeb6be4d3fcb8d5836e860cd3a4a5e142273adb445874
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278881353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b069418caa3ab32c031a26893854c643e850031688cd31445ce4a3966a33be`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:39 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:40 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:40 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:48 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8431c6c3df733811d535fc43e5dae4a8cdfc066045c8033d554bae76599ee7`  
		Last Modified: Fri, 02 Sep 2022 10:30:58 GMT  
		Size: 27.8 MB (27844735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b227553c53f601f3ae56249504bceff093b1ea32c264d4c2e00772481ddd3b`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1508344139ee175e5b80d231eaaa61b747bab0a5ddcbbaf9c1c15cfbc8d5325f`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 1.1 MB (1065003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506f358b046c79a8d412e41c0619714c10158344dc63f2035553d0af5d45eb15`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk17`

```console
$ docker pull jruby@sha256:8dde77edd288167d06acfccef9cff8be4468833d67cc6e654e4c4e371f66d20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:c9cab20ab7ba8ff31a1361702716ce7677cac26e3dd361a7d2e9ec1a6bd693ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276651588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42b6036760cfe2c903aa6536d82c8d1f2a464b71a14bed77eac6d4571fd760`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:54 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:27:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:27:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:27:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:27:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71665f13576ab12fef004a0d76fb73a1c61a9d546763ea2f8bed5c5db855b7a0`  
		Last Modified: Fri, 02 Sep 2022 10:31:13 GMT  
		Size: 27.8 MB (27844789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8283d71972d2c2b708df872e0ecd80d4e68e182b9d28b075775cde773bd63d`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188061e5c02cc7ad8decb0571ab21ce77561d541f161ba6e45107c1055d6acd5`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 1.1 MB (1064980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc28191e7e3c29a710f84c5a89ab91e5a42762e05240ea5cec384cf36b3a6ee`  
		Last Modified: Fri, 02 Sep 2022 10:31:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk8`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre11`

```console
$ docker pull jruby@sha256:5f27fe1c387b9197562b856c3a26b6d717db2db0f4447d61c53a0771a67f4e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:1c238bf43dce18e92359a02dd766c29a03c9737d73f60d6179a12ad595760482
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127250367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b8ab4497cd182d673fb9660a063813930f53cc9524128e58bb68b053d993b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a623dc9d17f85a3324c7edfa0339836ae0b861e99b829aaa0fe5a3123906a0a9`  
		Last Modified: Fri, 02 Sep 2022 10:30:44 GMT  
		Size: 27.8 MB (27844718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7290982960fe89b8ca68ea1c1c403100c7b16f0f0aba252cb6c0f81496935`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020d4d1fbdba7d973e1f6957c40b894b8f892aa8c820af15a4b18e2a4f806c4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:42 GMT  
		Size: 1.1 MB (1064984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2ac6dcee6097c87487fdbe47c30c474b34bcfea92b50cde3db6d14203de04`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre8`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-onbuild`

```console
$ docker pull jruby@sha256:9e1b31181dabe13276bdf88a6197ca14471ca31bf079307724f7041cb593917d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3054a535e6be949c681a22c4cbed9e53c917d373687325fb97deff07e1ec85ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c6aa0ad1fd92dff4047880283a81aad52855b93e486b5c1a6b128856e4f79d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
# Fri, 02 Sep 2022 10:27:06 GMT
RUN mkdir -p /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
WORKDIR /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD RUN bundle install --system
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2858d097b87b2673585fd7abedc0ad35c84b10a4a66c108b2a47cfc969a5d95`  
		Last Modified: Fri, 02 Sep 2022 10:31:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk11`

```console
$ docker pull jruby@sha256:d46b667c3b28a7db6b78fc471eb095ca004b94459ba4a53bf72006b8e9b56f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:f994c6c3d205cdc7183aeb6be4d3fcb8d5836e860cd3a4a5e142273adb445874
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278881353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b069418caa3ab32c031a26893854c643e850031688cd31445ce4a3966a33be`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:39 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:40 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:40 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:48 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8431c6c3df733811d535fc43e5dae4a8cdfc066045c8033d554bae76599ee7`  
		Last Modified: Fri, 02 Sep 2022 10:30:58 GMT  
		Size: 27.8 MB (27844735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b227553c53f601f3ae56249504bceff093b1ea32c264d4c2e00772481ddd3b`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1508344139ee175e5b80d231eaaa61b747bab0a5ddcbbaf9c1c15cfbc8d5325f`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 1.1 MB (1065003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506f358b046c79a8d412e41c0619714c10158344dc63f2035553d0af5d45eb15`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk17`

```console
$ docker pull jruby@sha256:8dde77edd288167d06acfccef9cff8be4468833d67cc6e654e4c4e371f66d20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:c9cab20ab7ba8ff31a1361702716ce7677cac26e3dd361a7d2e9ec1a6bd693ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276651588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42b6036760cfe2c903aa6536d82c8d1f2a464b71a14bed77eac6d4571fd760`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:54 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:27:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:27:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:27:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:27:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71665f13576ab12fef004a0d76fb73a1c61a9d546763ea2f8bed5c5db855b7a0`  
		Last Modified: Fri, 02 Sep 2022 10:31:13 GMT  
		Size: 27.8 MB (27844789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8283d71972d2c2b708df872e0ecd80d4e68e182b9d28b075775cde773bd63d`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188061e5c02cc7ad8decb0571ab21ce77561d541f161ba6e45107c1055d6acd5`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 1.1 MB (1064980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc28191e7e3c29a710f84c5a89ab91e5a42762e05240ea5cec384cf36b3a6ee`  
		Last Modified: Fri, 02 Sep 2022 10:31:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk8`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre11`

```console
$ docker pull jruby@sha256:5f27fe1c387b9197562b856c3a26b6d717db2db0f4447d61c53a0771a67f4e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:1c238bf43dce18e92359a02dd766c29a03c9737d73f60d6179a12ad595760482
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127250367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b8ab4497cd182d673fb9660a063813930f53cc9524128e58bb68b053d993b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a623dc9d17f85a3324c7edfa0339836ae0b861e99b829aaa0fe5a3123906a0a9`  
		Last Modified: Fri, 02 Sep 2022 10:30:44 GMT  
		Size: 27.8 MB (27844718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7290982960fe89b8ca68ea1c1c403100c7b16f0f0aba252cb6c0f81496935`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020d4d1fbdba7d973e1f6957c40b894b8f892aa8c820af15a4b18e2a4f806c4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:42 GMT  
		Size: 1.1 MB (1064984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2ac6dcee6097c87487fdbe47c30c474b34bcfea92b50cde3db6d14203de04`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre8`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-onbuild`

```console
$ docker pull jruby@sha256:9e1b31181dabe13276bdf88a6197ca14471ca31bf079307724f7041cb593917d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3054a535e6be949c681a22c4cbed9e53c917d373687325fb97deff07e1ec85ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c6aa0ad1fd92dff4047880283a81aad52855b93e486b5c1a6b128856e4f79d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
# Fri, 02 Sep 2022 10:27:06 GMT
RUN mkdir -p /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
WORKDIR /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD RUN bundle install --system
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2858d097b87b2673585fd7abedc0ad35c84b10a4a66c108b2a47cfc969a5d95`  
		Last Modified: Fri, 02 Sep 2022 10:31:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk11`

```console
$ docker pull jruby@sha256:d46b667c3b28a7db6b78fc471eb095ca004b94459ba4a53bf72006b8e9b56f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:f994c6c3d205cdc7183aeb6be4d3fcb8d5836e860cd3a4a5e142273adb445874
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278881353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b069418caa3ab32c031a26893854c643e850031688cd31445ce4a3966a33be`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:37 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:39 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:40 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:40 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:48 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8431c6c3df733811d535fc43e5dae4a8cdfc066045c8033d554bae76599ee7`  
		Last Modified: Fri, 02 Sep 2022 10:30:58 GMT  
		Size: 27.8 MB (27844735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b227553c53f601f3ae56249504bceff093b1ea32c264d4c2e00772481ddd3b`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1508344139ee175e5b80d231eaaa61b747bab0a5ddcbbaf9c1c15cfbc8d5325f`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 1.1 MB (1065003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506f358b046c79a8d412e41c0619714c10158344dc63f2035553d0af5d45eb15`  
		Last Modified: Fri, 02 Sep 2022 10:30:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk17`

```console
$ docker pull jruby@sha256:8dde77edd288167d06acfccef9cff8be4468833d67cc6e654e4c4e371f66d20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:c9cab20ab7ba8ff31a1361702716ce7677cac26e3dd361a7d2e9ec1a6bd693ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276651588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42b6036760cfe2c903aa6536d82c8d1f2a464b71a14bed77eac6d4571fd760`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:52 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:54 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:54 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:27:02 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:27:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:27:02 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:27:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:27:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71665f13576ab12fef004a0d76fb73a1c61a9d546763ea2f8bed5c5db855b7a0`  
		Last Modified: Fri, 02 Sep 2022 10:31:13 GMT  
		Size: 27.8 MB (27844789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8283d71972d2c2b708df872e0ecd80d4e68e182b9d28b075775cde773bd63d`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188061e5c02cc7ad8decb0571ab21ce77561d541f161ba6e45107c1055d6acd5`  
		Last Modified: Fri, 02 Sep 2022 10:31:11 GMT  
		Size: 1.1 MB (1064980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc28191e7e3c29a710f84c5a89ab91e5a42762e05240ea5cec384cf36b3a6ee`  
		Last Modified: Fri, 02 Sep 2022 10:31:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk8`

```console
$ docker pull jruby@sha256:ed23fef52ab14a3869588d503e7b6176d516babf009664d731b3a578a659550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:c5cce6bdb5a7975f53eb71ce350be386edf98381862bf16d14e23baa2aeb27af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7768d70d8a8c7344eccb17bbbd910d7dc70a2390c4d3b924453ec36b3dd8632e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre11`

```console
$ docker pull jruby@sha256:5f27fe1c387b9197562b856c3a26b6d717db2db0f4447d61c53a0771a67f4e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:1c238bf43dce18e92359a02dd766c29a03c9737d73f60d6179a12ad595760482
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127250367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b8ab4497cd182d673fb9660a063813930f53cc9524128e58bb68b053d993b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:23 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:34 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:34 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a623dc9d17f85a3324c7edfa0339836ae0b861e99b829aaa0fe5a3123906a0a9`  
		Last Modified: Fri, 02 Sep 2022 10:30:44 GMT  
		Size: 27.8 MB (27844718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7290982960fe89b8ca68ea1c1c403100c7b16f0f0aba252cb6c0f81496935`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020d4d1fbdba7d973e1f6957c40b894b8f892aa8c820af15a4b18e2a4f806c4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:42 GMT  
		Size: 1.1 MB (1064984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2ac6dcee6097c87487fdbe47c30c474b34bcfea92b50cde3db6d14203de04`  
		Last Modified: Fri, 02 Sep 2022 10:30:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre8`

```console
$ docker pull jruby@sha256:babe23366deaedc9959d9d145578fab71bd2d054e01c869905cea3743a9e5247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:1b03ea024c4d28c591ab26f8e2e6eb3ec1b4ab68209818034cf5522cfc9d20d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122560681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009cd831fe2e90f9be513f6aa777bc505f3c1d0c20d12d738a93b3cfac492a9b`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:25:53 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:25:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:56 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:04 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ab179fbe707e3c004376d7508e8d3db641d22f933bab0e3ae4aa2cae391f4`  
		Last Modified: Fri, 02 Sep 2022 10:29:52 GMT  
		Size: 27.8 MB (27844753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91974806af4d4f3340154f251762e5324fa792f29e89acc4d262a2ab9d85a01c`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927f2d3b9f85b32ae768802db74ed8861f675aca8e7a1f23bc0bbef9ae75fa96`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 1.1 MB (1064998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d297e40ad987ff2cc5b3a8a7c2e222acafd6a913835fb1a9278efccb756af`  
		Last Modified: Fri, 02 Sep 2022 10:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-onbuild`

```console
$ docker pull jruby@sha256:9e1b31181dabe13276bdf88a6197ca14471ca31bf079307724f7041cb593917d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3054a535e6be949c681a22c4cbed9e53c917d373687325fb97deff07e1ec85ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c6aa0ad1fd92dff4047880283a81aad52855b93e486b5c1a6b128856e4f79d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_VERSION=9.2.21.0
# Fri, 02 Sep 2022 10:26:09 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Fri, 02 Sep 2022 10:26:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:26:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:26:19 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:26:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:26:20 GMT
CMD ["irb"]
# Fri, 02 Sep 2022 10:27:06 GMT
RUN mkdir -p /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
WORKDIR /usr/src/app
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD RUN bundle install --system
# Fri, 02 Sep 2022 10:27:06 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d7921e81abf033560a237fe1c651b646a4344a75050da7513299238a937e6`  
		Last Modified: Fri, 02 Sep 2022 10:30:22 GMT  
		Size: 27.8 MB (27844702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57e6dfbe29529fe49853a5c5014faa669131b7f5614070abf5f371f2ef2f77`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d70dbe62e51b2e1e551d384f23650e50019dcdb27bbb57db9182c3e75ef4a`  
		Last Modified: Fri, 02 Sep 2022 10:30:20 GMT  
		Size: 1.1 MB (1064974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062ef2ca603786a8d07d87f2628f894b5f1c909f29cc4fea1b40bf1126508c78`  
		Last Modified: Fri, 02 Sep 2022 10:30:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2858d097b87b2673585fd7abedc0ad35c84b10a4a66c108b2a47cfc969a5d95`  
		Last Modified: Fri, 02 Sep 2022 10:31:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:e58b826220f48ead7afd3baa45797fe0f75d2a6f243743998eb47a77ab73d82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:a20c4fb237522d3f845e26a226372b4032e51c45036620c65a4d566e81492d78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278820425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1357bafae48055033b12a388904890faa7f57cff6901706873bd8fa20099cd8e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e931fa8b47480bd2656820dea66104d26af7fbedb0a1bf2bef7d9ba6c1463c7`  
		Last Modified: Fri, 02 Sep 2022 10:29:24 GMT  
		Size: 27.8 MB (27783701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65e8103a60f1b477ea22e0492f4dd24893c1a63c0b40bad1c7f6e8f796a8e40`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18801aac9857caba38832ccedcfda81c4f1b0714670be1efbe75d8068e17d24c`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b5f8c4b65ae645562d92719e15115a57a522b66a7bcab361ecf29728b9159a`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc6f1c91b3928e67f03ddbac00c757eccd3d9ac0276f621fda797a0750b62e5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272773622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2142b458ba20ab671f513372c22dbe3da187662390f412b05fec63aa037923dc`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:57:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:57:30 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:07 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:07 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:08 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:22 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:25 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:30:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38282daf13041b34e7a275ffe45ff83d490e7da74d3e4912181e19d2e3a8c052`  
		Last Modified: Fri, 02 Sep 2022 05:05:34 GMT  
		Size: 194.9 MB (194877344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099efc1763f8fefb84765e0a0f7b64c5e239caadcea844e881e9c2aad6cec6ad`  
		Last Modified: Fri, 02 Sep 2022 05:05:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb10249e7079bcafd05179dd57b8abf402d2e6d1b2f42b1cf986f43c83963f`  
		Last Modified: Fri, 02 Sep 2022 12:33:44 GMT  
		Size: 5.6 MB (5640810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9da22106580f98e4f02b889f375ba1d318c406d1b9c6f3b39d758912c3b9df`  
		Last Modified: Fri, 02 Sep 2022 12:33:45 GMT  
		Size: 27.8 MB (27782331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b39a60a7a1bbca1283083d0053c4a1d1100fcb540073506107917fb7a73bd`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ee02e207d9e30946695786af377b62d8f42de1798a8ca4a652866d9027d489`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 1.1 MB (1063987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d8789b32bbbde8435f8d05a97d8faeaf2ba03044568987f1d46561c6d0f7db`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:e82d29944d7bbb291dffabdaa578f5d44a7dc393682e32ea155a74e2fbc6a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:e70c98af12f9b29bb6781be4cf42a8c51b57637d9c9e2faa9bd97cc9860b1de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276590589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970f6b72e054f17e39e81d83bc9c83c30ecce2694887dd8f1da8885a7442101c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:41 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:42 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81528ad41a9e2947623353a9b9fc828613acf3383a2fa342c2fd167b85144529`  
		Last Modified: Fri, 02 Sep 2022 10:29:38 GMT  
		Size: 27.8 MB (27783653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5910f1bcb118a1b8e00e00b62b5f011698f00f4bcc539785d2574a953412c5e0`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e87eb4dab1b8a835a631a4dc3472850410612472c2f117e23495ce6469ddee`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 1.1 MB (1065119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643b0884b141fc75d95ea26d17a99341ba40a473e80d76565fb48843be0cecbe`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:c73312e4997103934bc6ab8384b297b93de26b082e7b712acb1a81329eccfae8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273418324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc7124c8a3a1ecb17312e1537ffd0fed72a3168a87ef1bbf1687e7af56f2497`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:58:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:58:47 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 04:59:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:59:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:59:04 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:43 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:44 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:58 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:01 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:31:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:31:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acfbc542a09b96c46a1e01db8b85890c47a99e4b81a47aaaefb32912107321d`  
		Last Modified: Fri, 02 Sep 2022 05:07:16 GMT  
		Size: 20.8 MB (20824963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3638142e41ead8a251d77bce24bae1e354bc1333cda5e68f87b7e72f16966d`  
		Last Modified: Fri, 02 Sep 2022 05:07:29 GMT  
		Size: 190.9 MB (190911792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16910885b6fde73e4df30796acc81fe0f4869c66a8e58c655ab35ffde6e19319`  
		Last Modified: Fri, 02 Sep 2022 05:07:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b3e3e67751cfa39fb723e8ee47699095c8391142b398714d0fa6a653a6e4b2`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 5.6 MB (5642984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd6922c9abe3c59ea704f28cf6930d11444bc31aa111d7ced7eb96ba97d81ac`  
		Last Modified: Fri, 02 Sep 2022 12:34:02 GMT  
		Size: 27.8 MB (27782312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77cd1cc39899f685ab213dd59e0118acb883d3b1731585c90c3430f6aa1756`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896eaca6d7996bb57c3b5ec364fb24e71197813972ed542981d3252f540a5988`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 1.1 MB (1063958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68f6bc7839e5a951ef7151c7989756877fb0c5103e67e8bbe68c36db7aac737`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:6278ac5de324ecf4dbe7fd6a7070e4ba38627250279da26b3e461346d3a9ee37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:8c49083c918e0392f24856f95070c1a943a5240642d3a52df7d6a992503b9755
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127189519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc2897e5f88a80cc50145e974e9c8505f152df42c8eb465420561ddbd1527d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:10 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd45f6b655625b189ae2d6ea8ad7912e7accb6a9ee085901f1a1062f5b0611f`  
		Last Modified: Fri, 02 Sep 2022 10:29:10 GMT  
		Size: 27.8 MB (27783727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b9cacf19b853994fd2fc07910df21ba7216958f07e8d32ca3a3dce516ad2e`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf32baa17033337036f1da7036898c12ae0673243daa02b35784270c8fe45fa6`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 1.1 MB (1065130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247a3daa1c4c7b1799d514a31a07cf2be94d4489add7cacab164bd34dfe1466a`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:28eeb4ab70473e011d3b18704ef374afcbf1412b4b6019b64f2f3e3947bb4e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122723320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e99e051cd211d5b0fa32a278744b96588d03e7e5645d3df18ab53adffc9848`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:58:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:58:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 12:29:30 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:29:30 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:29:31 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:29:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:29:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db301fee8d91c824e142c1d38d51b84ff501ef078dfc46ab78ebce098e6d819`  
		Last Modified: Fri, 02 Sep 2022 05:06:43 GMT  
		Size: 44.8 MB (44827029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d551363a43231a26706abc066d3ee44f28f4b1e284b9aaceb2510b60a9fa926e`  
		Last Modified: Fri, 02 Sep 2022 05:06:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a061ba7f23bd4d7daaa60d76a7fc5478f3b39f5cc894bbd460ccd909e7d53`  
		Last Modified: Fri, 02 Sep 2022 12:33:28 GMT  
		Size: 5.6 MB (5640820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f43a23d7543a5799346bd77b9ad2ed117c64e9a5af9923d9752680ded743b5`  
		Last Modified: Fri, 02 Sep 2022 12:33:29 GMT  
		Size: 27.8 MB (27782321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc8c87e94acdc58294e3735cdf0e5af773671e8ebc5401ebcb7565b81e987c4`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b25fbf7c4e17872b68990eeb197cf03aec38c991246b6cc733829724751488`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 1.1 MB (1064001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42c4ed4fb6c6831041a7828d638f050cf9a79f1234bec09f27592984060f50`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk11`

```console
$ docker pull jruby@sha256:e58b826220f48ead7afd3baa45797fe0f75d2a6f243743998eb47a77ab73d82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:a20c4fb237522d3f845e26a226372b4032e51c45036620c65a4d566e81492d78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278820425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1357bafae48055033b12a388904890faa7f57cff6901706873bd8fa20099cd8e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e931fa8b47480bd2656820dea66104d26af7fbedb0a1bf2bef7d9ba6c1463c7`  
		Last Modified: Fri, 02 Sep 2022 10:29:24 GMT  
		Size: 27.8 MB (27783701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65e8103a60f1b477ea22e0492f4dd24893c1a63c0b40bad1c7f6e8f796a8e40`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18801aac9857caba38832ccedcfda81c4f1b0714670be1efbe75d8068e17d24c`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b5f8c4b65ae645562d92719e15115a57a522b66a7bcab361ecf29728b9159a`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc6f1c91b3928e67f03ddbac00c757eccd3d9ac0276f621fda797a0750b62e5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272773622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2142b458ba20ab671f513372c22dbe3da187662390f412b05fec63aa037923dc`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:57:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:57:30 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:07 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:07 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:08 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:22 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:25 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:30:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38282daf13041b34e7a275ffe45ff83d490e7da74d3e4912181e19d2e3a8c052`  
		Last Modified: Fri, 02 Sep 2022 05:05:34 GMT  
		Size: 194.9 MB (194877344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099efc1763f8fefb84765e0a0f7b64c5e239caadcea844e881e9c2aad6cec6ad`  
		Last Modified: Fri, 02 Sep 2022 05:05:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb10249e7079bcafd05179dd57b8abf402d2e6d1b2f42b1cf986f43c83963f`  
		Last Modified: Fri, 02 Sep 2022 12:33:44 GMT  
		Size: 5.6 MB (5640810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9da22106580f98e4f02b889f375ba1d318c406d1b9c6f3b39d758912c3b9df`  
		Last Modified: Fri, 02 Sep 2022 12:33:45 GMT  
		Size: 27.8 MB (27782331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b39a60a7a1bbca1283083d0053c4a1d1100fcb540073506107917fb7a73bd`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ee02e207d9e30946695786af377b62d8f42de1798a8ca4a652866d9027d489`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 1.1 MB (1063987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d8789b32bbbde8435f8d05a97d8faeaf2ba03044568987f1d46561c6d0f7db`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk17`

```console
$ docker pull jruby@sha256:e82d29944d7bbb291dffabdaa578f5d44a7dc393682e32ea155a74e2fbc6a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:e70c98af12f9b29bb6781be4cf42a8c51b57637d9c9e2faa9bd97cc9860b1de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276590589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970f6b72e054f17e39e81d83bc9c83c30ecce2694887dd8f1da8885a7442101c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:41 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:42 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81528ad41a9e2947623353a9b9fc828613acf3383a2fa342c2fd167b85144529`  
		Last Modified: Fri, 02 Sep 2022 10:29:38 GMT  
		Size: 27.8 MB (27783653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5910f1bcb118a1b8e00e00b62b5f011698f00f4bcc539785d2574a953412c5e0`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e87eb4dab1b8a835a631a4dc3472850410612472c2f117e23495ce6469ddee`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 1.1 MB (1065119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643b0884b141fc75d95ea26d17a99341ba40a473e80d76565fb48843be0cecbe`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:c73312e4997103934bc6ab8384b297b93de26b082e7b712acb1a81329eccfae8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273418324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc7124c8a3a1ecb17312e1537ffd0fed72a3168a87ef1bbf1687e7af56f2497`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:58:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:58:47 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 04:59:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:59:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:59:04 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:43 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:44 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:58 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:01 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:31:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:31:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acfbc542a09b96c46a1e01db8b85890c47a99e4b81a47aaaefb32912107321d`  
		Last Modified: Fri, 02 Sep 2022 05:07:16 GMT  
		Size: 20.8 MB (20824963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3638142e41ead8a251d77bce24bae1e354bc1333cda5e68f87b7e72f16966d`  
		Last Modified: Fri, 02 Sep 2022 05:07:29 GMT  
		Size: 190.9 MB (190911792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16910885b6fde73e4df30796acc81fe0f4869c66a8e58c655ab35ffde6e19319`  
		Last Modified: Fri, 02 Sep 2022 05:07:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b3e3e67751cfa39fb723e8ee47699095c8391142b398714d0fa6a653a6e4b2`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 5.6 MB (5642984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd6922c9abe3c59ea704f28cf6930d11444bc31aa111d7ced7eb96ba97d81ac`  
		Last Modified: Fri, 02 Sep 2022 12:34:02 GMT  
		Size: 27.8 MB (27782312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77cd1cc39899f685ab213dd59e0118acb883d3b1731585c90c3430f6aa1756`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896eaca6d7996bb57c3b5ec364fb24e71197813972ed542981d3252f540a5988`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 1.1 MB (1063958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68f6bc7839e5a951ef7151c7989756877fb0c5103e67e8bbe68c36db7aac737`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk8`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jre` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre11`

```console
$ docker pull jruby@sha256:6278ac5de324ecf4dbe7fd6a7070e4ba38627250279da26b3e461346d3a9ee37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:8c49083c918e0392f24856f95070c1a943a5240642d3a52df7d6a992503b9755
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127189519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc2897e5f88a80cc50145e974e9c8505f152df42c8eb465420561ddbd1527d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:10 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd45f6b655625b189ae2d6ea8ad7912e7accb6a9ee085901f1a1062f5b0611f`  
		Last Modified: Fri, 02 Sep 2022 10:29:10 GMT  
		Size: 27.8 MB (27783727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b9cacf19b853994fd2fc07910df21ba7216958f07e8d32ca3a3dce516ad2e`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf32baa17033337036f1da7036898c12ae0673243daa02b35784270c8fe45fa6`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 1.1 MB (1065130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247a3daa1c4c7b1799d514a31a07cf2be94d4489add7cacab164bd34dfe1466a`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:28eeb4ab70473e011d3b18704ef374afcbf1412b4b6019b64f2f3e3947bb4e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122723320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e99e051cd211d5b0fa32a278744b96588d03e7e5645d3df18ab53adffc9848`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:58:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:58:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 12:29:30 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:29:30 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:29:31 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:29:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:29:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db301fee8d91c824e142c1d38d51b84ff501ef078dfc46ab78ebce098e6d819`  
		Last Modified: Fri, 02 Sep 2022 05:06:43 GMT  
		Size: 44.8 MB (44827029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d551363a43231a26706abc066d3ee44f28f4b1e284b9aaceb2510b60a9fa926e`  
		Last Modified: Fri, 02 Sep 2022 05:06:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a061ba7f23bd4d7daaa60d76a7fc5478f3b39f5cc894bbd460ccd909e7d53`  
		Last Modified: Fri, 02 Sep 2022 12:33:28 GMT  
		Size: 5.6 MB (5640820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f43a23d7543a5799346bd77b9ad2ed117c64e9a5af9923d9752680ded743b5`  
		Last Modified: Fri, 02 Sep 2022 12:33:29 GMT  
		Size: 27.8 MB (27782321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc8c87e94acdc58294e3735cdf0e5af773671e8ebc5401ebcb7565b81e987c4`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b25fbf7c4e17872b68990eeb197cf03aec38c991246b6cc733829724751488`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 1.1 MB (1064001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42c4ed4fb6c6831041a7828d638f050cf9a79f1234bec09f27592984060f50`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre8`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk11`

```console
$ docker pull jruby@sha256:e58b826220f48ead7afd3baa45797fe0f75d2a6f243743998eb47a77ab73d82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:a20c4fb237522d3f845e26a226372b4032e51c45036620c65a4d566e81492d78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278820425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1357bafae48055033b12a388904890faa7f57cff6901706873bd8fa20099cd8e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:23:29 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:19 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a078d5128a24e03737568ec1e82b00a718ebee2b2d78a0f1e3f362a48490520`  
		Last Modified: Fri, 02 Sep 2022 05:29:41 GMT  
		Size: 198.1 MB (198129181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc5061c60d48669d71388829f9dbd92de8cc47237595c5ff56d5db4e71ac97a`  
		Last Modified: Fri, 02 Sep 2022 05:29:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c961f2e5fa0598bd9e6dc7637697a1f6cd5b90fd76bd65fe09e34796d2c2`  
		Last Modified: Fri, 02 Sep 2022 10:29:23 GMT  
		Size: 6.9 MB (6915892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e931fa8b47480bd2656820dea66104d26af7fbedb0a1bf2bef7d9ba6c1463c7`  
		Last Modified: Fri, 02 Sep 2022 10:29:24 GMT  
		Size: 27.8 MB (27783701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65e8103a60f1b477ea22e0492f4dd24893c1a63c0b40bad1c7f6e8f796a8e40`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18801aac9857caba38832ccedcfda81c4f1b0714670be1efbe75d8068e17d24c`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b5f8c4b65ae645562d92719e15115a57a522b66a7bcab361ecf29728b9159a`  
		Last Modified: Fri, 02 Sep 2022 10:29:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bc6f1c91b3928e67f03ddbac00c757eccd3d9ac0276f621fda797a0750b62e5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272773622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2142b458ba20ab671f513372c22dbe3da187662390f412b05fec63aa037923dc`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:57:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:57:30 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:07 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:07 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:08 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:11 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:11 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:22 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:30:25 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:30:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38282daf13041b34e7a275ffe45ff83d490e7da74d3e4912181e19d2e3a8c052`  
		Last Modified: Fri, 02 Sep 2022 05:05:34 GMT  
		Size: 194.9 MB (194877344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099efc1763f8fefb84765e0a0f7b64c5e239caadcea844e881e9c2aad6cec6ad`  
		Last Modified: Fri, 02 Sep 2022 05:05:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb10249e7079bcafd05179dd57b8abf402d2e6d1b2f42b1cf986f43c83963f`  
		Last Modified: Fri, 02 Sep 2022 12:33:44 GMT  
		Size: 5.6 MB (5640810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9da22106580f98e4f02b889f375ba1d318c406d1b9c6f3b39d758912c3b9df`  
		Last Modified: Fri, 02 Sep 2022 12:33:45 GMT  
		Size: 27.8 MB (27782331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b39a60a7a1bbca1283083d0053c4a1d1100fcb540073506107917fb7a73bd`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ee02e207d9e30946695786af377b62d8f42de1798a8ca4a652866d9027d489`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 1.1 MB (1063987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d8789b32bbbde8435f8d05a97d8faeaf2ba03044568987f1d46561c6d0f7db`  
		Last Modified: Fri, 02 Sep 2022 12:33:43 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk17`

```console
$ docker pull jruby@sha256:e82d29944d7bbb291dffabdaa578f5d44a7dc393682e32ea155a74e2fbc6a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:e70c98af12f9b29bb6781be4cf42a8c51b57637d9c9e2faa9bd97cc9860b1de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276590589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970f6b72e054f17e39e81d83bc9c83c30ecce2694887dd8f1da8885a7442101c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:24:27 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:24:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 05:24:39 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 10:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:25:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:41 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:42 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5511391049b7fe5160b78ebae36e40eef43734a07d246dc389dff107a1d22`  
		Last Modified: Fri, 02 Sep 2022 05:30:57 GMT  
		Size: 20.1 MB (20104278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802306a4ec60975d4ea06f4af6b6fb48eebab54f0e842b3e419636f577d18aa`  
		Last Modified: Fri, 02 Sep 2022 05:31:08 GMT  
		Size: 192.1 MB (192146053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9871e921a16ac6bfb91341dba0e704435039616267174bf49031b5669e8e17`  
		Last Modified: Fri, 02 Sep 2022 05:30:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e76c2fb6b725050e0b46366dd52ffa5b258de328ba8be40f32b3dc1f78b8c2c`  
		Last Modified: Fri, 02 Sep 2022 10:29:37 GMT  
		Size: 6.9 MB (6918226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81528ad41a9e2947623353a9b9fc828613acf3383a2fa342c2fd167b85144529`  
		Last Modified: Fri, 02 Sep 2022 10:29:38 GMT  
		Size: 27.8 MB (27783653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5910f1bcb118a1b8e00e00b62b5f011698f00f4bcc539785d2574a953412c5e0`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e87eb4dab1b8a835a631a4dc3472850410612472c2f117e23495ce6469ddee`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 1.1 MB (1065119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643b0884b141fc75d95ea26d17a99341ba40a473e80d76565fb48843be0cecbe`  
		Last Modified: Fri, 02 Sep 2022 10:29:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:c73312e4997103934bc6ab8384b297b93de26b082e7b712acb1a81329eccfae8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273418324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc7124c8a3a1ecb17312e1537ffd0fed72a3168a87ef1bbf1687e7af56f2497`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:58:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:58:47 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 04:59:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:59:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 04:59:04 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 12:30:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:30:43 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:30:44 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:30:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:30:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:30:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:30:58 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:30:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:31:01 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:31:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:31:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acfbc542a09b96c46a1e01db8b85890c47a99e4b81a47aaaefb32912107321d`  
		Last Modified: Fri, 02 Sep 2022 05:07:16 GMT  
		Size: 20.8 MB (20824963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3638142e41ead8a251d77bce24bae1e354bc1333cda5e68f87b7e72f16966d`  
		Last Modified: Fri, 02 Sep 2022 05:07:29 GMT  
		Size: 190.9 MB (190911792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16910885b6fde73e4df30796acc81fe0f4869c66a8e58c655ab35ffde6e19319`  
		Last Modified: Fri, 02 Sep 2022 05:07:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b3e3e67751cfa39fb723e8ee47699095c8391142b398714d0fa6a653a6e4b2`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 5.6 MB (5642984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd6922c9abe3c59ea704f28cf6930d11444bc31aa111d7ced7eb96ba97d81ac`  
		Last Modified: Fri, 02 Sep 2022 12:34:02 GMT  
		Size: 27.8 MB (27782312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77cd1cc39899f685ab213dd59e0118acb883d3b1731585c90c3430f6aa1756`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896eaca6d7996bb57c3b5ec364fb24e71197813972ed542981d3252f540a5988`  
		Last Modified: Fri, 02 Sep 2022 12:34:00 GMT  
		Size: 1.1 MB (1063958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68f6bc7839e5a951ef7151c7989756877fb0c5103e67e8bbe68c36db7aac737`  
		Last Modified: Fri, 02 Sep 2022 12:33:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk8`

```console
$ docker pull jruby@sha256:0bcfd070fc67fbd86261f1965994567b588d602ba8f2fdb914f61fe4c86deb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:f695ab6ea1b58d8cf9fb299b3c5893e211b2c57afff32f5a4e5bf802d4c47696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184207446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda8de9bf75339795051cdcb843855c1807cf807cebdcd18c7b1907da5a3c6d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:22:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:39 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:42 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18550d9ddf67d4e108d13aa0c1dd579f2b028ce4f42e1552635912494fca13`  
		Last Modified: Fri, 02 Sep 2022 05:28:23 GMT  
		Size: 103.5 MB (103516129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef9c3189859e7dc13c2a28f668f074df18fe3e1b4d4992dafa6d122543ab76`  
		Last Modified: Fri, 02 Sep 2022 05:28:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b504dcddeb1cc92bfd5c0b47070fa7c533367e01b5733c59d2abbea5517139f`  
		Last Modified: Fri, 02 Sep 2022 10:28:42 GMT  
		Size: 6.9 MB (6915887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bfba0cbf25da20fe2ff928cdf9de70870f4d28f310b7052895c8d3a8c4d62`  
		Last Modified: Fri, 02 Sep 2022 10:28:43 GMT  
		Size: 27.8 MB (27783796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4749a55d6b09b1da05246facd74cbc5b7bac5a87dfcaec0f4cb05b4a691e0501`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca2ff2ed778a77e4172c86cbcb760875645c7ae8313df669a641e8339ef849`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 1.1 MB (1065107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce028e6b24c6bed8a5a0e7d8ecff16b4d384c7b600835e1f89f5c1778f5eb818`  
		Last Modified: Fri, 02 Sep 2022 10:28:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:a73cfe44ffb1d01eb9d4933220ea173ad03a7c7f97e83fea44e4faef73f0417d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ce5abc6f99fdb5d9de28390b6063d3abae4db0eadd07ca23a7fd997092ff35`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:55:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:53 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:54 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:58 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9f5e81b92b1223d05a7c9b19dd42fdd37b67dc111f528a2146ca9b8a6a8e3e`  
		Last Modified: Fri, 02 Sep 2022 05:04:04 GMT  
		Size: 102.6 MB (102615803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e16267aa5111dcc21f9e8752f0fc1dcc095d9aab9c7d1bdedae2a6c07066f`  
		Last Modified: Fri, 02 Sep 2022 05:03:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab31d3c3307a126dcfaf026924a3a735e9d36434ffd224eacbca333a28dce94`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 5.6 MB (5640799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85b2210f7c2979df40f0518f34d86307eea46556b1e2e8cabb64fa3e98aa8a`  
		Last Modified: Fri, 02 Sep 2022 12:32:57 GMT  
		Size: 27.8 MB (27782330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7eadd3d489082690f27d6a08d767fb844fc029beb1da23864791dab466170`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809ecb919c369e8c8220628bfc966702d7de12e12cf12a7c3f2ac2b5bf39142`  
		Last Modified: Fri, 02 Sep 2022 12:32:55 GMT  
		Size: 1.1 MB (1063998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac1b6f6aac7d38ce355ba29d856aa7854edaaab8411f9fa84e32057473a7531`  
		Last Modified: Fri, 02 Sep 2022 12:32:54 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre11`

```console
$ docker pull jruby@sha256:6278ac5de324ecf4dbe7fd6a7070e4ba38627250279da26b3e461346d3a9ee37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:8c49083c918e0392f24856f95070c1a943a5240642d3a52df7d6a992503b9755
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127189519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc2897e5f88a80cc50145e974e9c8505f152df42c8eb465420561ddbd1527d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:17 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:23:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:24:59 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:25:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:25:01 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:25:10 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:25:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:25:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:25:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:25:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddda6ec262688890aa2b9a222c7ca51e80af02c42cc1b7b8955b12310d6807ce`  
		Last Modified: Fri, 02 Sep 2022 05:30:27 GMT  
		Size: 46.5 MB (46498253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0138e2de6ea801eeb1c2e66d418cfcdab9954f13cb1543d9109f321eb305d72`  
		Last Modified: Fri, 02 Sep 2022 05:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6f21aec53086beae6ea54ebd32cea2dbee2a518d1bc73b4715e590150cc74`  
		Last Modified: Fri, 02 Sep 2022 10:29:09 GMT  
		Size: 6.9 MB (6915884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd45f6b655625b189ae2d6ea8ad7912e7accb6a9ee085901f1a1062f5b0611f`  
		Last Modified: Fri, 02 Sep 2022 10:29:10 GMT  
		Size: 27.8 MB (27783727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b9cacf19b853994fd2fc07910df21ba7216958f07e8d32ca3a3dce516ad2e`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf32baa17033337036f1da7036898c12ae0673243daa02b35784270c8fe45fa6`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 1.1 MB (1065130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247a3daa1c4c7b1799d514a31a07cf2be94d4489add7cacab164bd34dfe1466a`  
		Last Modified: Fri, 02 Sep 2022 10:29:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:28eeb4ab70473e011d3b18704ef374afcbf1412b4b6019b64f2f3e3947bb4e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122723320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e99e051cd211d5b0fa32a278744b96588d03e7e5645d3df18ab53adffc9848`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:06 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:58:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:58:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 12:29:30 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:29:30 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:29:31 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:29:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:29:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:29:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:29:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:29:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:29:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:29:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db301fee8d91c824e142c1d38d51b84ff501ef078dfc46ab78ebce098e6d819`  
		Last Modified: Fri, 02 Sep 2022 05:06:43 GMT  
		Size: 44.8 MB (44827029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d551363a43231a26706abc066d3ee44f28f4b1e284b9aaceb2510b60a9fa926e`  
		Last Modified: Fri, 02 Sep 2022 05:06:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a061ba7f23bd4d7daaa60d76a7fc5478f3b39f5cc894bbd460ccd909e7d53`  
		Last Modified: Fri, 02 Sep 2022 12:33:28 GMT  
		Size: 5.6 MB (5640820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f43a23d7543a5799346bd77b9ad2ed117c64e9a5af9923d9752680ded743b5`  
		Last Modified: Fri, 02 Sep 2022 12:33:29 GMT  
		Size: 27.8 MB (27782321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc8c87e94acdc58294e3735cdf0e5af773671e8ebc5401ebcb7565b81e987c4`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b25fbf7c4e17872b68990eeb197cf03aec38c991246b6cc733829724751488`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 1.1 MB (1064001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42c4ed4fb6c6831041a7828d638f050cf9a79f1234bec09f27592984060f50`  
		Last Modified: Fri, 02 Sep 2022 12:33:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre8`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.7.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.7.0-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:42e8e67d79c81445eb06f4cc03f4801e9c47febf783f4589e55bf76554c808db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:4b9c8e9ea5d653568aa49435feb910e2a1f25f6f7e3e78313c41f7c41acbe561
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122499793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8ca8274bef3da0175eeb77aa8539c26a9bfcebac51e9fca62ca77b921556a7`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:21:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:22:13 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 05:23:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 05:23:05 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 10:24:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:24:18 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 10:24:19 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 10:24:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 10:24:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 10:24:29 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 10:24:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 10:24:29 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:24:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 10:24:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f80c8980f9f06aee22e21e38ab7452b7606849d865d759e3a22e38084fefdf4`  
		Last Modified: Fri, 02 Sep 2022 05:28:17 GMT  
		Size: 16.4 MB (16353281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c553f7e1777de17cb89552b5b769bdd4c50c39400441c2fe825cda8ed3b7`  
		Last Modified: Fri, 02 Sep 2022 05:29:02 GMT  
		Size: 41.8 MB (41808517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273ff4b1f258368f859eb729f5d2c04e004a32bcaa736ec80274b2a155d0e5`  
		Last Modified: Fri, 02 Sep 2022 05:28:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6a6e598c612647e37f672c7ffba304fefad999cdd83b5fc79e46d99140209`  
		Last Modified: Fri, 02 Sep 2022 10:28:07 GMT  
		Size: 6.9 MB (6915889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296850265c22492d34b749535d321baee0e6e0d80c8bbae8aa7c2263224798d`  
		Last Modified: Fri, 02 Sep 2022 10:28:08 GMT  
		Size: 27.8 MB (27783776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6745735efeffdbb3ff66a8cb37c7a9fb4eeb013ae595c9c5e3cde04b30f100`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6100cacb383d82a1897f686204bfc0900c55586b4246b88406ae62e34fa31`  
		Last Modified: Fri, 02 Sep 2022 10:28:06 GMT  
		Size: 1.1 MB (1065085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67447305a2a1f16dde004778e2db3b2339dc8d62ec11dc70cf9ac87c44c50f1f`  
		Last Modified: Fri, 02 Sep 2022 10:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3141f503db2cd4118c5f8e44cee397a785c4f609638512fc3b97c9bf64a12067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118699920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fa12e06814ea25be74fdb96b701632d5a6f252dedfba9b1aaebb6ce788744e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:55:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:55:51 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:56:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 02 Sep 2022 12:28:15 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:28:15 GMT
ENV JRUBY_VERSION=9.3.7.0
# Fri, 02 Sep 2022 12:28:16 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Fri, 02 Sep 2022 12:28:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 02 Sep 2022 12:28:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:20 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 02 Sep 2022 12:28:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 02 Sep 2022 12:28:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 02 Sep 2022 12:28:33 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 12:28:34 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 02 Sep 2022 12:28:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e9e85c7aa375e63b9d777ac18f1d9372bd66278ffb9973a545b3b9075d3e94`  
		Last Modified: Fri, 02 Sep 2022 05:03:57 GMT  
		Size: 16.2 MB (16216835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8e658a13784d0f672673b4bdf1a70ef54138a63d4195213326fb4f8b2d6a6`  
		Last Modified: Fri, 02 Sep 2022 05:04:50 GMT  
		Size: 40.8 MB (40803901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000f34c6253669811a319731ec6bd7411f182fd8c7bb717b30c545029b82993`  
		Last Modified: Fri, 02 Sep 2022 05:04:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8229c3a073458dd34e2f8d2bcded1a2ea5beac224384352a363bf08a2dd580f4`  
		Last Modified: Fri, 02 Sep 2022 12:32:05 GMT  
		Size: 5.6 MB (5640813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e0d3d5ec15005aaa9879f3d801da7d79132c23c84bd812d5f9bf485044bb0`  
		Last Modified: Fri, 02 Sep 2022 12:32:07 GMT  
		Size: 27.8 MB (27782086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c1b48183fa8402e34aae3b9ef7976f13c6838fcd962a12dd805551ad6410dd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950bc0651d8acfb5cd063506a8a62c204c06dc922780f691e7666b0b9e33eddd`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 1.1 MB (1063997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58eb0be0544a61278e219f4725b2441d189f87bfe4edff262f278f57379326c`  
		Last Modified: Fri, 02 Sep 2022 12:32:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
