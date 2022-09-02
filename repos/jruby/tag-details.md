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
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
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
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:aa26e1c6642207a3f563aaddc7893ff3e084dc13e50a0457d4a7845f66dcb58c
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
$ docker pull jruby@sha256:bf357fe58f0cbdb6709d9a802a625023052ef638de8e6ed12bb0897a0cb76b53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272791122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1051b5435ef42d414a60182aec66a369da4ea21e9575c40e0d25c440760c79`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:40:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:40:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:40:59 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:08:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:58 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:02 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:16 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938ca8142b40380f0a1cf951e3962e60237444871a4283f68afe50ab4769dbe`  
		Last Modified: Wed, 24 Aug 2022 19:47:02 GMT  
		Size: 194.9 MB (194877241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d770114966e3198ea928c59b7053d4ff71a98db0ffbdc12066174ae2322819`  
		Last Modified: Wed, 24 Aug 2022 19:46:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db8137044d48feac626e9e4651e2756f3d9da597c1aa0eb4f41839538af8358`  
		Last Modified: Wed, 24 Aug 2022 22:11:22 GMT  
		Size: 5.6 MB (5640837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d989ff6939eb6c4b143fa17455cb763a6cbf0d4c255902f8d7fcdeeedd893`  
		Last Modified: Wed, 24 Aug 2022 22:11:23 GMT  
		Size: 27.8 MB (27782098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89a352782b6917754ff5611dd222f62bcc5951ef9a80b954aaa62598a90ecd8`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55163db39d27f64f3cef5d03a241e9bc8068a23b909e7c778c982ec273f14be2`  
		Last Modified: Wed, 24 Aug 2022 22:11:21 GMT  
		Size: 1.1 MB (1063978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150236b7d260be26baa7f38a2c2b9b0749ade84cc9fcea9a1ab6e3e8f3e63a07`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:a2348785e6916cc4b29364162a9f3833b61e1df99c5753a5329e62d68da3a338
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
$ docker pull jruby@sha256:79e2f96b8b0925d456ad9514bc47b1947792d1d9cfb8d1f905b2ae7929ff7610
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273432048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e73d21e273cb5ac07729fe2fdb2f8eed48b8ce4552ad75c2e7375e9237198c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:44:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:42:14 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:42:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:42:33 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:09:34 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:09:34 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:09:35 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:39 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c0ceb097615de30aaa4bce5d78e683a09d3766624f531951238f11979cc7f`  
		Last Modified: Fri, 12 Aug 2022 17:55:33 GMT  
		Size: 20.8 MB (20839019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ce586470e708a85551aff42fc396cd685bbfec1da65b08353946a55a7b2d2`  
		Last Modified: Wed, 24 Aug 2022 19:49:31 GMT  
		Size: 190.9 MB (190911717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16045745fcc8bef66b5a239924807d14f1343126bbcc5a7608dcb0ca4e176d5`  
		Last Modified: Wed, 24 Aug 2022 19:49:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153694f9c5cdbd22a0a402d798dc601158c36b37b0f4f1e5741901a3d03b49b0`  
		Last Modified: Wed, 24 Aug 2022 22:11:39 GMT  
		Size: 5.6 MB (5643002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b1e7197fd2840e2cf7d2a2406166bb472f746f331a023ba7ccee7f6dfa580`  
		Last Modified: Wed, 24 Aug 2022 22:11:41 GMT  
		Size: 27.8 MB (27782016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc3a116498bd4a5a5a10f2ac057dfc8db30bbed85104aa980fd4a61569ef34`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1064810cc9299513fafe762a044f6cbc71314200410f8610f1d87b95d470b95`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 1.1 MB (1063989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30533d22a06779305323255abcb42fe1156ce072a35b637d3aaef124442b14b`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:38996202cc6b0399614ab58bf398fc2161b51cca15840f59d7f457da70c6bc7e
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
$ docker pull jruby@sha256:b0f20cdd621d0c8848d72b387b4f7291a0d8300f279c469cf7fb11cf4bde5454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a82b806a1a9a0a100a12a502dfe9723ea822c29b88aaf05e753dc6786538dab`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:41:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:41:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 22:08:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:21 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:22 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:08:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:08:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:08:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:08:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:40 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:08:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db84143dec85e9e2416ee905155de01a99b12e4315a7c0cb4ad910df687f125e`  
		Last Modified: Wed, 24 Aug 2022 19:48:28 GMT  
		Size: 44.8 MB (44824775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb96e92353178516a5bddf70ff598ee0fd673ebae64f5268eeffd5b41d0d11e`  
		Last Modified: Wed, 24 Aug 2022 19:48:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58744fd45ffe76b42bf62b7b2433a6c3fc1184ddb5d8cf4fa4889f1095d2385c`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 5.6 MB (5640815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ffcc0ad6423e3cd7c29dbb650f90365daed2ab6ac882297ce497880576394`  
		Last Modified: Wed, 24 Aug 2022 22:11:06 GMT  
		Size: 27.8 MB (27782132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b61d74c835810c81c4ac9e7c356eb0b06eac80454195b06f5dfd519f2b08fa4`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e31b9d8b0b6b888b44b7546b4fc14e8fa195d11a9cf84114806646039a465`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 1.1 MB (1063980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a8ce168e1acc1ece45e1743573cd2c187c60d88b4c0c206e843e7f26be6b6`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk11`

```console
$ docker pull jruby@sha256:aa26e1c6642207a3f563aaddc7893ff3e084dc13e50a0457d4a7845f66dcb58c
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
$ docker pull jruby@sha256:bf357fe58f0cbdb6709d9a802a625023052ef638de8e6ed12bb0897a0cb76b53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272791122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1051b5435ef42d414a60182aec66a369da4ea21e9575c40e0d25c440760c79`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:40:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:40:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:40:59 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:08:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:58 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:02 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:16 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938ca8142b40380f0a1cf951e3962e60237444871a4283f68afe50ab4769dbe`  
		Last Modified: Wed, 24 Aug 2022 19:47:02 GMT  
		Size: 194.9 MB (194877241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d770114966e3198ea928c59b7053d4ff71a98db0ffbdc12066174ae2322819`  
		Last Modified: Wed, 24 Aug 2022 19:46:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db8137044d48feac626e9e4651e2756f3d9da597c1aa0eb4f41839538af8358`  
		Last Modified: Wed, 24 Aug 2022 22:11:22 GMT  
		Size: 5.6 MB (5640837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d989ff6939eb6c4b143fa17455cb763a6cbf0d4c255902f8d7fcdeeedd893`  
		Last Modified: Wed, 24 Aug 2022 22:11:23 GMT  
		Size: 27.8 MB (27782098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89a352782b6917754ff5611dd222f62bcc5951ef9a80b954aaa62598a90ecd8`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55163db39d27f64f3cef5d03a241e9bc8068a23b909e7c778c982ec273f14be2`  
		Last Modified: Wed, 24 Aug 2022 22:11:21 GMT  
		Size: 1.1 MB (1063978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150236b7d260be26baa7f38a2c2b9b0749ade84cc9fcea9a1ab6e3e8f3e63a07`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk17`

```console
$ docker pull jruby@sha256:a2348785e6916cc4b29364162a9f3833b61e1df99c5753a5329e62d68da3a338
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
$ docker pull jruby@sha256:79e2f96b8b0925d456ad9514bc47b1947792d1d9cfb8d1f905b2ae7929ff7610
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273432048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e73d21e273cb5ac07729fe2fdb2f8eed48b8ce4552ad75c2e7375e9237198c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:44:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:42:14 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:42:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:42:33 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:09:34 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:09:34 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:09:35 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:39 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c0ceb097615de30aaa4bce5d78e683a09d3766624f531951238f11979cc7f`  
		Last Modified: Fri, 12 Aug 2022 17:55:33 GMT  
		Size: 20.8 MB (20839019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ce586470e708a85551aff42fc396cd685bbfec1da65b08353946a55a7b2d2`  
		Last Modified: Wed, 24 Aug 2022 19:49:31 GMT  
		Size: 190.9 MB (190911717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16045745fcc8bef66b5a239924807d14f1343126bbcc5a7608dcb0ca4e176d5`  
		Last Modified: Wed, 24 Aug 2022 19:49:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153694f9c5cdbd22a0a402d798dc601158c36b37b0f4f1e5741901a3d03b49b0`  
		Last Modified: Wed, 24 Aug 2022 22:11:39 GMT  
		Size: 5.6 MB (5643002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b1e7197fd2840e2cf7d2a2406166bb472f746f331a023ba7ccee7f6dfa580`  
		Last Modified: Wed, 24 Aug 2022 22:11:41 GMT  
		Size: 27.8 MB (27782016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc3a116498bd4a5a5a10f2ac057dfc8db30bbed85104aa980fd4a61569ef34`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1064810cc9299513fafe762a044f6cbc71314200410f8610f1d87b95d470b95`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 1.1 MB (1063989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30533d22a06779305323255abcb42fe1156ce072a35b637d3aaef124442b14b`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jdk8`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre11`

```console
$ docker pull jruby@sha256:38996202cc6b0399614ab58bf398fc2161b51cca15840f59d7f457da70c6bc7e
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
$ docker pull jruby@sha256:b0f20cdd621d0c8848d72b387b4f7291a0d8300f279c469cf7fb11cf4bde5454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a82b806a1a9a0a100a12a502dfe9723ea822c29b88aaf05e753dc6786538dab`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:41:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:41:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 22:08:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:21 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:22 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:08:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:08:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:08:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:08:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:40 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:08:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db84143dec85e9e2416ee905155de01a99b12e4315a7c0cb4ad910df687f125e`  
		Last Modified: Wed, 24 Aug 2022 19:48:28 GMT  
		Size: 44.8 MB (44824775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb96e92353178516a5bddf70ff598ee0fd673ebae64f5268eeffd5b41d0d11e`  
		Last Modified: Wed, 24 Aug 2022 19:48:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58744fd45ffe76b42bf62b7b2433a6c3fc1184ddb5d8cf4fa4889f1095d2385c`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 5.6 MB (5640815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ffcc0ad6423e3cd7c29dbb650f90365daed2ab6ac882297ce497880576394`  
		Last Modified: Wed, 24 Aug 2022 22:11:06 GMT  
		Size: 27.8 MB (27782132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b61d74c835810c81c4ac9e7c356eb0b06eac80454195b06f5dfd519f2b08fa4`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e31b9d8b0b6b888b44b7546b4fc14e8fa195d11a9cf84114806646039a465`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 1.1 MB (1063980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a8ce168e1acc1ece45e1743573cd2c187c60d88b4c0c206e843e7f26be6b6`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7-jre8`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk11`

```console
$ docker pull jruby@sha256:aa26e1c6642207a3f563aaddc7893ff3e084dc13e50a0457d4a7845f66dcb58c
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
$ docker pull jruby@sha256:bf357fe58f0cbdb6709d9a802a625023052ef638de8e6ed12bb0897a0cb76b53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272791122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1051b5435ef42d414a60182aec66a369da4ea21e9575c40e0d25c440760c79`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:40:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2b89cabf0ce1c2cedadd92b798d6e9056bc27c71a06f5ba24ede5dc9c316e3e8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='a703acfd04ece4a4aac4cb9bda26b7d225874008bba324237bd6f53792edb778';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b18877871eda801ccb99bb34c5d7d77fccf6adad02514110c21389632ec91024';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b16b1b50699a9caaae3d782be687625d81e069c886df904f83d13e6c4322a179';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f6b513757d386352cf91514ed5859d1ab59364b4453e1f1c57152ba2039b8e2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:40:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:40:59 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:08:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:58 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:59 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:02 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:16 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938ca8142b40380f0a1cf951e3962e60237444871a4283f68afe50ab4769dbe`  
		Last Modified: Wed, 24 Aug 2022 19:47:02 GMT  
		Size: 194.9 MB (194877241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d770114966e3198ea928c59b7053d4ff71a98db0ffbdc12066174ae2322819`  
		Last Modified: Wed, 24 Aug 2022 19:46:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db8137044d48feac626e9e4651e2756f3d9da597c1aa0eb4f41839538af8358`  
		Last Modified: Wed, 24 Aug 2022 22:11:22 GMT  
		Size: 5.6 MB (5640837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d989ff6939eb6c4b143fa17455cb763a6cbf0d4c255902f8d7fcdeeedd893`  
		Last Modified: Wed, 24 Aug 2022 22:11:23 GMT  
		Size: 27.8 MB (27782098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89a352782b6917754ff5611dd222f62bcc5951ef9a80b954aaa62598a90ecd8`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55163db39d27f64f3cef5d03a241e9bc8068a23b909e7c778c982ec273f14be2`  
		Last Modified: Wed, 24 Aug 2022 22:11:21 GMT  
		Size: 1.1 MB (1063978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150236b7d260be26baa7f38a2c2b9b0749ade84cc9fcea9a1ab6e3e8f3e63a07`  
		Last Modified: Wed, 24 Aug 2022 22:11:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk17`

```console
$ docker pull jruby@sha256:a2348785e6916cc4b29364162a9f3833b61e1df99c5753a5329e62d68da3a338
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
$ docker pull jruby@sha256:79e2f96b8b0925d456ad9514bc47b1947792d1d9cfb8d1f905b2ae7929ff7610
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273432048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e73d21e273cb5ac07729fe2fdb2f8eed48b8ce4552ad75c2e7375e9237198c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:44:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:42:14 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c7460de77421284b38b4e57cb1bd584a6cef55c34fc51a12270620544de2b8a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='efba97cd38af8f43b61f09cb5041f81d92ecd005dcd51c81678fbcf4f24d8461';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cbedd0a1428b3058d156e99e8e9bc8769e0d633736d6776a4c4d9136648f2fd1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fdc82f4b06c880762503b0cb40e25f46cf8190d06011b3b768f4091d3334ef7f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fbf8b62c44f10be2efab97c5f5dbf15b74fae31e451ec10abbc74e54a04ff44';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:42:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:42:33 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 22:09:34 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:09:34 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:09:35 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:09:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:39 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:09:49 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:09:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:09:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:09:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:09:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c0ceb097615de30aaa4bce5d78e683a09d3766624f531951238f11979cc7f`  
		Last Modified: Fri, 12 Aug 2022 17:55:33 GMT  
		Size: 20.8 MB (20839019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ce586470e708a85551aff42fc396cd685bbfec1da65b08353946a55a7b2d2`  
		Last Modified: Wed, 24 Aug 2022 19:49:31 GMT  
		Size: 190.9 MB (190911717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16045745fcc8bef66b5a239924807d14f1343126bbcc5a7608dcb0ca4e176d5`  
		Last Modified: Wed, 24 Aug 2022 19:49:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153694f9c5cdbd22a0a402d798dc601158c36b37b0f4f1e5741901a3d03b49b0`  
		Last Modified: Wed, 24 Aug 2022 22:11:39 GMT  
		Size: 5.6 MB (5643002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b1e7197fd2840e2cf7d2a2406166bb472f746f331a023ba7ccee7f6dfa580`  
		Last Modified: Wed, 24 Aug 2022 22:11:41 GMT  
		Size: 27.8 MB (27782016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc3a116498bd4a5a5a10f2ac057dfc8db30bbed85104aa980fd4a61569ef34`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1064810cc9299513fafe762a044f6cbc71314200410f8610f1d87b95d470b95`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 1.1 MB (1063989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30533d22a06779305323255abcb42fe1156ce072a35b637d3aaef124442b14b`  
		Last Modified: Wed, 24 Aug 2022 22:11:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jdk8`

```console
$ docker pull jruby@sha256:c69d433202055bcb8480bffc3b776548abce1bb897d7f86455c5102016769c9f
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
$ docker pull jruby@sha256:e5695766fd60ca1209e8faa7789193c2df96c079b5e0297c7b27dbf711bd9230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180528748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f3c9a47d68a974fa5569d0ec31a834b9a9538b9b4aa7c741508793956ed42`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:40:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c1965fb24dded7d7944e2da36cd902adf3b7b1d327aaa21ea507cff00a5a0090';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='af4ecd311df32b405142d5756f966418d0200fbf6cb9009c20a44dc691e8da6f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f2be72678f6c2ad283453d0e21a6cb03144dda356e4edf79f818d99c37feaf34';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ed6c9db3719895584fb1fd69fc79c29240977675f26631911c5a1dbce07b7d58';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:40:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:47 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:10:00 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:10:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:10:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:10:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:10:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:10:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:10:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f871e1e192822db9c46e06e0f4ed23e8fad24696eb3631a7ec73f578ecdce`  
		Last Modified: Fri, 12 Aug 2022 17:51:13 GMT  
		Size: 102.6 MB (102615754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034b87a5e3a148d948c506678d3ac2d5b154e2525ab78143192da4fbba9b19a`  
		Last Modified: Fri, 12 Aug 2022 17:51:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfa681985f0876c5367fed76aa8e8d9eeda457dc95c2ebd830d847e3e2d8df`  
		Last Modified: Fri, 12 Aug 2022 19:36:41 GMT  
		Size: 5.6 MB (5644265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaa0a2fd837ababa72213ec1dcef64928849dd31727c736a5d4712733acc747`  
		Last Modified: Wed, 17 Aug 2022 00:13:22 GMT  
		Size: 27.8 MB (27782033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed610a566dbb9742cd58a3d380925b550384017764d81d92234c11d39d434b`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e43662f2e9daad7f0320ef7ea204389587a000bfbdaf36f505bc6c2d09750ee`  
		Last Modified: Wed, 17 Aug 2022 00:13:20 GMT  
		Size: 1.1 MB (1059759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe4d37e10fad6299407f6b7b6b084012bc518743c58d2e4e3f1fc43225ed8e`  
		Last Modified: Wed, 17 Aug 2022 00:13:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre11`

```console
$ docker pull jruby@sha256:38996202cc6b0399614ab58bf398fc2161b51cca15840f59d7f457da70c6bc7e
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
$ docker pull jruby@sha256:b0f20cdd621d0c8848d72b387b4f7291a0d8300f279c469cf7fb11cf4bde5454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a82b806a1a9a0a100a12a502dfe9723ea822c29b88aaf05e753dc6786538dab`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:40:22 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:41:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:41:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 22:08:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 22:08:21 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 24 Aug 2022 22:08:22 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 24 Aug 2022 22:08:25 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 24 Aug 2022 22:08:25 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:26 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 24 Aug 2022 22:08:37 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 24 Aug 2022 22:08:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Aug 2022 22:08:40 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:08:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 24 Aug 2022 22:08:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db84143dec85e9e2416ee905155de01a99b12e4315a7c0cb4ad910df687f125e`  
		Last Modified: Wed, 24 Aug 2022 19:48:28 GMT  
		Size: 44.8 MB (44824775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb96e92353178516a5bddf70ff598ee0fd673ebae64f5268eeffd5b41d0d11e`  
		Last Modified: Wed, 24 Aug 2022 19:48:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58744fd45ffe76b42bf62b7b2433a6c3fc1184ddb5d8cf4fa4889f1095d2385c`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 5.6 MB (5640815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ffcc0ad6423e3cd7c29dbb650f90365daed2ab6ac882297ce497880576394`  
		Last Modified: Wed, 24 Aug 2022 22:11:06 GMT  
		Size: 27.8 MB (27782132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b61d74c835810c81c4ac9e7c356eb0b06eac80454195b06f5dfd519f2b08fa4`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e31b9d8b0b6b888b44b7546b4fc14e8fa195d11a9cf84114806646039a465`  
		Last Modified: Wed, 24 Aug 2022 22:11:04 GMT  
		Size: 1.1 MB (1063980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a8ce168e1acc1ece45e1743573cd2c187c60d88b4c0c206e843e7f26be6b6`  
		Last Modified: Wed, 24 Aug 2022 22:11:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.7.0-jre8`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:676ba7883e2cde1894a5eb82faf15915ca70a261ae25a43360daa0dadaa83e9f
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
$ docker pull jruby@sha256:066ccc18fd476403e2b1a7413f3c231867cd1eadf4e75824240fc6994b04a3ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118716905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aee362c392d35581b8f36ce4322795d8c24f961a00da8985e1ade463f1797`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 12 Aug 2022 19:32:10 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 17 Aug 2022 00:09:31 GMT
ENV JRUBY_VERSION=9.3.7.0
# Wed, 17 Aug 2022 00:09:32 GMT
ENV JRUBY_SHA256=94a7a8b3beeac2253a8876e73adfac6bececb2b54d2ddfa68f245dc81967d0c1
# Wed, 17 Aug 2022 00:09:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Wed, 17 Aug 2022 00:09:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:36 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Wed, 17 Aug 2022 00:09:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Wed, 17 Aug 2022 00:09:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Aug 2022 00:09:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Aug 2022 00:09:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Aug 2022 00:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4abd2d5e6a76c28aa9d6d587eff40b5fd58b134cd2bc648cac6240b269fbd32`  
		Last Modified: Fri, 12 Aug 2022 19:35:58 GMT  
		Size: 5.6 MB (5644262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2a5ece08c5e3d9f1890cac4014a46618ab8d0dd0377f5176b5aba3fd4375f`  
		Last Modified: Wed, 17 Aug 2022 00:12:39 GMT  
		Size: 27.8 MB (27782065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b55452775336bfc805534522c90b903b3ba773ea29cb106825d4a1f78329d`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed9c72feb134590f94de995777b2c98cd46c1556227432f515f135bb31ec23`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 1.1 MB (1059803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910316e31862906ec23714b5335e69e04d1c42e0c0ce1ce3fdcfa3a4446c3325`  
		Last Modified: Wed, 17 Aug 2022 00:12:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
